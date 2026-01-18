---
name: ux-designer
description: UX design and research
---

# ux-designer

UX design and research

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-ux-designer
# or
npm install -g @anthropic/mcp-ux-designer
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "ux-designer": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-ux-designer"],
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

After installation, the ux-designer tools will be available in Claude Code.

## Features

- ux
- design
- research





## Author

Anthropic

## Version

1.0.0
