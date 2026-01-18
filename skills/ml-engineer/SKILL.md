---
name: ml-engineer
description: ML engineering for model deployment and MLOps
---

# ml-engineer

ML engineering for model deployment and MLOps

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-ml-engineer
# or
npm install -g @anthropic/mcp-ml-engineer
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "ml-engineer": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-ml-engineer"],
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

After installation, the ml-engineer tools will be available in Claude Code.

## Features

- ml
- mlops
- deployment





## Author

Anthropic

## Version

1.0.0
