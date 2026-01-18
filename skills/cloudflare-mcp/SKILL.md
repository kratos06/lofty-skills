---
name: cloudflare
description: Cloudflare Workers, KV, R2, and D1 management
---

# Cloudflare Integration

Cloudflare Workers, KV, R2, and D1 management

## Configuration

### Environment Variable

```bash
export CLOUDFLARE_API_TOKEN="your-api-key"
```

### Get API Credentials

https://dash.cloudflare.com/profile/api-tokens

---

## API Reference

**Base URL:** `https://api.cloudflare.com/client/v4`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
  "https://api.cloudflare.com/client/v4/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/zones` | List zones/domains |
| GET | `/zones/{zone_id}/dns_records` | List DNS records |
| POST | `/zones/{zone_id}/dns_records` | Create DNS record |
| GET | `/accounts/{account_id}/workers/scripts` | List Workers |
| PUT | `/accounts/{account_id}/workers/scripts/{script_name}` | Deploy Worker |

## Examples

### 1. List zones/domains

```bash
curl -s -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
  "https://api.cloudflare.com/client/v4/zones"
```

### 2. List DNS records

```bash
curl -s -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
  "https://api.cloudflare.com/client/v4/zones/{zone_id}/dns_records"
```

### 3. Create DNS record

```bash
curl -s -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" -X POST -H "Content-Type: application/json" -d '{"type":"A","name":"www","content":"1.2.3.4"}' \
  "https://api.cloudflare.com/client/v4/zones/{zone_id}/dns_records"
```

### 4. List Workers

```bash
curl -s -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
  "https://api.cloudflare.com/client/v4/accounts/{account_id}/workers/scripts"
```

### 5. Deploy Worker

```bash
curl -s -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" -X PUT -H "Content-Type: application/json" \
  "https://api.cloudflare.com/client/v4/accounts/{account_id}/workers/scripts/{script_name}"
```

---

## Author

Cloudflare

## Version

1.0.0
