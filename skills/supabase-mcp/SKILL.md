---
name: supabase-mcp
description: Supabase database, auth, and edge functions (Official)
---

# supabase-mcp

Supabase database, auth, and edge functions (Official)

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "supabase-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-supabase"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add supabase-mcp
```

## Quick Start

After configuration, the supabase-mcp tools will be available in Claude Code.

## Features

- supabase
- database
- auth
- serverless



## Source

GitHub: https://github.com/supabase/mcp-server

## Author

Supabase

## Version

1.0.0
