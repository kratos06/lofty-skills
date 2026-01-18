---
name: ollama-mcp
description: Ollama local LLM running and model management
---

# ollama-mcp

Ollama local LLM running and model management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-ollama
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "ollama": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-ollama"],
      "env": {
            "OLLAMA_HOST": "http://localhost:11434"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available ollama commands"
```

---

## Environment Variables

- `OLLAMA_HOST`: http://localhost:11434

## Available Tools

- `generate`
- `chat`
- `list_models`
- `pull_model`

## Quick Start Examples

### Example 1
```
User: "Help me with ollama"
```

## Documentation

See @anthropic/mcp-ollama documentation for more details.

## Source

GitHub: https://github.com/ollama/mcp-server

## Author

Ollama

## Version

1.0.0
