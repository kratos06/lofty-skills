---
name: netlify
description: Netlify site deployment and functions
---

# Netlify Integration

Netlify site deployment and functions

## Configuration

### Environment Variable

```bash
export NETLIFY_AUTH_TOKEN="your-api-key"
```

### Get API Credentials

https://app.netlify.com/user/applications#personal-access-tokens

---

## API Reference

**Base URL:** `https://api.netlify.com/api/v1`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $NETLIFY_AUTH_TOKEN" \
  "https://api.netlify.com/api/v1/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/sites` | List sites |
| GET | `/sites/{site_id}/deploys` | List deploys |
| POST | `/sites/{site_id}/deploys` | Create deploy |
| GET | `/sites/{site_id}/forms` | List forms |

## Examples

### 1. List sites

```bash
curl -s -H "Authorization: Bearer $NETLIFY_AUTH_TOKEN" \
  "https://api.netlify.com/api/v1/sites"
```

### 2. List deploys

```bash
curl -s -H "Authorization: Bearer $NETLIFY_AUTH_TOKEN" \
  "https://api.netlify.com/api/v1/sites/{site_id}/deploys"
```

### 3. Create deploy

```bash
curl -s -H "Authorization: Bearer $NETLIFY_AUTH_TOKEN" -X POST -H "Content-Type: application/json" \
  "https://api.netlify.com/api/v1/sites/{site_id}/deploys"
```

### 4. List forms

```bash
curl -s -H "Authorization: Bearer $NETLIFY_AUTH_TOKEN" \
  "https://api.netlify.com/api/v1/sites/{site_id}/forms"
```

---

## Author

Netlify

## Version

1.0.0
