---
name: stability-mcp
description: Stability AI image generation
---

# stability-mcp

Stability AI image generation

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-stability
```

### Step 2: Get API Credentials

Get your credentials from: https://platform.stability.ai/account/keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "stability": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-stability"],
      "env": {
            "STABILITY_API_KEY": "sk-your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available stability commands"
```

---

## Environment Variables

- `STABILITY_API_KEY`: Required - sk-Your api-key

## Available Tools

- `generate_image`
- `upscale`
- `edit_image`

## Quick Start Examples

### Example 1
```
User: "Help me with stability"
```

## Documentation

See @anthropic/mcp-stability documentation for more details.



## Author

stability

## Version

1.0.0
