---
name: sentry
description: Sentry error tracking and performance monitoring
---

# Sentry Integration

Sentry error tracking and performance monitoring

## Configuration

### Environment Variable

```bash
export SENTRY_AUTH_TOKEN="your-api-key"
```

### Get API Credentials

https://sentry.io/settings/account/api/auth-tokens/

---

## API Reference

**Base URL:** `https://sentry.io/api/0`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $SENTRY_AUTH_TOKEN" \
  "https://sentry.io/api/0/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/organizations/{org}/issues/` | List issues |
| GET | `/issues/{issue_id}/` | Get issue |
| PUT | `/issues/{issue_id}/` | Update issue |
| GET | `/projects/{org}/{project}/events/` | List events |

## Examples

### 1. List issues

```bash
curl -s -H "Authorization: Bearer $SENTRY_AUTH_TOKEN" \
  "https://sentry.io/api/0/organizations/{org}/issues/"
```

### 2. Get issue

```bash
curl -s -H "Authorization: Bearer $SENTRY_AUTH_TOKEN" \
  "https://sentry.io/api/0/issues/{issue_id}/"
```

### 3. Update issue

```bash
curl -s -H "Authorization: Bearer $SENTRY_AUTH_TOKEN" -X PUT -H "Content-Type: application/json" -d '{"status":"resolved"}' \
  "https://sentry.io/api/0/issues/{issue_id}/"
```

### 4. List events

```bash
curl -s -H "Authorization: Bearer $SENTRY_AUTH_TOKEN" \
  "https://sentry.io/api/0/projects/{org}/{project}/events/"
```

---

## Author

Sentry

## Version

1.0.0
