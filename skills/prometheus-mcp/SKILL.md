---
name: prometheus-mcp
description: Prometheus metrics and alerting
---

# prometheus-mcp

Prometheus metrics and alerting

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-prometheus
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "prometheus": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-prometheus"],
      "env": {
            "PROMETHEUS_URL": "http://localhost:9090"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available prometheus commands"
```

---

## Environment Variables

- `PROMETHEUS_URL`: http://localhost:9090

## Available Tools

- `query`
- `query_range`
- `list_metrics`
- `get_alerts`

## Quick Start Examples

### Example 1
```
User: "Help me with prometheus"
```

## Documentation

See @anthropic/mcp-prometheus documentation for more details.



## Author

prometheus

## Version

1.0.0
