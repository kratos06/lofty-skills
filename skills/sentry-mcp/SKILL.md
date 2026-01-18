---
name: sentry-mcp
description: Sentry error tracking and performance monitoring
---

# sentry-mcp

Sentry error tracking and performance monitoring

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-sentry
```

### Step 2: Get API Credentials

Get your credentials from: https://sentry.io/settings/account/api/auth-tokens/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "sentry": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-sentry"],
      "env": {
            "SENTRY_AUTH_TOKEN": "your-token",
            "SENTRY_ORG": "your-org"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available sentry commands"
```

---

## Environment Variables

- `SENTRY_AUTH_TOKEN`: Required - Your token
- `SENTRY_ORG`: Required - Your org

## Available Tools

- `list_issues`
- `get_issue`
- `resolve_issue`
- `list_events`

## Quick Start Examples

### Example 1
```
User: "Help me with sentry"
```

## Documentation

See @anthropic/mcp-sentry documentation for more details.

## Source

GitHub: https://github.com/sentry/mcp-server

## Author

Sentry

## Version

1.0.0
