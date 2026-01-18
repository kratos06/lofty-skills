---
name: artifacts-builder
description: Build complex claude.ai HTML artifacts using React, Tailwind CSS, and shadcn/ui
---

# artifacts-builder

Build complex claude.ai HTML artifacts using React, Tailwind CSS, and shadcn/ui

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-artifacts-builder
# or
npm install -g @anthropic/mcp-artifacts-builder
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "artifacts-builder": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-artifacts-builder"],
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

After installation, the artifacts-builder tools will be available in Claude Code.

## Features

- artifacts
- react
- tailwind
- html

## Documentation

https://code.claude.com/docs/en/skills/artifacts-builder



## Author

Anthropic

## Version

1.0.0
