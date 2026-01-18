---
name: devops-skill
description: DevOps with CI/CD, infrastructure, and cloud platforms
---

# devops-skill

DevOps with CI/CD, infrastructure, and cloud platforms

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-devops-skill
# or
npm install -g @anthropic/mcp-devops-skill
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "devops-skill": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-devops-skill"],
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

After installation, the devops-skill tools will be available in Claude Code.

## Features

- devops
- cicd
- infrastructure





## Author

Anthropic

## Version

1.0.0
