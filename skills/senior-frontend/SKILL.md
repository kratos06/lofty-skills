---
name: senior-frontend
description: Senior frontend development with React, Next.js, TypeScript, and Tailwind
---

# senior-frontend

Senior frontend development with React, Next.js, TypeScript, and Tailwind

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-senior-frontend
# or
npm install -g @anthropic/mcp-senior-frontend
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "senior-frontend": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-senior-frontend"],
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

After installation, the senior-frontend tools will be available in Claude Code.

## Features

- frontend
- react
- nextjs





## Author

Anthropic

## Version

1.0.0
