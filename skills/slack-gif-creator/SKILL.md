---
name: slack-gif-creator
description: Create animated GIFs optimized for Slack's size constraints
---

# slack-gif-creator

Create animated GIFs optimized for Slack's size constraints

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-slack-gif-creator
# or
npm install -g @anthropic/mcp-slack-gif-creator
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "slack-gif-creator": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-slack-gif-creator"],
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

After installation, the slack-gif-creator tools will be available in Claude Code.

## Features

- slack
- gif
- animation





## Author

Anthropic

## Version

1.0.0
