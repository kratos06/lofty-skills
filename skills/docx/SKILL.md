---
name: docx
description: Create, edit, and analyze Word documents with support for tracked changes, templates, and formatting
---

# docx

Create, edit, and analyze Word documents with support for tracked changes, templates, and formatting

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-docx
# or
npm install -g @anthropic/mcp-docx
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "docx": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-docx"],
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

After installation, the docx tools will be available in Claude Code.

## Features

- word
- docx
- documents
- templates

## Documentation

https://code.claude.com/docs/en/skills/docx



## Author

Anthropic

## Version

1.5.0
