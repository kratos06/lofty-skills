---
name: firecrawl
description: Firecrawl web scraping and search capabilities (Official)
---

# Firecrawl Integration

Firecrawl web scraping and search capabilities (Official)

## Configuration

### Environment Variable

```bash
export FIRECRAWL_API_KEY="your-api-key"
```

### Get API Credentials

https://firecrawl.dev/app/api-keys

---

## API Reference

**Base URL:** `https://api.firecrawl.dev/v0`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $FIRECRAWL_API_KEY" \
  "https://api.firecrawl.dev/v0/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/scrape` | Scrape URL |
| POST | `/crawl` | Crawl website |
| GET | `/crawl/{id}` | Get crawl status |

## Examples

### 1. Scrape URL

```bash
curl -s -H "Authorization: Bearer $FIRECRAWL_API_KEY" -X POST -H "Content-Type: application/json" -d '{"url":"https://example.com"}' \
  "https://api.firecrawl.dev/v0/scrape"
```

### 2. Crawl website

```bash
curl -s -H "Authorization: Bearer $FIRECRAWL_API_KEY" -X POST -H "Content-Type: application/json" -d '{"url":"https://example.com","limit":10}' \
  "https://api.firecrawl.dev/v0/crawl"
```

### 3. Get crawl status

```bash
curl -s -H "Authorization: Bearer $FIRECRAWL_API_KEY" \
  "https://api.firecrawl.dev/v0/crawl/{id}"
```

---

## Author

Firecrawl

## Version

1.0.0
