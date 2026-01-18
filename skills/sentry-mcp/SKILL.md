---
name: sentry-mcp
description: Sentry error tracking and performance monitoring
---

# sentry-mcp

Sentry error tracking and performance monitoring

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "sentry-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-sentry"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add sentry-mcp
```

## Quick Start

After configuration, the sentry-mcp tools will be available in Claude Code.

## Features

- sentry
- errors
- debugging



## Source

GitHub: https://github.com/sentry/mcp-server

## Author

Sentry

## Version

1.0.0
