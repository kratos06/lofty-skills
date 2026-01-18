# Zendesk Advanced Workflows

## Ticket Escalation Workflow

Escalate tickets based on priority and age:

```bash
# Find tickets needing escalation (open > 24 hours, not urgent)
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:ticket%20status:open%20priority:normal%20created<24hours" \
  | python3 -c "
import json, sys
data = json.load(sys.stdin)
for ticket in data.get('results', []):
    print(f\"Ticket #{ticket['id']}: {ticket['subject']} - Priority: {ticket['priority']}\")
"

# Escalate a ticket
curl -s -X PUT \
  -u "your-email@example.com/token:your-api-token" \
  -H "Content-Type: application/json" \
  -d '{
    "ticket": {
      "priority": "high",
      "tags": ["escalated"],
      "comment": {
        "body": "Ticket escalated due to SLA threshold",
        "public": false
      }
    }
  }' \
  "https://your-subdomain.zendesk.com/api/v2/tickets/{TICKET_ID}.json"
```

## SLA Monitoring

Monitor tickets approaching SLA breach:

```bash
# Get tickets updated more than 4 hours ago that are still open
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:ticket%20status:open%20updated<4hours" \
  | python3 -c "
import json, sys
from datetime import datetime
data = json.load(sys.stdin)
print('Tickets at SLA risk:')
for t in data.get('results', []):
    print(f\"  #{t['id']}: {t['subject'][:50]}... (Priority: {t['priority']})\")
"
```

## Customer History Report

Get complete ticket history for a customer:

```bash
# Step 1: Find user by email
USER_EMAIL="customer@example.com"
USER_DATA=$(curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:user%20email:${USER_EMAIL}")

# Step 2: Get all tickets for user
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:ticket%20requester:${USER_EMAIL}" \
  | python3 -c "
import json, sys
data = json.load(sys.stdin)
print(f\"Customer: ${USER_EMAIL}\")
print(f\"Total tickets: {data.get('count', 0)}\")
print('\\nTicket History:')
for t in data.get('results', []):
    print(f\"  #{t['id']} [{t['status']}] {t['subject'][:60]}\")
"
```

## Bulk Ticket Operations

### Close Multiple Solved Tickets

```bash
# Find solved tickets older than 7 days
TICKET_IDS=$(curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:ticket%20status:solved%20solved>7days" \
  | python3 -c "import json,sys; print(','.join(str(t['id']) for t in json.load(sys.stdin).get('results',[])))")

# Close them in bulk
curl -s -X PUT \
  -u "your-email@example.com/token:your-api-token" \
  -H "Content-Type: application/json" \
  -d "{\"tickets\": [{\"id\": \"${TICKET_IDS}\", \"status\": \"closed\"}]}" \
  "https://your-subdomain.zendesk.com/api/v2/tickets/update_many.json?ids=${TICKET_IDS}"
```

### Add Tag to Multiple Tickets

```bash
curl -s -X PUT \
  -u "your-email@example.com/token:your-api-token" \
  -H "Content-Type: application/json" \
  -d '{"ticket": {"additional_tags": ["reviewed"]}}' \
  "https://your-subdomain.zendesk.com/api/v2/tickets/update_many.json?ids=123,124,125"
```

## Ticket Analytics

### Ticket Volume by Status

```bash
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/tickets/count.json?status=open"

# Get counts for each status
for status in new open pending hold solved; do
  count=$(curl -s -u "your-email@example.com/token:your-api-token" \
    "https://your-subdomain.zendesk.com/api/v2/search/count.json?query=type:ticket%20status:${status}" \
    | python3 -c "import json,sys; print(json.load(sys.stdin).get('count',0))")
  echo "${status}: ${count}"
done
```

### Recent Ticket Summary

```bash
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:ticket%20created>7days" \
  | python3 -c "
import json, sys
from collections import Counter
data = json.load(sys.stdin)
tickets = data.get('results', [])
statuses = Counter(t['status'] for t in tickets)
priorities = Counter(t['priority'] for t in tickets)
print(f'Tickets created in last 7 days: {len(tickets)}')
print('\\nBy Status:')
for s, c in statuses.most_common():
    print(f'  {s}: {c}')
print('\\nBy Priority:')
for p, c in priorities.most_common():
    print(f'  {p}: {c}')
"
```

## Automation Helpers

### Auto-Response Template

```bash
# Add a templated response to a ticket
TICKET_ID=12345
RESPONSE="Thank you for contacting support. We've received your request and will respond within 24 hours.

In the meantime, please check our FAQ at https://support.example.com/faq

Best regards,
Support Team"

curl -s -X PUT \
  -u "your-email@example.com/token:your-api-token" \
  -H "Content-Type: application/json" \
  -d "{
    \"ticket\": {
      \"comment\": {
        \"body\": \"${RESPONSE}\",
        \"public\": true
      }
    }
  }" \
  "https://your-subdomain.zendesk.com/api/v2/tickets/${TICKET_ID}.json"
```

### Ticket Categorization by Keywords

```bash
# Find tickets mentioning specific keywords and tag them
KEYWORDS=("billing" "refund" "payment")
for keyword in "${KEYWORDS[@]}"; do
  curl -s -u "your-email@example.com/token:your-api-token" \
    "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:ticket%20status:new%20${keyword}" \
    | python3 -c "
import json, sys
data = json.load(sys.stdin)
for t in data.get('results', []):
    print(f\"Ticket #{t['id']} matches '${keyword}': {t['subject']}\")
"
done
```

## Views and Filters

### Get All Views

```bash
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/views.json" \
  | python3 -c "
import json, sys
data = json.load(sys.stdin)
for v in data.get('views', []):
    print(f\"{v['id']}: {v['title']}\")
"
```

### Get Tickets from a View

```bash
VIEW_ID=12345
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/views/${VIEW_ID}/tickets.json"
```

## Organization Management

### Get Organization Tickets

```bash
ORG_ID=12345
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/organizations/${ORG_ID}/tickets.json"
```

### Search by Organization

```bash
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/search.json?query=type:ticket%20organization:\"Acme%20Corp\""
```

## Macros

### List Available Macros

```bash
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/macros.json" \
  | python3 -c "
import json, sys
data = json.load(sys.stdin)
for m in data.get('macros', []):
    print(f\"{m['id']}: {m['title']}\")
"
```

### Apply Macro to Ticket

```bash
TICKET_ID=12345
MACRO_ID=67890
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/tickets/${TICKET_ID}/macros/${MACRO_ID}/apply.json"
```

## Attachments

### Get Ticket Attachments

```bash
TICKET_ID=12345
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/tickets/${TICKET_ID}/comments.json" \
  | python3 -c "
import json, sys
data = json.load(sys.stdin)
for comment in data.get('comments', []):
    for att in comment.get('attachments', []):
        print(f\"Attachment: {att['file_name']} ({att['size']} bytes)\")
        print(f\"  URL: {att['content_url']}\")
"
```

## Satisfaction Ratings

### Get Satisfaction Scores

```bash
curl -s -u "your-email@example.com/token:your-api-token" \
  "https://your-subdomain.zendesk.com/api/v2/satisfaction_ratings.json?score=good" \
  | python3 -c "
import json, sys
data = json.load(sys.stdin)
print(f\"Good ratings: {len(data.get('satisfaction_ratings', []))}\")
"
```
