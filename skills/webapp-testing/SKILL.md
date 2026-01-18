---
name: webapp-testing
description: Test local web applications using Playwright for UI verification and end-to-end testing
---

# webapp-testing

Test local web applications using Playwright for UI verification and end-to-end testing

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-webapp-testing
# or
npm install -g @anthropic/mcp-webapp-testing
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "webapp-testing": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-webapp-testing"],
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

After installation, the webapp-testing tools will be available in Claude Code.

## Features

- testing
- playwright
- e2e
- automation

## Documentation

https://code.claude.com/docs/en/skills/webapp-testing



## Author

Anthropic

## Version

1.0.0
