---
name: slack-mcp
description: Slack messaging with channel management and bot capabilities
---

# slack-mcp

Slack messaging with channel management and bot capabilities

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-slack
```

### Step 2: Get API Credentials

Get your credentials from: https://api.slack.com/apps

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "slack": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-slack"],
      "env": {
            "SLACK_BOT_TOKEN": "xoxb-your-bot-token",
            "SLACK_TEAM_ID": "T0123456789"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available slack commands"
```

---

## Environment Variables

- `SLACK_BOT_TOKEN`: Required - xoxb-Your bot-token
- `SLACK_TEAM_ID`: T0123456789

## Available Tools

- `list_channels`
- `post_message`
- `get_channel_history`
- `search_messages`

## Quick Start Examples

### Example 1
```
User: "Help me with slack"
```

## Documentation

See @modelcontextprotocol/server-slack documentation for more details.

## Source

GitHub: https://github.com/slack/mcp-server

## Author

Slack

## Version

1.2.0
