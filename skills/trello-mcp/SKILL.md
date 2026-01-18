---
name: trello-mcp
description: Trello boards, lists, and cards management
---

# trello-mcp

Trello boards, lists, and cards management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-trello
```

### Step 2: Get API Credentials

Get your credentials from: https://trello.com/app-key

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "trello": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-trello"],
      "env": {
            "TRELLO_API_KEY": "your-api-key",
            "TRELLO_TOKEN": "your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available trello commands"
```

---

## Environment Variables

- `TRELLO_API_KEY`: Required - Your api-key
- `TRELLO_TOKEN`: Required - Your token

## Available Tools

- `list_boards`
- `list_cards`
- `create_card`
- `move_card`

## Quick Start Examples

### Example 1
```
User: "Help me with trello"
```

## Documentation

See @anthropic/mcp-trello documentation for more details.



## Author

atlassian

## Version

1.0.0
