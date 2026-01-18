---
name: grafana-mcp
description: Grafana dashboards and visualization
---

# grafana-mcp

Grafana dashboards and visualization

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-grafana
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "grafana": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-grafana"],
      "env": {
            "GRAFANA_URL": "http://localhost:3000",
            "GRAFANA_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available grafana commands"
```

---

## Environment Variables

- `GRAFANA_URL`: http://localhost:3000
- `GRAFANA_API_KEY`: Required - Your api-key

## Available Tools

- `list_dashboards`
- `get_dashboard`
- `query_datasource`

## Quick Start Examples

### Example 1
```
User: "Help me with grafana"
```

## Documentation

See @anthropic/mcp-grafana documentation for more details.



## Author

grafana

## Version

1.0.0
