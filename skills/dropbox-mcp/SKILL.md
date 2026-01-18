---
name: dropbox-mcp
description: Dropbox cloud storage integration
---

# dropbox-mcp

Dropbox cloud storage integration

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-dropbox
```

### Step 2: Get API Credentials

Get your credentials from: https://www.dropbox.com/developers/apps

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "dropbox": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-dropbox"],
      "env": {
            "DROPBOX_ACCESS_TOKEN": "your-access-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available dropbox commands"
```

---

## Environment Variables

- `DROPBOX_ACCESS_TOKEN`: Required - Your access-token

## Available Tools

- `list_files`
- `get_file`
- `upload_file`
- `search`

## Quick Start Examples

### Example 1
```
User: "Help me with dropbox"
```

## Documentation

See @anthropic/mcp-dropbox documentation for more details.



## Author

dropbox

## Version

1.0.0
