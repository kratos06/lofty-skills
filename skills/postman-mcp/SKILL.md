---
name: postman-mcp
description: Postman API testing and collection management
---

# postman-mcp

Postman API testing and collection management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-postman
```

### Step 2: Get API Credentials

Get your credentials from: https://web.postman.co/settings/me/api-keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "postman": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-postman"],
      "env": {
            "POSTMAN_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available postman commands"
```

---

## Environment Variables

- `POSTMAN_API_KEY`: Required - Your api-key

## Available Tools

- `list_collections`
- `run_collection`
- `get_environment`

## Quick Start Examples

### Example 1
```
User: "Help me with postman"
```

## Documentation

See @anthropic/mcp-postman documentation for more details.



## Author

postman

## Version

1.0.0
