---
name: planning
description: Implementation planning for multi-step tasks
---

# planning

Implementation planning for multi-step tasks

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-planning
# or
npm install -g @anthropic/mcp-planning
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "planning": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-planning"],
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

After installation, the planning tools will be available in Claude Code.

## Features

- planning
- tasks
- architecture





## Author

Anthropic

## Version

1.0.0
