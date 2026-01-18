---
name: slack-mcp
description: Slack messaging with channel management and bot capabilities
---

# slack-mcp

Slack messaging with channel management and bot capabilities

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "slack-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-slack"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add slack-mcp
```

## Quick Start

After configuration, the slack-mcp tools will be available in Claude Code.

## Features

- slack
- messaging
- chat



## Source

GitHub: https://github.com/slack/mcp-server

## Author

Slack

## Version

1.2.0
