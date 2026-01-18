---
name: fly-mcp
description: Fly.io edge deployment platform
---

# fly-mcp

Fly.io edge deployment platform

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-fly
```

### Step 2: Get API Credentials

Get your credentials from: https://fly.io/user/personal_access_tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "fly": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-fly"],
      "env": {
            "FLY_API_TOKEN": "your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available fly commands"
```

---

## Environment Variables

- `FLY_API_TOKEN`: Required - Your token

## Available Tools

- `list_apps`
- `get_app`
- `deploy`
- `scale`

## Quick Start Examples

### Example 1
```
User: "Help me with fly"
```

## Documentation

See @anthropic/mcp-fly documentation for more details.



## Author

fly

## Version

1.0.0
