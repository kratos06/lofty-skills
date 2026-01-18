---
name: slack
description: Slack messaging with channel management and bot capabilities
---

# Slack Integration

Slack messaging with channel management and bot capabilities

## Configuration

### Environment Variable

```bash
export SLACK_TOKEN="your-api-key"
```

### Get API Credentials

https://api.slack.com/apps → OAuth & Permissions → Bot Token

---

## API Reference

**Base URL:** `https://slack.com/api`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $SLACK_TOKEN" \
  "https://slack.com/api/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/conversations.list` | List channels |
| POST | `/chat.postMessage` | Send message |
| GET | `/conversations.history` | Get messages |
| POST | `/conversations.create` | Create channel |
| GET | `/users.list` | List users |
| POST | `/files.upload` | Upload file |

## Examples

### 1. List channels

```bash
curl -s -H "Authorization: Bearer $SLACK_TOKEN" \
  "https://slack.com/api/conversations.list?types=public_channel,private_channel"
```

### 2. Send message

```bash
curl -s -H "Authorization: Bearer $SLACK_TOKEN" -X POST -H "Content-Type: application/json" -d '{"channel":"C123","text":"Hello"}' \
  "https://slack.com/api/chat.postMessage"
```

### 3. Get messages

```bash
curl -s -H "Authorization: Bearer $SLACK_TOKEN" \
  "https://slack.com/api/conversations.history?channel=C123&limit=100"
```

### 4. Create channel

```bash
curl -s -H "Authorization: Bearer $SLACK_TOKEN" -X POST -H "Content-Type: application/json" -d '{"name":"new-channel"}' \
  "https://slack.com/api/conversations.create"
```

### 5. List users

```bash
curl -s -H "Authorization: Bearer $SLACK_TOKEN" \
  "https://slack.com/api/users.list"
```

### 6. Upload file

```bash
curl -s -H "Authorization: Bearer $SLACK_TOKEN" -X POST -H "Content-Type: application/json" -d '{"channels":"C123","content":"file content"}' \
  "https://slack.com/api/files.upload"
```

## Common Workflows

### Send a message to a channel

1. Get channel ID via conversations.list
2. Post message via chat.postMessage

### Get recent messages

1. Get channel ID
2. Call conversations.history with channel ID

---

## Author

Slack

## Version

1.2.0
