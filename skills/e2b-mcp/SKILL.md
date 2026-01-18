---
name: e2b-mcp
description: E2B code sandbox execution
---

# e2b-mcp

E2B code sandbox execution

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-e2b
```

### Step 2: Get API Credentials

Get your credentials from: https://e2b.dev/dashboard/keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "e2b": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-e2b"],
      "env": {
            "E2B_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available e2b commands"
```

---

## Environment Variables

- `E2B_API_KEY`: Required - Your api-key

## Available Tools

- `create_sandbox`
- `run_code`
- `run_command`
- `upload_file`

## Quick Start Examples

### Example 1
```
User: "Help me with e2b"
```

## Documentation

See @anthropic/mcp-e2b documentation for more details.



## Author

E2B

## Version

1.0.0
