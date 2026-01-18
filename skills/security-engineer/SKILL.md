---
name: security-engineer
description: Security engineering and penetration testing
---

# security-engineer

Security engineering and penetration testing

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-security-engineer
# or
npm install -g @anthropic/mcp-security-engineer
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "security-engineer": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-security-engineer"],
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

After installation, the security-engineer tools will be available in Claude Code.

## Features

- security
- pentesting
- audit





## Author

Anthropic

## Version

1.0.0
