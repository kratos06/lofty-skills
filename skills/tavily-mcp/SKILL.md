---
name: tavily-mcp
description: Tavily AI search for LLMs
---

# tavily-mcp

Tavily AI search for LLMs

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-tavily
```

### Step 2: Get API Credentials

Get your credentials from: https://tavily.com/#api

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "tavily": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-tavily"],
      "env": {
            "TAVILY_API_KEY": "tvly-your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available tavily commands"
```

---

## Environment Variables

- `TAVILY_API_KEY`: Required - tvly-Your api-key

## Available Tools

- `search`
- `extract`

## Quick Start Examples

### Example 1
```
User: "Help me with tavily"
```

## Documentation

See @anthropic/mcp-tavily documentation for more details.



## Author

tavily

## Version

1.0.0
