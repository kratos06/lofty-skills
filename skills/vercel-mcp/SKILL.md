---
name: vercel
description: Vercel deployment and project management
---

# Vercel Integration

Vercel deployment and project management

## Configuration

### Environment Variable

```bash
export VERCEL_TOKEN="your-api-key"
```

### Get API Credentials

https://vercel.com/account/tokens

---

## API Reference

**Base URL:** `https://api.vercel.com`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $VERCEL_TOKEN" \
  "https://api.vercel.com/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/v9/projects` | List projects |
| GET | `/v6/deployments` | List deployments |
| POST | `/v13/deployments` | Create deployment |
| GET | `/v2/deployments/{id}/events` | Get deployment logs |

## Examples

### 1. List projects

```bash
curl -s -H "Authorization: Bearer $VERCEL_TOKEN" \
  "https://api.vercel.com/v9/projects"
```

### 2. List deployments

```bash
curl -s -H "Authorization: Bearer $VERCEL_TOKEN" \
  "https://api.vercel.com/v6/deployments"
```

### 3. Create deployment

```bash
curl -s -H "Authorization: Bearer $VERCEL_TOKEN" -X POST -H "Content-Type: application/json" \
  "https://api.vercel.com/v13/deployments"
```

### 4. Get deployment logs

```bash
curl -s -H "Authorization: Bearer $VERCEL_TOKEN" \
  "https://api.vercel.com/v2/deployments/{id}/events"
```

---

## Author

Vercel

## Version

1.0.0
