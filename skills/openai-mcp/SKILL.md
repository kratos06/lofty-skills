---
name: openai-mcp
description: OpenAI API integration for GPT models and embeddings
---

# openai-mcp

OpenAI API integration for GPT models and embeddings

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-openai
```

### Step 2: Get API Credentials

Get your credentials from: https://platform.openai.com/api-keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "openai": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-openai"],
      "env": {
            "OPENAI_API_KEY": "sk-your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available openai commands"
```

---

## Environment Variables

- `OPENAI_API_KEY`: Required - sk-Your api-key

## Available Tools

- `chat`
- `complete`
- `embed`
- `create_image`

## Quick Start Examples

### Example 1
```
User: "Help me with openai"
```

## Documentation

See @anthropic/mcp-openai documentation for more details.

## Source

GitHub: https://github.com/openai/mcp-server

## Author

OpenAI

## Version

1.0.0
