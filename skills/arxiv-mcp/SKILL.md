---
name: arxiv-mcp
description: arXiv academic papers search
---

# arxiv-mcp

arXiv academic papers search

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-arxiv
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "arxiv": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-arxiv"],
      "env": {}
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available arxiv commands"
```

---

## Environment Variables



## Available Tools

- `search`
- `get_paper`
- `download_pdf`

## Quick Start Examples

### Example 1
```
User: "Help me with arxiv"
```

## Documentation

See @anthropic/mcp-arxiv documentation for more details.



## Author

arxiv

## Version

1.0.0
