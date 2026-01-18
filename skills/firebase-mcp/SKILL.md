---
name: firebase-mcp
description: Firebase platform integration
---

# firebase-mcp

Firebase platform integration

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-firebase
```

### Step 2: Get API Credentials

Get your credentials from: https://console.firebase.google.com/project/_/settings/serviceaccounts/adminsdk

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "firebase": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-firebase"],
      "env": {
            "FIREBASE_PROJECT_ID": "your-project-id",
            "FIREBASE_PRIVATE_KEY": "your-private-key",
            "FIREBASE_CLIENT_EMAIL": "your-client-email"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available firebase commands"
```

---

## Environment Variables

- `FIREBASE_PROJECT_ID`: Required - Your project-id
- `FIREBASE_PRIVATE_KEY`: Required - Your private-key
- `FIREBASE_CLIENT_EMAIL`: Required - Your client-email

## Available Tools

- `get_document`
- `set_document`
- `query_collection`
- `delete_document`

## Quick Start Examples

### Example 1
```
User: "Help me with firebase"
```

## Documentation

See @anthropic/mcp-firebase documentation for more details.



## Author

google

## Version

1.0.0
