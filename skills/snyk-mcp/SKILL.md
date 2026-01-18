---
name: snyk-mcp
description: Snyk security vulnerability scanning
---

# snyk-mcp

Snyk security vulnerability scanning

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "snyk-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-snyk"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add snyk-mcp
```

## Quick Start

After configuration, the snyk-mcp tools will be available in Claude Code.

## Features

- snyk
- security
- vulnerabilities





## Author

snyk

## Version

1.0.0
