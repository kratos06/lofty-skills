---
name: cloudflare-mcp
description: Cloudflare Workers, KV, R2, and D1 management
---

# cloudflare-mcp

Cloudflare Workers, KV, R2, and D1 management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-cloudflare
```

### Step 2: Get API Credentials

Get your credentials from: https://dash.cloudflare.com/profile/api-tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "cloudflare": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-cloudflare"],
      "env": {
            "CLOUDFLARE_API_TOKEN": "your-api-token",
            "CLOUDFLARE_ACCOUNT_ID": "your-account-id"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available cloudflare commands"
```

---

## Environment Variables

- `CLOUDFLARE_API_TOKEN`: Required - Your api-token
- `CLOUDFLARE_ACCOUNT_ID`: Required - Your account-id

## Available Tools

- `list_zones`
- `list_workers`
- `deploy_worker`
- `kv_get`
- `kv_put`

## Quick Start Examples

### Example 1
```
User: "Help me with cloudflare"
```

## Documentation

See @anthropic/mcp-cloudflare documentation for more details.

## Source

GitHub: https://github.com/cloudflare/mcp-server

## Author

Cloudflare

## Version

1.0.0
