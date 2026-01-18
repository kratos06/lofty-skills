---
name: senior-fullstack
description: Full-stack development with modern web technologies
---

# senior-fullstack

Full-stack development with modern web technologies

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-senior-fullstack
# or
npm install -g @anthropic/mcp-senior-fullstack
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "senior-fullstack": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-senior-fullstack"],
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

After installation, the senior-fullstack tools will be available in Claude Code.

## Features

- fullstack
- web
- development





## Author

Anthropic

## Version

1.0.0
