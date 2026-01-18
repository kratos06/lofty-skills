---
name: exa-mcp
description: Exa AI-powered search engine
---

# exa-mcp

Exa AI-powered search engine

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-exa
```

### Step 2: Get API Credentials

Get your credentials from: https://dashboard.exa.ai/api-keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "exa": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-exa"],
      "env": {
            "EXA_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available exa commands"
```

---

## Environment Variables

- `EXA_API_KEY`: Required - Your api-key

## Available Tools

- `search`
- `find_similar`
- `get_contents`

## Quick Start Examples

### Example 1
```
User: "Help me with exa"
```

## Documentation

See @anthropic/mcp-exa documentation for more details.



## Author

Exa

## Version

1.0.0
