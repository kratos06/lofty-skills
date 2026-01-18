---
name: langchain-mcp
description: LangChain framework integration
---

# langchain-mcp

LangChain framework integration

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "langchain-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-langchain"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add langchain-mcp
```

## Quick Start

After configuration, the langchain-mcp tools will be available in Claude Code.

## Features

- langchain
- llm
- framework





## Author

langchain

## Version

1.0.0
