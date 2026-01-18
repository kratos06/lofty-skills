---
name: replicate
description: Replicate AI model hosting
---

# Replicate Integration

Replicate AI model hosting

## Configuration

### Environment Variable

```bash
export REPLICATE_API_TOKEN="your-api-key"
```

### Get API Credentials

https://replicate.com/account/api-tokens

---

## API Reference

**Base URL:** `https://api.replicate.com/v1`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $REPLICATE_API_TOKEN" \
  "https://api.replicate.com/v1/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/predictions` | Run model |
| GET | `/predictions/{id}` | Get prediction |
| GET | `/models` | List models |

## Examples

### 1. Run model

```bash
curl -s -H "Authorization: Bearer $REPLICATE_API_TOKEN" -X POST -H "Content-Type: application/json" -d '{"version":"model_version_id","input":{"prompt":"Hello"}}' \
  "https://api.replicate.com/v1/predictions"
```

### 2. Get prediction

```bash
curl -s -H "Authorization: Bearer $REPLICATE_API_TOKEN" \
  "https://api.replicate.com/v1/predictions/{id}"
```

### 3. List models

```bash
curl -s -H "Authorization: Bearer $REPLICATE_API_TOKEN" \
  "https://api.replicate.com/v1/models"
```

---

## Author

replicate

## Version

1.0.0
