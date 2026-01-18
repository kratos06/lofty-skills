---
name: exa
description: Exa AI-powered search engine
---

# Exa Search Integration

Exa AI-powered search engine

## Configuration

### Environment Variable

```bash
export EXA_API_KEY="your-api-key"
```

### Get API Credentials

https://dashboard.exa.ai/api-keys

---

## API Reference

**Base URL:** `https://api.exa.ai`

**Authentication:** Bearer token in `x-api-key` header

```bash
curl -H "x-api-key: Bearer $EXA_API_KEY" \
  "https://api.exa.ai/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/search` | Search web |
| POST | `/findSimilar` | Find similar |
| POST | `/contents` | Get contents |

## Examples

### 1. Search web

```bash
curl -s -H "x-api-key: Bearer $EXA_API_KEY" -X POST -H "Content-Type: application/json" -d '{"query":"search term","numResults":10}' \
  "https://api.exa.ai/search"
```

### 2. Find similar

```bash
curl -s -H "x-api-key: Bearer $EXA_API_KEY" -X POST -H "Content-Type: application/json" -d '{"url":"https://example.com"}' \
  "https://api.exa.ai/findSimilar"
```

### 3. Get contents

```bash
curl -s -H "x-api-key: Bearer $EXA_API_KEY" -X POST -H "Content-Type: application/json" -d '{"ids":["id1","id2"]}' \
  "https://api.exa.ai/contents"
```

---

## Author

Exa

## Version

1.0.0
