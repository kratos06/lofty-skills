---
name: brave-search
description: Brave Search API integration
---

# Brave Search Integration

Brave Search API integration

## Configuration

### Environment Variable

```bash
export BRAVE_API_KEY="your-api-key"
```

### Get API Credentials

https://api.search.brave.com/app/keys

---

## API Reference

**Base URL:** `https://api.search.brave.com/res/v1`

**Authentication:** API key in `X-Subscription-Token` header

```bash
curl -H "X-Subscription-Token: $BRAVE_API_KEY" \
  "https://api.search.brave.com/res/v1/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/web/search` | Web search |
| GET | `/news/search` | News search |
| GET | `/images/search` | Image search |

## Examples

### 1. Web search

```bash
curl -s -H "X-Subscription-Token: $BRAVE_API_KEY" \
  "https://api.search.brave.com/res/v1/web/search?q=search+term"
```

### 2. News search

```bash
curl -s -H "X-Subscription-Token: $BRAVE_API_KEY" \
  "https://api.search.brave.com/res/v1/news/search?q=search+term"
```

### 3. Image search

```bash
curl -s -H "X-Subscription-Token: $BRAVE_API_KEY" \
  "https://api.search.brave.com/res/v1/images/search?q=search+term"
```

---

## Author

Brave

## Version

1.0.0
