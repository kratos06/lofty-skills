---
name: data-engineer
description: Data engineering with pipelines, ETL, and data infrastructure
---

# data-engineer

Data engineering with pipelines, ETL, and data infrastructure

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-data-engineer
# or
npm install -g @anthropic/mcp-data-engineer
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "data-engineer": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-data-engineer"],
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

After installation, the data-engineer tools will be available in Claude Code.

## Features

- data
- etl
- pipelines





## Author

Anthropic

## Version

1.0.0
