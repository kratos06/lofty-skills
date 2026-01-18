---
name: grafana-mcp
description: Grafana dashboards and visualization
---

# grafana-mcp

Grafana dashboards and visualization

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "grafana-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-grafana"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add grafana-mcp
```

## Quick Start

After configuration, the grafana-mcp tools will be available in Claude Code.

## Features

- grafana
- dashboards
- visualization





## Author

grafana

## Version

1.0.0
