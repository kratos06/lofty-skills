---
name: kaggle-mcp
description: Kaggle datasets, models, competitions, and notebooks
---

# kaggle-mcp

Kaggle datasets, models, competitions, and notebooks

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-kaggle
```

### Step 2: Get API Credentials

Get your credentials from: https://www.kaggle.com/settings/account

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "kaggle": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-kaggle"],
      "env": {
            "KAGGLE_USERNAME": "your-username",
            "KAGGLE_KEY": "your-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available kaggle commands"
```

---

## Environment Variables

- `KAGGLE_USERNAME`: Required - Your username
- `KAGGLE_KEY`: Required - Your key

## Available Tools

- `list_datasets`
- `download_dataset`
- `list_competitions`

## Quick Start Examples

### Example 1
```
User: "Help me with kaggle"
```

## Documentation

See @anthropic/mcp-kaggle documentation for more details.

## Source

GitHub: https://github.com/kaggle/mcp-server

## Author

Kaggle

## Version

1.0.0
