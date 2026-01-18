---
name: code-review
description: Deep code review focusing on architecture, security, performance, and maintainability
---

# code-review

Deep code review focusing on architecture, security, performance, and maintainability

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-code-review
# or
npm install -g @anthropic/mcp-code-review
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "code-review": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-code-review"],
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

After installation, the code-review tools will be available in Claude Code.

## Features

- code-review
- quality
- security



## Source

GitHub: https://github.com/community/code-review-skill

## Author

Community

## Version

1.0.0
