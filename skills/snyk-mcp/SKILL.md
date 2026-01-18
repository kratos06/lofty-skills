---
name: snyk-mcp
description: Snyk security vulnerability scanning
---

# snyk-mcp

Snyk security vulnerability scanning

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-snyk
```

### Step 2: Get API Credentials

Get your credentials from: https://app.snyk.io/account

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "snyk": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-snyk"],
      "env": {
            "SNYK_TOKEN": "your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available snyk commands"
```

---

## Environment Variables

- `SNYK_TOKEN`: Required - Your token

## Available Tools

- `test`
- `monitor`
- `list_issues`
- `get_issue`

## Quick Start Examples

### Example 1
```
User: "Help me with snyk"
```

## Documentation

See @anthropic/mcp-snyk documentation for more details.



## Author

snyk

## Version

1.0.0
