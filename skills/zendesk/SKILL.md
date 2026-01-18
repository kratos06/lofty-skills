---
name: zendesk
description: Access Zendesk Support API for ticket management, user lookup, and customer support workflows. Use when querying tickets, creating/updating support tickets, searching customers, viewing ticket history, or managing support operations. Triggers on requests involving Zendesk tickets, support cases, customer issues, or helpdesk operations.
---

# Zendesk Support API Integration

Access Zendesk Support for ticket management, user lookup, and customer support workflows.

## Configuration

```
ZENDESK_SUBDOMAIN=your-subdomain
ZENDESK_EMAIL=your-email@example.com
ZENDESK_API_TOKEN=your-api-token
```

**Base URL:** `https://your-subdomain.zendesk.com/api/v2`

**Authentication:** Basic Auth with `{email}/token:{api_token}`

## Quick Reference

| Task | Endpoint | Method |
|------|----------|--------|
| List tickets | `/tickets.json` | GET |
| Get ticket | `/tickets/{id}.json` | GET |
| Create ticket | `/tickets.json` | POST |
| Update ticket | `/tickets/{id}.json` | PUT |
| Search | `/search.json?query={query}` | GET |
| List users | `/users.json` | GET |
| Get user | `/users/{id}.json` | GET |

## API Access via Bash

Use curl with Basic Auth for all API calls:

```bash
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/{endpoint}"
```

## Core Workflows

### 1. List Recent Tickets

```bash
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/tickets.json?sort_by=created_at&sort_order=desc" | python3 -m json.tool
```

### 2. Get Specific Ticket

```bash
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/tickets/{TICKET_ID}.json" | python3 -m json.tool
```

### 3. Search Tickets

Search by various criteria:

```bash
# Search by status
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:ticket%20status:open" | python3 -m json.tool

# Search by requester email
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:ticket%20requester:user@example.com" | python3 -m json.tool

# Search by keyword
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:ticket%20login%20issue" | python3 -m json.tool
```

### 4. Create Ticket

```bash
curl -s -X POST \
  -u "your-email@example.com/token:your-api-token" \
  -H "Content-Type: application/json" \
  -d '{
    "ticket": {
      "subject": "Ticket Subject",
      "comment": {
        "body": "Ticket description here"
      },
      "priority": "normal",
      "requester": {
        "email": "customer@example.com",
        "name": "Customer Name"
      }
    }
  }' \
  "https://your-subdomain.zendesk.com/api/v2/tickets.json" | python3 -m json.tool
```

### 5. Update Ticket

```bash
curl -s -X PUT \
  -u "your-email@example.com/token:your-api-token" \
  -H "Content-Type: application/json" \
  -d '{
    "ticket": {
      "status": "solved",
      "comment": {
        "body": "Issue has been resolved.",
        "public": true
      }
    }
  }' \
  "https://your-subdomain.zendesk.com/api/v2/tickets/{TICKET_ID}.json" | python3 -m json.tool
```

### 6. Add Comment to Ticket

```bash
curl -s -X PUT \
  -u "your-email@example.com/token:your-api-token" \
  -H "Content-Type: application/json" \
  -d '{
    "ticket": {
      "comment": {
        "body": "Internal note or public reply",
        "public": false
      }
    }
  }' \
  "https://your-subdomain.zendesk.com/api/v2/tickets/{TICKET_ID}.json" | python3 -m json.tool
```

### 7. Get Ticket Comments/History

```bash
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/tickets/{TICKET_ID}/comments.json" | python3 -m json.tool
```

### 8. Lookup User

```bash
# By ID
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/users/{USER_ID}.json" | python3 -m json.tool

# Search by email
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:user%20email:user@example.com" | python3 -m json.tool
```

## Search Query Syntax

Zendesk search supports powerful query syntax:

| Query | Description |
|-------|-------------|
| `type:ticket` | Search only tickets |
| `type:user` | Search only users |
| `status:open` | Tickets with open status |
| `status:pending` | Tickets with pending status |
| `status:solved` | Tickets with solved status |
| `priority:urgent` | Urgent priority tickets |
| `assignee:none` | Unassigned tickets |
| `created>2024-01-01` | Created after date |
| `updated<24hours` | Updated in last 24 hours |
| `requester:email@example.com` | By requester email |
| `tags:billing` | Tickets with specific tag |

Combine queries: `type:ticket status:open priority:high`

## Ticket Statuses

| Status | Description |
|--------|-------------|
| `new` | Newly created, not yet opened |
| `open` | Assigned and being worked on |
| `pending` | Waiting for customer response |
| `hold` | On hold, waiting internally |
| `solved` | Issue resolved |
| `closed` | Ticket closed (final state) |

## Ticket Priorities

| Priority | Description |
|----------|-------------|
| `low` | Low priority |
| `normal` | Default priority |
| `high` | High priority |
| `urgent` | Urgent, immediate attention |

## Pagination

API responses are paginated. Check for `next_page` in response:

```json
{
  "tickets": [...],
  "next_page": "https://your-subdomain.zendesk.com/api/v2/tickets.json?page=2",
  "previous_page": null,
  "count": 100
}
```

Use `per_page` parameter (max 100): `?per_page=100`

## Rate Limits

- Standard: 400 requests per minute
- Search: 1 request per second
- Monitor `X-RateLimit-Remaining` header

## Common Use Cases

### Get All Open Tickets for a User

```bash
USER_EMAIL="customer@example.com"
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:ticket%20requester:${USER_EMAIL}%20status:open"
```

### Get Recent Activity

```bash
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:ticket%20updated>1hour"
```

### Bulk Update Tickets

```bash
curl -s -X PUT \
  -u "your-email@example.com/token:your-api-token" \
  -H "Content-Type: application/json" \
  -d '{
    "tickets": [
      {"id": 123, "status": "solved"},
      {"id": 124, "status": "solved"}
    ]
  }' \
  "https://your-subdomain.zendesk.com/api/v2/tickets/update_many.json"
```

## Error Handling

| Code | Meaning |
|------|---------|
| 401 | Invalid credentials |
| 403 | Insufficient permissions |
| 404 | Resource not found |
| 422 | Validation error (check request body) |
| 429 | Rate limit exceeded |

## Advanced Workflows

For complex operations, see [references/advanced-workflows.md](references/advanced-workflows.md):
- Ticket escalation workflows
- Automated ticket categorization
- SLA monitoring
- Customer history reports
- Bulk operations
