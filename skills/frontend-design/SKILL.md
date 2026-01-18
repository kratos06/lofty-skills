---
name: frontend-design
description: React/Tailwind frontend design system with component scaffolding, performance optimization, and UI best practices
---

# frontend-design

React/Tailwind frontend design system with component scaffolding, performance optimization, and UI best practices

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-frontend-design
# or
npm install -g @anthropic/mcp-frontend-design
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "frontend-design": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-frontend-design"],
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

After installation, the frontend-design tools will be available in Claude Code.

## Features

- frontend
- react
- tailwind
- design
- ui

## Documentation

https://code.claude.com/docs/en/skills/frontend-design



## Author

Anthropic

## Version

1.2.0
