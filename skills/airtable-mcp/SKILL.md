---
name: airtable-mcp
description: Airtable database and spreadsheet operations
---

# airtable-mcp

Airtable database and spreadsheet operations

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "airtable-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-airtable"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add airtable-mcp
```

## Quick Start

After configuration, the airtable-mcp tools will be available in Claude Code.

## Features

- airtable
- database
- spreadsheet





## Author

airtable

## Version

1.0.0
