---
name: debugging
description: Advanced debugging and problem diagnosis skill
---

# debugging

Advanced debugging and problem diagnosis skill

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-debugging
# or
npm install -g @anthropic/mcp-debugging
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "debugging": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-debugging"],
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

After installation, the debugging tools will be available in Claude Code.

## Features

- debugging
- troubleshooting



## Source

GitHub: https://github.com/community/debugging-skill

## Author

Community

## Version

1.0.0
