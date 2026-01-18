---
name: pdf
description: Comprehensive PDF manipulation toolkit for extracting text and tables, creating new PDFs, merging/splitting documents, and handling forms
---

# pdf

Comprehensive PDF manipulation toolkit for extracting text and tables, creating new PDFs, merging/splitting documents, and handling forms

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-pdf
# or
npm install -g @anthropic/mcp-pdf
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "pdf": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-pdf"],
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

After installation, the pdf tools will be available in Claude Code.

## Features

- pdf
- documents
- extraction
- merge
- forms

## Documentation

https://code.claude.com/docs/en/skills/pdf



## Author

Anthropic

## Version

2.0.0
