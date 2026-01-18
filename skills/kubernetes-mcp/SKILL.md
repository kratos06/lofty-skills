---
name: kubernetes-mcp
description: Kubernetes cluster operations and resource management
---

# kubernetes-mcp

Kubernetes cluster operations and resource management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "kubernetes-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-kubernetes"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add kubernetes-mcp
```

## Quick Start

After configuration, the kubernetes-mcp tools will be available in Claude Code.

## Features

- kubernetes
- k8s
- containers
- orchestration



## Source

GitHub: https://github.com/kubernetes/mcp-server

## Author

CNCF

## Version

1.0.0
