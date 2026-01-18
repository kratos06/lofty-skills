---
name: github-mcp
description: GitHub repository management, PRs, issues, and CI/CD workflows (Official)
---

# github-mcp

GitHub repository management, PRs, issues, and CI/CD workflows (Official)

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-github
```

### Step 2: Get API Credentials

Get your credentials from: https://github.com/settings/tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
            "GITHUB_PERSONAL_ACCESS_TOKEN": "ghp_your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available github commands"
```

---

## Environment Variables

- `GITHUB_PERSONAL_ACCESS_TOKEN`: Required - ghp_Your token

## Available Tools

- `search_repositories`
- `get_file_contents`
- `create_issue`
- `create_pull_request`

## Quick Start Examples

### Example 1
```
User: "Help me with github"
```

## Documentation

See @modelcontextprotocol/server-github documentation for more details.

## Source

GitHub: https://github.com/github/mcp-server

## Author

GitHub

## Version

1.5.0
