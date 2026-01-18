---
name: replicate-mcp
description: Replicate AI model hosting
---

# replicate-mcp

Replicate AI model hosting

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-replicate
```

### Step 2: Get API Credentials

Get your credentials from: https://replicate.com/account/api-tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "replicate": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-replicate"],
      "env": {
            "REPLICATE_API_TOKEN": "r8_your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available replicate commands"
```

---

## Environment Variables

- `REPLICATE_API_TOKEN`: Required - r8_Your token

## Available Tools

- `run`
- `list_models`
- `get_prediction`

## Quick Start Examples

### Example 1
```
User: "Help me with replicate"
```

## Documentation

See @anthropic/mcp-replicate documentation for more details.



## Author

replicate

## Version

1.0.0
