---
name: supabase-mcp
description: Supabase database, auth, and edge functions (Official)
---

# supabase-mcp

Supabase database, auth, and edge functions (Official)

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-supabase
```

### Step 2: Get API Credentials

Get your credentials from: https://app.supabase.com/project/_/settings/api

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "supabase": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-supabase"],
      "env": {
            "SUPABASE_URL": "https://your-project.supabase.co",
            "SUPABASE_KEY": "your-anon-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available supabase commands"
```

---

## Environment Variables

- `SUPABASE_URL`: Required - https://Your project.supabase.co
- `SUPABASE_KEY`: Required - Your anon-key

## Available Tools

- `query`
- `insert`
- `update`
- `delete`
- `rpc`

## Quick Start Examples

### Example 1
```
User: "Help me with supabase"
```

## Documentation

See @anthropic/mcp-supabase documentation for more details.

## Source

GitHub: https://github.com/supabase/mcp-server

## Author

Supabase

## Version

1.0.0
