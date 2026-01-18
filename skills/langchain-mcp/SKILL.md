---
name: langchain-mcp
description: LangChain framework integration
---

# langchain-mcp

LangChain framework integration

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-langchain
```

### Step 2: Get API Credentials

Get your credentials from: https://smith.langchain.com/settings

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "langchain": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-langchain"],
      "env": {
            "LANGCHAIN_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available langchain commands"
```

---

## Environment Variables

- `LANGCHAIN_API_KEY`: Required - Your api-key

## Available Tools

- `run_chain`
- `list_chains`
- `trace`

## Quick Start Examples

### Example 1
```
User: "Help me with langchain"
```

## Documentation

See @anthropic/mcp-langchain documentation for more details.



## Author

langchain

## Version

1.0.0
