---
name: sharepoint-mcp
description: SharePoint document and site management
---

# sharepoint-mcp

SharePoint document and site management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "sharepoint-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-sharepoint"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add sharepoint-mcp
```

## Quick Start

After configuration, the sharepoint-mcp tools will be available in Claude Code.

## Features

- sharepoint
- documents
- intranet





## Author

microsoft

## Version

1.0.0
