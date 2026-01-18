---
name: vault-mcp
description: HashiCorp Vault secrets management and encryption
---

# vault-mcp

HashiCorp Vault secrets management and encryption

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-vault
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "vault": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-vault"],
      "env": {
            "VAULT_ADDR": "http://localhost:8200",
            "VAULT_TOKEN": "your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available vault commands"
```

---

## Environment Variables

- `VAULT_ADDR`: http://localhost:8200
- `VAULT_TOKEN`: Required - Your token

## Available Tools

- `read_secret`
- `write_secret`
- `list_secrets`
- `delete_secret`

## Quick Start Examples

### Example 1
```
User: "Help me with vault"
```

## Documentation

See @anthropic/mcp-vault documentation for more details.

## Source

GitHub: https://github.com/hashicorp/vault-mcp

## Author

HashiCorp

## Version

1.0.0
