---
name: pipedrive
description: Pipedrive sales pipeline management and deal tracking
---

# Pipedrive Integration

Pipedrive sales pipeline management and deal tracking

## Configuration

### Environment Variable

```bash
export PIPEDRIVE_TOKEN="your-api-key"
```

### Get API Credentials

Settings → Personal preferences → API

---

## API Reference

**Base URL:** `https://api.pipedrive.com/v1`

**Authentication:** API key in query parameters

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/deals` | List deals |
| POST | `/deals` | Create deal |
| GET | `/persons` | List persons |
| POST | `/persons` | Create person |
| GET | `/organizations` | List organizations |

## Examples

### 1. List deals

```bash
curl -s \
  "https://api.pipedrive.com/v1/deals?api_token=$PIPEDRIVE_TOKEN"
```

### 2. Create deal

```bash
curl -s -X POST -H "Content-Type: application/json" -d '{"title":"New Deal","value":1000}' \
  "https://api.pipedrive.com/v1/deals?api_token=$PIPEDRIVE_TOKEN"
```

### 3. List persons

```bash
curl -s \
  "https://api.pipedrive.com/v1/persons?api_token=$PIPEDRIVE_TOKEN"
```

### 4. Create person

```bash
curl -s -X POST -H "Content-Type: application/json" -d '{"name":"John Doe","email":"john@example.com"}' \
  "https://api.pipedrive.com/v1/persons?api_token=$PIPEDRIVE_TOKEN"
```

### 5. List organizations

```bash
curl -s \
  "https://api.pipedrive.com/v1/organizations?api_token=$PIPEDRIVE_TOKEN"
```

---

## Author

Pipedrive

## Version

1.0.0
