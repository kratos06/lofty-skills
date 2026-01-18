---
name: brand-guidelines
description: Apply Anthropic's official brand colors, typography, and design guidelines
---

# brand-guidelines

Apply Anthropic's official brand colors, typography, and design guidelines

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-brand-guidelines
# or
npm install -g @anthropic/mcp-brand-guidelines
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "brand-guidelines": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-brand-guidelines"],
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

After installation, the brand-guidelines tools will be available in Claude Code.

## Features

- brand
- design
- guidelines

## Documentation

https://code.claude.com/docs/en/skills/brand-guidelines



## Author

Anthropic

## Version

1.0.0
