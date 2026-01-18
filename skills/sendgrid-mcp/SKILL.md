---
name: sendgrid
description: SendGrid email marketing and delivery
---

# SendGrid Integration

SendGrid email marketing and delivery

## Configuration

### Environment Variable

```bash
export SENDGRID_API_KEY="your-api-key"
```

### Get API Credentials

https://app.sendgrid.com/settings/api_keys

---

## API Reference

**Base URL:** `https://api.sendgrid.com/v3`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $SENDGRID_API_KEY" \
  "https://api.sendgrid.com/v3/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/mail/send` | Send email |
| GET | `/templates` | List templates |
| GET | `/stats` | Get stats |

## Examples

### 1. Send email

```bash
curl -s -H "Authorization: Bearer $SENDGRID_API_KEY" -X POST -H "Content-Type: application/json" -d '{"personalizations":[{"to":[{"email":"to@example.com"}]}],"from":{"email":"from@example.com"},"subject":"Hello","content":[{"type":"text/plain","value":"Body"}]}' \
  "https://api.sendgrid.com/v3/mail/send"
```

### 2. List templates

```bash
curl -s -H "Authorization: Bearer $SENDGRID_API_KEY" \
  "https://api.sendgrid.com/v3/templates"
```

### 3. Get stats

```bash
curl -s -H "Authorization: Bearer $SENDGRID_API_KEY" \
  "https://api.sendgrid.com/v3/stats?start_date=2024-01-01"
```

---

## Author

sendgrid

## Version

1.0.0
