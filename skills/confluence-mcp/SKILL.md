---
name: confluence-mcp
description: Confluence page management with CQL queries and content creation
---

# confluence-mcp

Confluence page management with CQL queries and content creation

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "confluence-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-confluence"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add confluence-mcp
```

## Quick Start

After configuration, the confluence-mcp tools will be available in Claude Code.

## Features

- confluence
- pages
- documentation



## Source

GitHub: https://github.com/atlassian/confluence-mcp

## Author

Atlassian

## Version

1.1.0
