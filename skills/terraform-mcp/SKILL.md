---
name: terraform-mcp
description: Terraform IaC with provider registry and best practices (Official HashiCorp)
---

# terraform-mcp

Terraform IaC with provider registry and best practices (Official HashiCorp)

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-terraform
```

### Step 2: Get API Credentials

Get your credentials from: https://app.terraform.io/app/settings/tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "terraform": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-terraform"],
      "env": {
            "TF_CLOUD_TOKEN": "your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available terraform commands"
```

---

## Environment Variables

- `TF_CLOUD_TOKEN`: Required - Your token

## Available Tools

- `plan`
- `apply`
- `show_state`
- `list_workspaces`

## Quick Start Examples

### Example 1
```
User: "Help me with terraform"
```

## Documentation

See @anthropic/mcp-terraform documentation for more details.

## Source

GitHub: https://github.com/hashicorp/terraform-mcp-server

## Author

HashiCorp

## Version

1.0.0
