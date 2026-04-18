# A2A-SIN-Research

Autonomous research agent for OpenSIN-AI.

## Purpose

Specialized research agent operating within the OpenSIN-AI ecosystem.

## Agent Configuration

| Property | Value |
|:---|:---|
| **Team** | Team Research |
| **Manager** | A2A-SIN-Research |
| **Type** | Research Agent |
| **Primary Model** | `gemini-3.1-pro` |

### Subagenten-Modelle (oh-my-openagent.json)

| Subagent | Modell |
|:---|:---|
| **explore** | `nvidia-nim/stepfun-ai/step-3.5-flash` |
| **librarian** | `nvidia-nim/stepfun-ai/step-3.5-flash` |

## Agent Config System v5

This agent is registered in the central team system:
- **Team Register:** `oh-my-sin.json` → `team-research`
- **Team Config:** `my-sin-team-research.json`

### PARALLEL-EXPLORATION MANDATE

Bei grossen Codebases (100k+ Zeilen) MUSS der Agent **5-10 parallele explore + 5-10 librarian-Agenten** starten.

→ [Full Documentation](https://github.com/OpenSIN-AI/OpenSIN-documentation/blob/main/docs/guide/agent-configuration.md)

## License

Apache-2.0
