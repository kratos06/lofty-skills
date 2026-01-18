# Advanced Jira-Confluence Workflows

## Table of Contents
- [Epic Documentation Hub](#epic-documentation-hub)
- [Automated Status Dashboards](#automated-status-dashboards)
- [Meeting Notes with Issue Links](#meeting-notes-with-issue-links)
- [Technical Spec from Requirements](#technical-spec-from-requirements)
- [Incident Postmortem Generation](#incident-postmortem-generation)

---

## Epic Documentation Hub

Create a comprehensive documentation page for an epic with all related information.

### Workflow

```
1. Fetch epic: getJiraIssue(epicKey)
2. Fetch all stories: searchJiraIssuesUsingJql("parent = {epicKey} ORDER BY created")
3. Fetch linked Confluence pages: getJiraIssueRemoteIssueLinks(epicKey)
4. Build page structure:
   - Epic overview (description, acceptance criteria)
   - Story breakdown table
   - Links to related documentation
   - Status summary
5. Create/update Confluence page
```

### Page Structure

```markdown
# {Epic Title}

## Overview
{Epic description}

## Acceptance Criteria
{From epic's acceptance criteria field}

## Stories

| Key | Summary | Status | Assignee | Points |
|-----|---------|--------|----------|--------|
| PROJ-101 | User login | Done | @alice | 3 |
| PROJ-102 | Password reset | In Progress | @bob | 2 |

## Progress
- Total Stories: 5
- Completed: 3 (60%)
- Story Points: 8/13 (62%)

## Related Documentation
- [Technical Design](link)
- [API Specification](link)

## Timeline
- Created: {date}
- Target: {fixVersion release date}
```

---

## Automated Status Dashboards

Create project status pages that pull live data from Jira.

### Weekly Status Report

```
1. Query recent activity:
   - Created this week: "created >= startOfWeek()"
   - Resolved this week: "resolved >= startOfWeek()"
   - In progress: "status = 'In Progress'"

2. Calculate velocity:
   - Points completed in last 3 sprints
   - Average cycle time

3. Identify blockers:
   - "status = Blocked" or "labels = blocked"

4. Generate page with metrics and charts description
```

### Team Capacity View

```markdown
# Team Status - Week of {date}

## Capacity
| Team Member | Assigned | In Progress | Blocked |
|-------------|----------|-------------|---------|
| Alice | 5 | 2 | 0 |
| Bob | 3 | 1 | 1 |

## Blockers Requiring Attention
- PROJ-150: Waiting on external API access
- PROJ-152: Dependency on Team B

## This Week's Focus
{Sprint goal or weekly objectives}
```

---

## Meeting Notes with Issue Links

Create meeting notes that automatically link to discussed issues.

### Workflow

```
1. User provides meeting notes with issue keys mentioned
2. Extract all issue keys using regex: [A-Z]+-\d+
3. Fetch each issue: getJiraIssue(key)
4. Create Confluence page with:
   - Meeting metadata (date, attendees)
   - Notes content
   - Issue summary table at bottom
5. Optionally add comment to each discussed issue linking to notes
```

### Template

```markdown
# {Meeting Title} - {date}

**Attendees:** {list}
**Type:** {standup/planning/retro/etc}

## Discussion

{User's notes with issue keys as links}

## Referenced Issues

| Key | Summary | Status | Owner |
|-----|---------|--------|-------|
{auto-populated from extracted keys}

## Action Items
- [ ] {action} - @owner - {due date}
```

---

## Technical Spec from Requirements

Generate technical specification from a requirements epic.

### Workflow

```
1. Get epic and all child stories
2. For each story, extract:
   - User story format (As a... I want... So that...)
   - Acceptance criteria
   - Technical notes from comments
3. Structure into spec document:
   - Requirements summary
   - Functional requirements (from stories)
   - Non-functional requirements (from labels/custom fields)
   - Technical approach (placeholder for team input)
```

### Output Structure

```markdown
# Technical Specification: {Epic Title}

## 1. Introduction
{Epic description}

## 2. Requirements Summary

### 2.1 Functional Requirements

#### FR-1: {Story PROJ-101 summary}
- **User Story:** As a {persona}, I want {goal} so that {benefit}
- **Acceptance Criteria:**
  - {criterion 1}
  - {criterion 2}
- **Priority:** {priority}

### 2.2 Non-Functional Requirements
{Extracted from labels: performance, security, scalability}

## 3. Technical Approach
{To be completed by engineering team}

## 4. Dependencies
{From issue links}

## 5. Timeline
{From fixVersion and sprint assignments}
```

---

## Incident Postmortem Generation

Create postmortem documentation from incident tickets.

### Trigger Conditions
- Issue type = "Incident" or "Bug" with label "production"
- Status changed to "Done" or "Resolved"

### Workflow

```
1. Get incident issue with full details
2. Get issue changelog for timeline
3. Get comments for investigation notes
4. Get linked issues (related incidents, fixes)
5. Generate postmortem page
```

### Postmortem Template

```markdown
# Incident Postmortem: {Issue Key} - {Summary}

## Incident Summary
- **Severity:** {priority}
- **Duration:** {time from status->In Progress to status->Done}
- **Impact:** {from custom field or description}
- **Services Affected:** {from components}

## Timeline
| Time | Event |
|------|-------|
| {timestamp} | Incident reported |
| {timestamp} | Investigation started |
| {timestamp} | Root cause identified |
| {timestamp} | Fix deployed |
| {timestamp} | Incident resolved |

## Root Cause
{From resolution field or specific comment}

## Resolution
{Description of fix applied}

## Action Items
{Generated from subtasks or linked improvement issues}

| Action | Owner | Due | Status |
|--------|-------|-----|--------|
| {action} | {assignee} | {date} | {status} |

## Lessons Learned
{From comments tagged with #lessons or retro notes}
```

---

## Tips for Complex Workflows

1. **Batch API calls** - When fetching multiple issues, use JQL with `key in (KEY-1, KEY-2, ...)` instead of individual calls

2. **Handle pagination** - Both Jira and Confluence APIs paginate. Check for `nextPageToken` or `cursor` in responses

3. **Cache cloudId** - Store the cloudId after first lookup to avoid repeated calls to `getAccessibleAtlassianResources`

4. **Use ADF for complex formatting** - When markdown isn't sufficient, use `contentFormat: "adf"` for Atlassian Document Format

5. **Preserve existing content** - When updating pages, fetch current content first to avoid overwriting sections you don't want to change
