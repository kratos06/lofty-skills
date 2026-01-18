---
name: tdd-guide
description: Test-driven development guide
---

# tdd-guide

Test-driven development guide

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-tdd-guide
# or
npm install -g @anthropic/mcp-tdd-guide
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "tdd-guide": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-tdd-guide"],
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

After installation, the tdd-guide tools will be available in Claude Code.

## Features

- tdd
- testing
- development





## Author

Anthropic

## Version

1.0.0
