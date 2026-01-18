---
name: canvas-design
description: Create beautiful visual art in PNG and PDF formats using design principles
---

# canvas-design

Create beautiful visual art in PNG and PDF formats using design principles

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-canvas-design
# or
npm install -g @anthropic/mcp-canvas-design
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "canvas-design": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-canvas-design"],
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

After installation, the canvas-design tools will be available in Claude Code.

## Features

- design
- png
- pdf
- visual





## Author

Anthropic

## Version

1.0.0
