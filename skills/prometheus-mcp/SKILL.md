---
name: prometheus-mcp
description: Prometheus metrics and alerting
---

# prometheus-mcp

Prometheus metrics and alerting

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "prometheus-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-prometheus"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add prometheus-mcp
```

## Quick Start

After configuration, the prometheus-mcp tools will be available in Claude Code.

## Features

- prometheus
- metrics
- alerting





## Author

prometheus

## Version

1.0.0
