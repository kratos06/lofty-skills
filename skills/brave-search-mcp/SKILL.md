---
name: brave-search-mcp
description: Brave Search API integration
---

# brave-search-mcp

Brave Search API integration

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-brave-search
```

### Step 2: Get API Credentials

Get your credentials from: https://api.search.brave.com/app/keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "brave-search": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-brave-search"],
      "env": {
            "BRAVE_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available brave-search commands"
```

---

## Environment Variables

- `BRAVE_API_KEY`: Required - Your api-key

## Available Tools

- `web_search`
- `news_search`
- `image_search`

## Quick Start Examples

### Example 1
```
User: "Help me with brave-search"
```

## Documentation

See @anthropic/mcp-brave-search documentation for more details.

## Source

GitHub: https://github.com/anthropics/brave-search-mcp

## Author

Brave

## Version

1.0.0
