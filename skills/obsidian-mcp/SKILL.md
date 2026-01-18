---
name: obsidian-mcp
description: Obsidian notes and knowledge base
---

# obsidian-mcp

Obsidian notes and knowledge base

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-obsidian
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "obsidian": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-obsidian"],
      "env": {
            "OBSIDIAN_VAULT_PATH": "/path/to/vault"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available obsidian commands"
```

---

## Environment Variables

- `OBSIDIAN_VAULT_PATH`: /path/to/vault

## Available Tools

- `read_note`
- `write_note`
- `search_notes`
- `list_notes`

## Quick Start Examples

### Example 1
```
User: "Help me with obsidian"
```

## Documentation

See @anthropic/mcp-obsidian documentation for more details.



## Author

obsidian

## Version

1.0.0
