---
name: kubernetes-mcp
description: Kubernetes cluster operations and resource management
---

# kubernetes-mcp

Kubernetes cluster operations and resource management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-kubernetes
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "kubernetes": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-kubernetes"],
      "env": {
            "KUBECONFIG": "~/.kube/config"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available kubernetes commands"
```

---

## Environment Variables

- `KUBECONFIG`: ~/.kube/config

## Available Tools

- `get_pods`
- `get_deployments`
- `apply`
- `delete`
- `logs`

## Quick Start Examples

### Example 1
```
User: "Help me with kubernetes"
```

## Documentation

See @anthropic/mcp-kubernetes documentation for more details.

## Source

GitHub: https://github.com/kubernetes/mcp-server

## Author

CNCF

## Version

1.0.0
