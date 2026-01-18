---
name: pptx
description: Create, edit, and analyze PowerPoint presentations with support for layouts, templates, charts, and automated slide generation
---

# pptx

Create, edit, and analyze PowerPoint presentations with support for layouts, templates, charts, and automated slide generation

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-pptx
# or
npm install -g @anthropic/mcp-pptx
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "pptx": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-pptx"],
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

After installation, the pptx tools will be available in Claude Code.

## Features

- powerpoint
- pptx
- presentations
- slides

## Documentation

https://code.claude.com/docs/en/skills/pptx



## Author

Anthropic

## Version

1.5.0
