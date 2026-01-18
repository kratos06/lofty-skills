---
name: code-review-skill
description: Deep code review for architecture, security, and quality
---

# code-review-skill

Deep code review for architecture, security, and quality

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-code-review-skill
# or
npm install -g @anthropic/mcp-code-review-skill
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "code-review-skill": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-code-review-skill"],
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

After installation, the code-review-skill tools will be available in Claude Code.

## Features

- review
- code
- quality





## Author

Anthropic

## Version

1.0.0
