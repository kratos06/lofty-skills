---
name: atlassian-mcp
description: Unified Atlassian API integration for Jira, Confluence, and other Atlassian products
---

# atlassian-mcp

Unified Atlassian API integration for Jira, Confluence, and other Atlassian products

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "atlassian-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-atlassian"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add atlassian-mcp
```

## Quick Start

After configuration, the atlassian-mcp tools will be available in Claude Code.

## Features

- atlassian
- jira
- confluence
- api



## Source

GitHub: https://github.com/atlassian/mcp-server

## Author

Atlassian

## Version

1.2.0
