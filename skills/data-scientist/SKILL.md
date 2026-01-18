---
name: data-scientist
description: Data science with ML, statistics, and analytics
---

# data-scientist

Data science with ML, statistics, and analytics

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-data-scientist
# or
npm install -g @anthropic/mcp-data-scientist
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "data-scientist": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-data-scientist"],
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

After installation, the data-scientist tools will be available in Claude Code.

## Features

- data-science
- ml
- analytics





## Author

Anthropic

## Version

1.0.0
