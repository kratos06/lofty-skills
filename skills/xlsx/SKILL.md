---
name: xlsx
description: Create, edit, and analyze Excel spreadsheets with support for formulas, formatting, data analysis, and visualization
---

# xlsx

Create, edit, and analyze Excel spreadsheets with support for formulas, formatting, data analysis, and visualization

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-xlsx
# or
npm install -g @anthropic/mcp-xlsx
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "xlsx": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-xlsx"],
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

After installation, the xlsx tools will be available in Claude Code.

## Features

- excel
- spreadsheet
- xlsx
- formulas
- data-analysis

## Documentation

https://code.claude.com/docs/en/skills/xlsx



## Author

Anthropic

## Version

2.0.0
