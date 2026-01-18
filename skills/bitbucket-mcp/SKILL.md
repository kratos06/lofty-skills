---
name: bitbucket-mcp
description: Bitbucket repositories and pipelines
---

# bitbucket-mcp

Bitbucket repositories and pipelines

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-bitbucket
```

### Step 2: Get API Credentials

Get your credentials from: https://bitbucket.org/account/settings/app-passwords/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "bitbucket": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-bitbucket"],
      "env": {
            "BITBUCKET_USERNAME": "your-username",
            "BITBUCKET_APP_PASSWORD": "your-app-password"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available bitbucket commands"
```

---

## Environment Variables

- `BITBUCKET_USERNAME`: Required - Your username
- `BITBUCKET_APP_PASSWORD`: Required - Your app-password

## Available Tools

- `list_repos`
- `get_file`
- `create_pr`
- `list_prs`

## Quick Start Examples

### Example 1
```
User: "Help me with bitbucket"
```

## Documentation

See @anthropic/mcp-bitbucket documentation for more details.



## Author

atlassian

## Version

1.0.0
