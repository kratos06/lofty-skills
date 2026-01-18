---
name: qrcode-mcp
description: QR code generation and reading
---

# qrcode-mcp

QR code generation and reading

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "qrcode-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-qrcode"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add qrcode-mcp
```

## Quick Start

After configuration, the qrcode-mcp tools will be available in Claude Code.

## Features

- qrcode
- barcode
- generator





## Author

community

## Version

1.0.0
