---
name: skill-creator
description: Interactive skill creation tool that guides you through building new Claude skills
---

# skill-creator

Interactive skill creation tool that guides you through building new Claude skills

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-skill-creator
# or
npm install -g @anthropic/mcp-skill-creator
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "skill-creator": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-skill-creator"],
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

After installation, the skill-creator tools will be available in Claude Code.

## Features

- skill
- creation
- development

## Documentation

https://code.claude.com/docs/en/skills/skill-creator



## Author

Anthropic

## Version

1.0.0
