---
name: devops
description: DevOps skill for CI/CD, infrastructure, and deployment automation
---

# devops

DevOps skill for CI/CD, infrastructure, and deployment automation

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-devops
# or
npm install -g @anthropic/mcp-devops
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "devops": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-devops"],
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

After installation, the devops tools will be available in Claude Code.

## Features

- devops
- ci-cd
- infrastructure



## Source

GitHub: https://github.com/community/devops-skill

## Author

Community

## Version

1.0.0
