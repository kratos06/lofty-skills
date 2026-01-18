---
name: bitbucket-mcp
description: Bitbucket repositories and pipelines
---

# bitbucket-mcp

Bitbucket repositories and pipelines

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "bitbucket-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-bitbucket"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add bitbucket-mcp
```

## Quick Start

After configuration, the bitbucket-mcp tools will be available in Claude Code.

## Features

- bitbucket
- git
- atlassian





## Author

atlassian

## Version

1.0.0
