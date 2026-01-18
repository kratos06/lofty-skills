---
name: mcp-builder
description: Guide for creating high-quality MCP servers to integrate external APIs and services
---

# mcp-builder

Guide for creating high-quality MCP servers to integrate external APIs and services

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "mcp-builder": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-mcp-builder"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add mcp-builder
```

## Quick Start

After configuration, the mcp-builder tools will be available in Claude Code.

## Features

- mcp
- api
- integration
- development

## Documentation

https://code.claude.com/docs/en/skills/mcp-builder



## Author

Anthropic

## Version

1.0.0
