---
name: npm-mcp
description: NPM package management and registry
---

# npm-mcp

NPM package management and registry

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-npm
```

### Step 2: Get API Credentials

Get your credentials from: https://www.npmjs.com/settings/~/tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "npm": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-npm"],
      "env": {
            "NPM_TOKEN": "your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available npm commands"
```

---

## Environment Variables

- `NPM_TOKEN`: Required - Your token

## Available Tools

- `search`
- `get_package`
- `list_versions`
- `publish`

## Quick Start Examples

### Example 1
```
User: "Help me with npm"
```

## Documentation

See @anthropic/mcp-npm documentation for more details.



## Author

npm

## Version

1.0.0
