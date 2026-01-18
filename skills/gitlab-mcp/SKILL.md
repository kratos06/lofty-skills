---
name: gitlab-mcp
description: GitLab projects, merge requests, and CI/CD
---

# gitlab-mcp

GitLab projects, merge requests, and CI/CD

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-gitlab
```

### Step 2: Get API Credentials

Get your credentials from: https://gitlab.com/-/profile/personal_access_tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "gitlab": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-gitlab"],
      "env": {
            "GITLAB_PERSONAL_ACCESS_TOKEN": "glpat-your-token",
            "GITLAB_API_URL": "https://gitlab.com/api/v4"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available gitlab commands"
```

---

## Environment Variables

- `GITLAB_PERSONAL_ACCESS_TOKEN`: Required - glpat-Your token
- `GITLAB_API_URL`: https://gitlab.com/api/v4

## Available Tools

- `list_projects`
- `get_file`
- `create_issue`
- `create_merge_request`

## Quick Start Examples

### Example 1
```
User: "Help me with gitlab"
```

## Documentation

See @modelcontextprotocol/server-gitlab documentation for more details.



## Author

gitlab

## Version

1.0.0
