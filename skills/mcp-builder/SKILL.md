---
name: mcp-builder
description: Guide for creating high-quality MCP servers to integrate external APIs and services
---

# mcp-builder

Guide for creating high-quality MCP servers to integrate external APIs and services

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-mcp-builder
# or
npm install -g @anthropic/mcp-mcp-builder
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "mcp-builder": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-mcp-builder"],
      "env": {
        // Add required environment variables
      }
    }
  }
}
```

### Step 3: Restart Claude Code

After configuration, restart Claude Code to load the MCP server.

## Quick Start

After installation, the mcp-builder tools will be available in Claude Code.

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
