---
name: resend
description: Resend developer email API
---

# Resend Integration

Resend developer email API

## Configuration

### Environment Variable

```bash
export RESEND_API_KEY="your-api-key"
```

### Get API Credentials

https://resend.com/api-keys

---

## API Reference

**Base URL:** `https://api.resend.com`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $RESEND_API_KEY" \
  "https://api.resend.com/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/emails` | Send email |
| GET | `/emails/{email_id}` | Get email |
| GET | `/domains` | List domains |

## Examples

### 1. Send email

```bash
curl -s -H "Authorization: Bearer $RESEND_API_KEY" -X POST -H "Content-Type: application/json" -d '{"from":"you@example.com","to":["user@example.com"],"subject":"Hello","html":"<p>Body</p>"}' \
  "https://api.resend.com/emails"
```

### 2. Get email

```bash
curl -s -H "Authorization: Bearer $RESEND_API_KEY" \
  "https://api.resend.com/emails/{email_id}"
```

### 3. List domains

```bash
curl -s -H "Authorization: Bearer $RESEND_API_KEY" \
  "https://api.resend.com/domains"
```

---

## Author

resend

## Version

1.0.0
