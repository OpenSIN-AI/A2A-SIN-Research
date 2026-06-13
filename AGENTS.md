# A2A-SIN-Research — AGENTS.md

## Purpose

Autonomous research agent operating within the Team Research ecosystem.

## Rules

- NEVER ask user for manual help — find your own way
- ALWAYS use opencode CLI for LLM calls — never direct API calls
- ALWAYS publish logs and evidence to the approved artifact storage surface — never leave critical artifacts only on the local machine
- ALWAYS follow the Google account matrix for any Google operations
- ALWAYS use the approved OpenSIN browser automation surfaces — never ad-hoc raw automation

## LLM Call Architecture

```python
import subprocess, json

def call_llm(prompt, timeout=120):
    result = subprocess.run(
        ["opencode", "run", prompt, "--format", "json"],
        capture_output=True, text=True, timeout=timeout,
    )
    parts = []
    for line in result.stdout.splitlines():
        try:
            ev = json.loads(line)
            if ev.get("type") == "text":
                parts.append(ev.get("part", {}).get("text", ""))
        except json.JSONDecodeError:
            pass
    return "".join(parts).strip()
```

**Model:** `opencode/qwen3.6-plus-free` + `--fallback opencode/minimax-m2.5-free`

## PARALLEL-EXPLORATION MANDATE (PRIORITY -4.5)

Bei grossen Codebases (100k+ Zeilen, 1000+ Dateien) MUESSEN Agenten **5-10 parallele explore + 5-10 librarian-Agenten** starten.

```
task(subagent_type="explore", run_in_background=true, load_skills=[], description="Find APIs", prompt="[CONTEXT]: Grosse Codebase. [GOAL]: Alle API-Endpunkte. [REQUEST]: Dateipfade + Beschreibung.")
task(subagent_type="explore", run_in_background=true, load_skills=[], description="Find Services", prompt="[CONTEXT]: Grosse Codebase. [GOAL]: Alle Services. [REQUEST]: Dateipfade + Methoden.")
task(subagent_type="librarian", run_in_background=true, load_skills=[], description="Framework Docs", prompt="[GOAL]: Offizielle Doku. [REQUEST]: Best Practices.")
```

**HARTE REGELN:**
1. `run_in_background=true` ist PFLICHT
2. `load_skills=[]` ist PFLICHT
3. WARTEN bis ALLE background-Agenten fertig sind
4. Ergebnisse deduplizieren und zusammenfuehren

## Subagenten-Modelle

| Subagent | Modell | Fallback-Kette |
|:---|:---|:---|
| **explore** | `nvidia-nim/stepfun-ai/step-3.5-flash` | gemini-3-flash → gpt-5.4 → gemini-3.1-pro → claude-sonnet → qwen |
| **librarian** | `nvidia-nim/stepfun-ai/step-3.5-flash` | gemini-3-flash → gpt-5.4 → gemini-3.1-pro → claude-sonnet → qwen |

## Agent Config System v5

- **Team:** Team Research
- **Manager:** A2A-SIN-Research
- **Config:** `my-sin-team-research.json`
- **Team Register:** `oh-my-sin.json`

→ [Full Documentation](https://github.com/OpenSIN-AI/OpenSIN-documentation/blob/main/docs/guide/agent-configuration.md)

## Web Search Tools

For multi-source research, use the unified `sin-websearch` stack:
- MCP tools: `websearch_search`, `websearch_pulse`, `websearch_resolve`, `websearch_alchemist`
- Active repo: `OpenSIN-Code/web_search_bundle`
- Deprecated (archived): `OpenSIN-Code/SIN-Code-Websearch-Skill`, `OpenSIN-Code/SIN-Websearch-SerpAPI-Bundle`

## Boundary Guidance for Agents

When modifying this repo:

- Prefer autonomous research and knowledge synthesis work.
- Do not turn this repo into a generic platform bucket.
- Do not redefine organization docs, architecture, or runtime canon here.
- Move non-research behavior back to the repos that own those surfaces.
