---
name: vault-mcp
description: HashiCorp Vault secrets management and encryption
---

# vault-mcp

HashiCorp Vault secrets management and encryption

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "vault-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-vault"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add vault-mcp
```

## Quick Start

After configuration, the vault-mcp tools will be available in Claude Code.

## Features

- vault
- secrets
- security



## Source

GitHub: https://github.com/hashicorp/vault-mcp

## Author

HashiCorp

## Version

1.0.0
