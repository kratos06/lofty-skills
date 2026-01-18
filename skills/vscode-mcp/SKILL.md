---
name: vscode-mcp
description: VS Code editor integration and extensions
---

# vscode-mcp

VS Code editor integration and extensions

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-vscode
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "vscode": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-vscode"],
      "env": {}
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available vscode commands"
```

---

## Environment Variables



## Available Tools

- `open_file`
- `edit_file`
- `run_command`
- `get_diagnostics`

## Quick Start Examples

### Example 1
```
User: "Help me with vscode"
```

## Documentation

See @anthropic/mcp-vscode documentation for more details.



## Author

microsoft

## Version

1.0.0
