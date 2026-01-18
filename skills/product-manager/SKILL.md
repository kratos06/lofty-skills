---
name: product-manager
description: Product management with RICE, PRDs, and discovery
---

# product-manager

Product management with RICE, PRDs, and discovery

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-product-manager
# or
npm install -g @anthropic/mcp-product-manager
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "product-manager": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-product-manager"],
      "env": {
        // Add required environment variables
      }
    }
  }
}
```

### Step 3: Restart Claude Code

After configuration, restart Claude Code to load the MCP server.

## Quick Start

After installation, the product-manager tools will be available in Claude Code.

## Features

- product
- prd
- discovery





## Author

Anthropic

## Version

1.0.0
