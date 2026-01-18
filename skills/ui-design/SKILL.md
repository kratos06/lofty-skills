---
name: ui-design
description: UI design system toolkit
---

# ui-design

UI design system toolkit

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-ui-design
# or
npm install -g @anthropic/mcp-ui-design
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "ui-design": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-ui-design"],
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

After installation, the ui-design tools will be available in Claude Code.

## Features

- ui
- design
- systems





## Author

Anthropic

## Version

1.0.0
