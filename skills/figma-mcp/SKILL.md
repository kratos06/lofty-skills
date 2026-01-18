---
name: figma-mcp
description: Figma Dev Mode integration for design-to-code workflows
---

# figma-mcp

Figma Dev Mode integration for design-to-code workflows

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-figma
```

### Step 2: Get API Credentials

Get your credentials from: https://www.figma.com/developers/api#access-tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "figma": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-figma"],
      "env": {
            "FIGMA_ACCESS_TOKEN": "your-access-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available figma commands"
```

---

## Environment Variables

- `FIGMA_ACCESS_TOKEN`: Required - Your access-token

## Available Tools

- `get_file`
- `get_comments`
- `post_comment`
- `get_images`

## Quick Start Examples

### Example 1
```
User: "Help me with figma"
```

## Documentation

See @anthropic/mcp-figma documentation for more details.

## Source

GitHub: https://github.com/figma/mcp-server

## Author

Figma

## Version

1.0.0
