---
name: notion-mcp
description: Notion workspace integration with semantic search and page management
---

# notion-mcp

Notion workspace integration with semantic search and page management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-notion
```

### Step 2: Get API Credentials

Get your credentials from: https://www.notion.so/my-integrations

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "notion": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-notion"],
      "env": {
            "NOTION_API_TOKEN": "secret_your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available notion commands"
```

---

## Environment Variables

- `NOTION_API_TOKEN`: Required - secret_Your token

## Available Tools

- `search`
- `get_page`
- `create_page`
- `update_page`
- `query_database`

## Quick Start Examples

### Example 1
```
User: "Help me with notion"
```

## Documentation

See @modelcontextprotocol/server-notion documentation for more details.

## Source

GitHub: https://github.com/notion/mcp-server

## Author

Notion

## Version

1.0.0
