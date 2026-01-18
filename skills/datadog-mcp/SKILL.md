---
name: datadog-mcp
description: Datadog monitoring, logs, traces, and incident response (Official)
---

# datadog-mcp

Datadog monitoring, logs, traces, and incident response (Official)

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "datadog-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-datadog"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add datadog-mcp
```

## Quick Start

After configuration, the datadog-mcp tools will be available in Claude Code.

## Features

- datadog
- monitoring
- observability

## Documentation

https://docs.datadoghq.com/bits_ai/mcp_server/

## Source

GitHub: https://github.com/DataDog/mcp-server

## Author

Datadog

## Version

1.0.0
