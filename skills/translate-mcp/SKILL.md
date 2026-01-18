---
name: translate-mcp
description: Translation services integration
---

# translate-mcp

Translation services integration

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-translate
```

### Step 2: Get API Credentials

Get your credentials from: https://www.deepl.com/pro-api

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "translate": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-translate"],
      "env": {
            "DEEPL_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available translate commands"
```

---

## Environment Variables

- `DEEPL_API_KEY`: Required - Your api-key

## Available Tools

- `translate`
- `detect_language`
- `list_languages`

## Quick Start Examples

### Example 1
```
User: "Help me with translate"
```

## Documentation

See @anthropic/mcp-translate documentation for more details.



## Author

community

## Version

1.0.0
