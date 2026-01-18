---
name: ollama-mcp
description: Ollama local LLM running and model management
---

# ollama-mcp

Ollama local LLM running and model management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "ollama-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-ollama"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add ollama-mcp
```

## Quick Start

After configuration, the ollama-mcp tools will be available in Claude Code.

## Features

- ollama
- llm
- local



## Source

GitHub: https://github.com/ollama/mcp-server

## Author

Ollama

## Version

1.0.0
