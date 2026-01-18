---
name: openai-mcp
description: OpenAI API integration for GPT models and embeddings
---

# openai-mcp

OpenAI API integration for GPT models and embeddings

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "openai-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-openai"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add openai-mcp
```

## Quick Start

After configuration, the openai-mcp tools will be available in Claude Code.

## Features

- openai
- gpt
- ai
- llm



## Source

GitHub: https://github.com/openai/mcp-server

## Author

OpenAI

## Version

1.0.0
