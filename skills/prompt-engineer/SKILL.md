---
name: prompt-engineer
description: Prompt engineering and LLM optimization
---

# prompt-engineer

Prompt engineering and LLM optimization

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-prompt-engineer
# or
npm install -g @anthropic/mcp-prompt-engineer
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "prompt-engineer": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-prompt-engineer"],
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

After installation, the prompt-engineer tools will be available in Claude Code.

## Features

- prompt
- llm
- optimization





## Author

Anthropic

## Version

1.0.0
