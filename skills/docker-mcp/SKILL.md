---
name: docker-mcp
description: Docker container management, builds, and deployment
---

# docker-mcp

Docker container management, builds, and deployment

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "docker-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-docker"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add docker-mcp
```

## Quick Start

After configuration, the docker-mcp tools will be available in Claude Code.

## Features

- docker
- containers
- devops



## Source

GitHub: https://github.com/docker/mcp-server

## Author

Docker

## Version

1.0.0
