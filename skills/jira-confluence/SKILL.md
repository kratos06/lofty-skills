---
name: jira-confluence
description: Integrate Jira and Confluence for seamless project documentation workflows. Use when linking Jira issues to Confluence pages, creating documentation from sprint/epic data, generating release notes, syncing issue status to docs, cross-referencing between systems, or building project dashboards. Triggers on requests involving both Jira tickets and Confluence pages, sprint documentation, release notes generation, or project status pages.
---

# Jira-Confluence Integration

Bidirectional integration between Jira and Confluence for project documentation, sprint reporting, and cross-referencing.

## Prerequisites

This skill requires the **Atlassian MCP Server** to be configured.

### Step 1: Install Atlassian MCP Server

```bash
npm install -g @anthropic/mcp-atlassian
```

### Step 2: Configure MCP Server

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "atlassian": {
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

### Step 3: Get Atlassian API Token

1. Go to https://id.atlassian.com/manage-profile/security/api-tokens
2. Click "Create API token"
3. Give it a name (e.g., "Claude Code")
4. Copy the token and add to your config

### Step 4: Verify Configuration

Restart Claude Code and test:
```
User: "Search for recent Jira issues"
```

If configured correctly, Claude will use `mcp__atlassian__search` to query your Atlassian instance.

---

## Quick Reference

| Task | Primary Tools |
|------|---------------|
| Search across both | `mcp__atlassian__search` (Rovo) |
| Get Jira issue | `mcp__atlassian__getJiraIssue` |
| Get Confluence page | `mcp__atlassian__getConfluencePage` |
| Create Confluence page | `mcp__atlassian__createConfluencePage` |
| Create Jira issue | `mcp__atlassian__createJiraIssue` |
| Link issue to page | `mcp__atlassian__getJiraIssueRemoteIssueLinks` |

## Core Workflows

### 1. Create Documentation from Jira Issues

```
User: "Create a Confluence page documenting epic PROJ-100"

Steps:
1. Get epic details: getJiraIssue(issueIdOrKey: "PROJ-100")
2. Get child issues: searchJiraIssuesUsingJql(jql: "parent = PROJ-100")
3. Get space ID: getConfluenceSpaces(keys: "DOCS")
4. Create page: createConfluencePage(spaceId, title, body in markdown)
```

### 2. Generate Sprint Documentation

```
User: "Create release notes for sprint 42"

Steps:
1. Get sprint issues: searchJiraIssuesUsingJql(jql: "sprint = 42 AND status = Done")
2. Group by type (features, bugs, improvements)
3. Create Confluence page with categorized list
4. Include issue keys as links: [PROJ-123](https://site.atlassian.net/browse/PROJ-123)
```

### 3. Cross-Reference Search

```
User: "Find all docs related to authentication"

Steps:
1. Use unified search: mcp__atlassian__search(query: "authentication")
2. Results include both Jira issues and Confluence pages
3. Use fetch() with ARI to get full details
```

### 4. Sync Issue Status to Documentation

```
User: "Update the project status page with current sprint progress"

Steps:
1. Get current sprint: searchJiraIssuesUsingJql(jql: "sprint in openSprints()")
2. Calculate metrics (done, in progress, todo counts)
3. Get existing page: getConfluencePage(pageId)
4. Update page: updateConfluencePage(pageId, newContent)
```

## Page Templates

### Release Notes Template

```markdown
# Release v{version} - {date}

## New Features
{for each Story/Feature in sprint where status=Done}
- **{summary}** ({key}) - {description snippet}

## Bug Fixes
{for each Bug in sprint where status=Done}
- {summary} ({key})

## Known Issues
{for each Bug in sprint where status!=Done}
- {summary} ({key}) - Status: {status}
```

### Sprint Report Template

```markdown
# Sprint {number} Report

**Duration:** {startDate} - {endDate}
**Goal:** {sprint goal}

## Metrics
- Completed: {done count}/{total count} ({percentage}%)
- Story Points: {completed points}/{committed points}

## Completed Items
| Key | Type | Summary | Assignee |
|-----|------|---------|----------|
{table rows}

## Carried Over
{items not completed}
```

## JQL Patterns for Documentation

| Purpose | JQL |
|---------|-----|
| Sprint completed items | `sprint = {id} AND status = Done` |
| Epic children | `parent = {epicKey}` or `"Epic Link" = {epicKey}` |
| Recent updates | `updated >= -7d AND project = {key}` |
| Release items | `fixVersion = {version}` |
| Team items | `assignee in membersOf("{team}")` |

## CQL Patterns for Confluence

| Purpose | CQL |
|---------|-----|
| Pages mentioning issue | `text ~ "PROJ-123"` |
| Space pages | `space = "DOCS" AND type = page` |
| Recent updates | `lastModified > now("-7d")` |
| By label | `label = "release-notes"` |

## Best Practices

1. **Always get cloudId first** - Use `getAccessibleAtlassianResources` if needed
2. **Use Rovo search for discovery** - `mcp__atlassian__search` searches both systems
3. **Markdown for content** - Both create/update page tools accept markdown
4. **Preserve page hierarchy** - Use `parentId` when creating child pages
5. **Include issue links** - Format: `[KEY-123](https://site.atlassian.net/browse/KEY-123)`

## Advanced Workflows

For complex integration patterns, see [references/advanced-workflows.md](references/advanced-workflows.md):
- Epic documentation hubs
- Automated status dashboards
- Meeting notes with issue links
- Technical specs from requirements
- Incident postmortem generation

## Error Handling

- **403 Forbidden**: Check space/project permissions
- **404 Not Found**: Verify cloudId, pageId, or issueKey
- **Invalid JQL/CQL**: Validate query syntax before execution
