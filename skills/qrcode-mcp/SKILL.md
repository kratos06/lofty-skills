---
name: qrcode-mcp
description: QR code generation and reading
---

# qrcode-mcp

QR code generation and reading

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-qrcode
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "qrcode": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-qrcode"],
      "env": {}
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available qrcode commands"
```

---

## Environment Variables



## Available Tools

- `generate`
- `read`

## Quick Start Examples

### Example 1
```
User: "Help me with qrcode"
```

## Documentation

See @anthropic/mcp-qrcode documentation for more details.



## Author

community

## Version

1.0.0
