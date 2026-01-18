---
name: internal-comms
description: Write internal communications like status reports, newsletters, FAQs, and incident reports
---

# internal-comms

Write internal communications like status reports, newsletters, FAQs, and incident reports

## Installation

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-internal-comms
# or
npm install -g @anthropic/mcp-internal-comms
```

### Step 2: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json`):

```json
{
  "mcpServers": {
    "internal-comms": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-internal-comms"],
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

After installation, the internal-comms tools will be available in Claude Code.

## Features

- communication
- reports
- documentation

## Documentation

https://code.claude.com/docs/en/skills/internal-comms



## Author

Anthropic

## Version

1.0.0
