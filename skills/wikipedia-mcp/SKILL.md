---
name: wikipedia
description: Wikipedia knowledge base access
---

# Wikipedia Integration

Wikipedia knowledge base access

## Configuration

No authentication required.

---

## API Reference

**Base URL:** `https://en.wikipedia.org/api/rest_v1`

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/page/summary/{title}` | Get page summary |
| GET | `/page/html/{title}` | Get page HTML |

## Examples

### 1. Get page summary

```bash
curl -s \
  "https://en.wikipedia.org/api/rest_v1/page/summary/{title}"
```

### 2. Get page HTML

```bash
curl -s \
  "https://en.wikipedia.org/api/rest_v1/page/html/{title}"
```

---

## Author

wikipedia

## Version

1.0.0
