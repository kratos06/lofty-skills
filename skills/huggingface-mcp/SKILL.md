---
name: huggingface-mcp
description: Hugging Face models, datasets, and inference API
---

# huggingface-mcp

Hugging Face models, datasets, and inference API

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-huggingface
```

### Step 2: Get API Credentials

Get your credentials from: https://huggingface.co/settings/tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "huggingface": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-huggingface"],
      "env": {
            "HUGGINGFACE_API_KEY": "hf_your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available huggingface commands"
```

---

## Environment Variables

- `HUGGINGFACE_API_KEY`: Required - hf_Your api-key

## Available Tools

- `inference`
- `list_models`
- `get_model`

## Quick Start Examples

### Example 1
```
User: "Help me with huggingface"
```

## Documentation

See @anthropic/mcp-huggingface documentation for more details.

## Source

GitHub: https://github.com/huggingface/mcp-server

## Author

Hugging Face

## Version

1.0.0
