---
name: notion
description: Notion workspace integration with semantic search and page management
---

# Notion Integration

Notion workspace integration with semantic search and page management

## Configuration

### Environment Variable

```bash
export NOTION_TOKEN="your-api-key"
```

### Get API Credentials

https://www.notion.so/my-integrations → Create integration → Copy Internal Integration Token

---

## API Reference

**Base URL:** `https://api.notion.com/v1`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $NOTION_TOKEN" \
  "https://api.notion.com/v1/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/search` | Search pages/databases |
| GET | `/pages/{page_id}` | Get page |
| POST | `/pages` | Create page |
| PATCH | `/pages/{page_id}` | Update page |
| POST | `/databases/{database_id}/query` | Query database |
| GET | `/blocks/{block_id}/children` | Get page content |

## Examples

### 1. Search pages/databases

```bash
curl -s -H "Authorization: Bearer $NOTION_TOKEN" -H "Notion-Version: 2022-06-28" -X POST -H "Content-Type: application/json" -d '{"query":"keyword"}' \
  "https://api.notion.com/v1/search"
```

### 2. Get page

```bash
curl -s -H "Authorization: Bearer $NOTION_TOKEN" -H "Notion-Version: 2022-06-28" \
  "https://api.notion.com/v1/pages/{page_id}"
```

### 3. Create page

```bash
curl -s -H "Authorization: Bearer $NOTION_TOKEN" -H "Notion-Version: 2022-06-28" -X POST -H "Content-Type: application/json" -d '{"parent":{"database_id":"xxx"},"properties":{}}' \
  "https://api.notion.com/v1/pages"
```

### 4. Update page

```bash
curl -s -H "Authorization: Bearer $NOTION_TOKEN" -H "Notion-Version: 2022-06-28" -X PATCH -H "Content-Type: application/json" -d '{"properties":{}}' \
  "https://api.notion.com/v1/pages/{page_id}"
```

### 5. Query database

```bash
curl -s -H "Authorization: Bearer $NOTION_TOKEN" -H "Notion-Version: 2022-06-28" -X POST -H "Content-Type: application/json" -d '{"filter":{}}' \
  "https://api.notion.com/v1/databases/{database_id}/query"
```

### 6. Get page content

```bash
curl -s -H "Authorization: Bearer $NOTION_TOKEN" -H "Notion-Version: 2022-06-28" \
  "https://api.notion.com/v1/blocks/{block_id}/children"
```

---

## Author

Notion

## Version

1.0.0
