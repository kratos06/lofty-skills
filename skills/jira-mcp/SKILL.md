---
name: jira-mcp
description: Jira issue management with JQL queries, transitions, and workflow automation
---

# jira-mcp

Jira issue management with JQL queries, transitions, and workflow automation

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-atlassian
```

### Step 2: Get API Credentials

Get your credentials from: https://id.atlassian.com/manage-profile/security/api-tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "jira": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-atlassian"],
      "env": {
            "ATLASSIAN_SITE_URL": "https://your-site.atlassian.net",
            "ATLASSIAN_USER_EMAIL": "your-email@example.com",
            "ATLASSIAN_API_TOKEN": "your-api-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available jira commands"
```

---

## Environment Variables

- `ATLASSIAN_SITE_URL`: Required - https://Your site.atlassian.net
- `ATLASSIAN_USER_EMAIL`: Required - Your email@example.com
- `ATLASSIAN_API_TOKEN`: Required - Your api-token

## Available Tools

- `getJiraIssue`
- `createJiraIssue`
- `searchJiraIssuesUsingJql`
- `transitionJiraIssue`

## Quick Start Examples

### Example 1
```
User: "Help me with jira"
```

## Documentation

See @anthropic/mcp-atlassian documentation for more details.

## Source

GitHub: https://github.com/atlassian/jira-mcp

## Author

Atlassian

## Version

1.1.0
