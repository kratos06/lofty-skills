---
name: docker-mcp
description: Docker container management, builds, and deployment
---

# docker-mcp

Docker container management, builds, and deployment

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-docker
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "docker": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-docker"],
      "env": {
            "DOCKER_HOST": "unix:///var/run/docker.sock"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available docker commands"
```

---

## Environment Variables

- `DOCKER_HOST`: unix:///var/run/docker.sock

## Available Tools

- `list_containers`
- `run_container`
- `stop_container`
- `list_images`
- `build_image`

## Quick Start Examples

### Example 1
```
User: "Help me with docker"
```

## Documentation

See @anthropic/mcp-docker documentation for more details.

## Source

GitHub: https://github.com/docker/mcp-server

## Author

Docker

## Version

1.0.0
