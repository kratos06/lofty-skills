---
name: airtable-mcp
description: Airtable database and spreadsheet operations
---

# airtable-mcp

Airtable database and spreadsheet operations

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-airtable
```

### Step 2: Get API Credentials

Get your credentials from: https://airtable.com/create/tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "airtable": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-airtable"],
      "env": {
            "AIRTABLE_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available airtable commands"
```

---

## Environment Variables

- `AIRTABLE_API_KEY`: Required - Your api-key

## Available Tools

- `list_records`
- `get_record`
- `create_record`
- `update_record`

## Quick Start Examples

### Example 1
```
User: "Help me with airtable"
```

## Documentation

See @anthropic/mcp-airtable documentation for more details.



## Author

airtable

## Version

1.0.0
