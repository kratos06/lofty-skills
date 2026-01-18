---
name: cloudinary-mcp
description: Cloudinary media management
---

# cloudinary-mcp

Cloudinary media management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-cloudinary
```

### Step 2: Get API Credentials

Get your credentials from: https://console.cloudinary.com/settings/api-keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "cloudinary": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-cloudinary"],
      "env": {
            "CLOUDINARY_CLOUD_NAME": "your-cloud-name",
            "CLOUDINARY_API_KEY": "your-api-key",
            "CLOUDINARY_API_SECRET": "your-api-secret"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available cloudinary commands"
```

---

## Environment Variables

- `CLOUDINARY_CLOUD_NAME`: Required - Your cloud-name
- `CLOUDINARY_API_KEY`: Required - Your api-key
- `CLOUDINARY_API_SECRET`: Required - Your api-secret

## Available Tools

- `upload`
- `search`
- `transform`
- `delete`

## Quick Start Examples

### Example 1
```
User: "Help me with cloudinary"
```

## Documentation

See @anthropic/mcp-cloudinary documentation for more details.



## Author

cloudinary

## Version

1.0.0
