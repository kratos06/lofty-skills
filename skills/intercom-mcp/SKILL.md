---
name: intercom
description: Intercom customer conversations and messaging platform
---

# Intercom Integration

Intercom customer conversations and messaging platform

## Configuration

### Environment Variable

```bash
export INTERCOM_TOKEN="your-api-key"
```

### Get API Credentials

https://app.intercom.com → Settings → Developers → Developer Hub

---

## API Reference

**Base URL:** `https://api.intercom.io`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $INTERCOM_TOKEN" \
  "https://api.intercom.io/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/conversations` | List conversations |
| GET | `/conversations/{id}` | Get conversation |
| POST | `/conversations/{id}/reply` | Reply to conversation |
| GET | `/contacts` | List contacts |
| POST | `/contacts` | Create contact |

## Examples

### 1. List conversations

```bash
curl -s -H "Authorization: Bearer $INTERCOM_TOKEN" \
  "https://api.intercom.io/conversations"
```

### 2. Get conversation

```bash
curl -s -H "Authorization: Bearer $INTERCOM_TOKEN" \
  "https://api.intercom.io/conversations/{id}"
```

### 3. Reply to conversation

```bash
curl -s -H "Authorization: Bearer $INTERCOM_TOKEN" -X POST -H "Content-Type: application/json" -d '{"message_type":"comment","type":"admin","admin_id":"xxx","body":"Reply text"}' \
  "https://api.intercom.io/conversations/{id}/reply"
```

### 4. List contacts

```bash
curl -s -H "Authorization: Bearer $INTERCOM_TOKEN" \
  "https://api.intercom.io/contacts"
```

### 5. Create contact

```bash
curl -s -H "Authorization: Bearer $INTERCOM_TOKEN" -X POST -H "Content-Type: application/json" -d '{"role":"user","email":"test@example.com"}' \
  "https://api.intercom.io/contacts"
```

---

## Author

Intercom

## Version

1.0.0
