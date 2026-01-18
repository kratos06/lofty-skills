---
name: netlify-mcp
description: Netlify site deployment and functions
---

# netlify-mcp

Netlify site deployment and functions

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-netlify
```

### Step 2: Get API Credentials

Get your credentials from: https://app.netlify.com/user/applications#personal-access-tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "netlify": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-netlify"],
      "env": {
            "NETLIFY_AUTH_TOKEN": "your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available netlify commands"
```

---

## Environment Variables

- `NETLIFY_AUTH_TOKEN`: Required - Your token

## Available Tools

- `list_sites`
- `get_site`
- `create_deploy`
- `list_deploys`

## Quick Start Examples

### Example 1
```
User: "Help me with netlify"
```

## Documentation

See @anthropic/mcp-netlify documentation for more details.

## Source

GitHub: https://github.com/netlify/mcp-server

## Author

Netlify

## Version

1.0.0
