---
name: algorithmic-art
description: Create generative art using p5.js with seeded randomness, flow fields, and particle systems
---

# algorithmic-art

Create generative art using p5.js with seeded randomness, flow fields, and particle systems

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-algorithmic-art
# or
npm install -g @anthropic/mcp-algorithmic-art
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "algorithmic-art": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-algorithmic-art"],
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

After installation, the algorithmic-art tools will be available in Claude Code.

## Features

- art
- generative
- p5js
- creative

## Documentation

https://code.claude.com/docs/en/skills/algorithmic-art



## Author

Anthropic

## Version

1.0.0
