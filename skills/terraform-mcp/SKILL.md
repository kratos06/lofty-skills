---
name: terraform-mcp
description: Terraform IaC with provider registry and best practices (Official HashiCorp)
---

# terraform-mcp

Terraform IaC with provider registry and best practices (Official HashiCorp)

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "terraform-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-terraform"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add terraform-mcp
```

## Quick Start

After configuration, the terraform-mcp tools will be available in Claude Code.

## Features

- terraform
- iac
- infrastructure



## Source

GitHub: https://github.com/hashicorp/terraform-mcp-server

## Author

HashiCorp

## Version

1.0.0
