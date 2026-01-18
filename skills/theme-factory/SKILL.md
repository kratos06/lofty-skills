---
name: theme-factory
description: Toolkit for styling artifacts with professional themes including colors and fonts
---

# theme-factory

Toolkit for styling artifacts with professional themes including colors and fonts

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-theme-factory
# or
npm install -g @anthropic/mcp-theme-factory
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "theme-factory": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-theme-factory"],
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

After installation, the theme-factory tools will be available in Claude Code.

## Features

- themes
- styling
- design





## Author

Anthropic

## Version

1.0.0
