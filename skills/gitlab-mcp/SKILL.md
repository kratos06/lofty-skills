---
name: gitlab-mcp
description: GitLab projects, merge requests, and CI/CD
---

# gitlab-mcp

GitLab projects, merge requests, and CI/CD

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "gitlab-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-gitlab"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add gitlab-mcp
```

## Quick Start

After configuration, the gitlab-mcp tools will be available in Claude Code.

## Features

- gitlab
- git
- devops





## Author

gitlab

## Version

1.0.0
