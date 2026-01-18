---
name: gcp-mcp
description: Google Cloud Platform integration for compute, storage, and AI services
---

# gcp-mcp

Google Cloud Platform integration for compute, storage, and AI services

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-gcp
```

### Step 2: Get API Credentials

Get your credentials from: https://console.cloud.google.com/iam-admin/serviceaccounts

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "gcp": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-gcp"],
      "env": {
            "GOOGLE_APPLICATION_CREDENTIALS": "/path/to/service-account.json",
            "GCP_PROJECT_ID": "your-project-id"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available gcp commands"
```

---

## Environment Variables

- `GOOGLE_APPLICATION_CREDENTIALS`: /path/to/service-account.json
- `GCP_PROJECT_ID`: Required - Your project-id

## Available Tools

- `list_buckets`
- `list_instances`
- `run_query`

## Quick Start Examples

### Example 1
```
User: "Help me with gcp"
```

## Documentation

See @anthropic/mcp-gcp documentation for more details.

## Source

GitHub: https://github.com/google/gcp-mcp

## Author

Google

## Version

1.0.0
