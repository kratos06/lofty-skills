---
name: datadog-mcp
description: Datadog monitoring, logs, traces, and incident response (Official)
---

# datadog-mcp

Datadog monitoring, logs, traces, and incident response (Official)

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-datadog
```

### Step 2: Get API Credentials

Get your credentials from: https://app.datadoghq.com/organization-settings/api-keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "datadog": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-datadog"],
      "env": {
            "DATADOG_API_KEY": "your-api-key",
            "DATADOG_APP_KEY": "your-app-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available datadog commands"
```

---

## Environment Variables

- `DATADOG_API_KEY`: Required - Your api-key
- `DATADOG_APP_KEY`: Required - Your app-key

## Available Tools

- `query_metrics`
- `list_monitors`
- `create_event`
- `search_logs`

## Quick Start Examples

### Example 1
```
User: "Help me with datadog"
```

## Documentation

Official docs: https://docs.datadoghq.com/bits_ai/mcp_server/

## Source

GitHub: https://github.com/DataDog/mcp-server

## Author

Datadog

## Version

1.0.0
