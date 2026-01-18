---
name: github-mcp
description: GitHub repository management, PRs, issues, and CI/CD workflows (Official)
---

# github-mcp

GitHub repository management, PRs, issues, and CI/CD workflows (Official)

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "github-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add github-mcp
```

## Quick Start

After configuration, the github-mcp tools will be available in Claude Code.

## Features

- github
- git
- repository
- ci-cd



## Source

GitHub: https://github.com/github/mcp-server

## Author

GitHub

## Version

1.5.0
