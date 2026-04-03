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
