# A2A-SIN-Research

> Research A2A agent.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Stars](https://img.shields.io/github/stars/OpenSIN-AI/A2A-SIN-Research)](https://github.com/OpenSIN-AI/A2A-SIN-Research)

## Overview

Multi-source information gathering, analysis, and structured research artifact generation.

## Quick Start

```bash
git clone https://github.com/OpenSIN-AI/A2A-SIN-Research.git
cd A2A-SIN-Research
npm install
npm start
```

## Features

- A2A protocol support for agent-to-agent communication
- MCP stdio transport integration
- CLI wrapper for local and automated use
- Docker-ready deployment

## Architecture

A2A agent with JSON-RPC runtime, MCP stdio transport, and Docker deployment support.

### A2A Surface

- Card: `GET /.well-known/agent-card.json`
- Health: `GET /health`
- RPC: `POST /a2a/v1`

### MCP Surface

- Transport: `stdio`

## API Reference

### Local Commands

```bash
npm start
npm run build
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT — See [LICENSE](LICENSE).

---

## 📚 Documentation

Full documentation: **[docs.opensin.ai](https://docs.opensin.ai)**

| Section | Link |
|---------|------|
| Getting Started | [Guide](https://docs.opensin.ai/guide/getting-started) |
| API Reference | [API](https://docs.opensin.ai/api/overview) |
| Tutorials | [Tutorials](https://docs.opensin.ai/tutorials/agent-basics) |
| Integrations | [Integrations](https://docs.opensin.ai/integrations/telegram) |
| Architecture | [Architecture](https://docs.opensin.ai/architecture/overview) |
| Community | [Discord](https://discord.gg/opensin) |


## 📚 Documentation

This repository follows the [Global Dev Docs Standard](https://github.com/OpenSIN-AI/Global-Dev-Docs-Standard).

For contribution guidelines, see [CONTRIBUTING.md](CONTRIBUTING.md).
For security policy, see [SECURITY.md](SECURITY.md).
For the complete OpenSIN ecosystem, see [OpenSIN-AI Organization](https://github.com/OpenSIN-AI).

## 🔗 See Also

- [OpenSIN Core](https://github.com/OpenSIN-AI/OpenSIN) — Main platform
- [OpenSIN-Code](https://github.com/OpenSIN-AI/OpenSIN-Code) — CLI
- [OpenSIN-backend](https://github.com/OpenSIN-AI/OpenSIN-backend) — Backend
- [OpenSIN-Infrastructure](https://github.com/OpenSIN-AI/OpenSIN-Infrastructure) — Deploy
- [Global Dev Docs Standard](https://github.com/OpenSIN-AI/Global-Dev-Docs-Standard) — Docs
