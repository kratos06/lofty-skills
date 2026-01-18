---
name: google-workspace-mcp
description: Google Workspace integration for Docs, Sheets, Drive, and Calendar
---

# google-workspace-mcp

Google Workspace integration for Docs, Sheets, Drive, and Calendar

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "google-workspace-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-google-workspace"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add google-workspace-mcp
```

## Quick Start

After configuration, the google-workspace-mcp tools will be available in Claude Code.

## Features

- google
- workspace
- productivity



## Source

GitHub: https://github.com/google/mcp-server

## Author

Google

## Version

1.0.0
