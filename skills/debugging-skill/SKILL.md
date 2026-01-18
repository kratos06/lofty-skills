---
name: debugging-skill
description: Bug investigation and root cause analysis
---

# debugging-skill

Bug investigation and root cause analysis

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-debugging-skill
# or
npm install -g @anthropic/mcp-debugging-skill
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "debugging-skill": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-debugging-skill"],
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

After installation, the debugging-skill tools will be available in Claude Code.

## Features

- debugging
- bugs
- analysis





## Author

Anthropic

## Version

1.0.0
