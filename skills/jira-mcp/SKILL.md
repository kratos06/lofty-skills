---
name: jira-mcp
description: Jira issue management with JQL queries, transitions, and workflow automation
---

# jira-mcp

Jira issue management with JQL queries, transitions, and workflow automation

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "jira-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-jira"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add jira-mcp
```

## Quick Start

After configuration, the jira-mcp tools will be available in Claude Code.

## Features

- jira
- issues
- workflow



## Source

GitHub: https://github.com/atlassian/jira-mcp

## Author

Atlassian

## Version

1.1.0
