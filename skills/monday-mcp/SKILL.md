---
name: monday
description: Monday.com board management with items and team planning
---

# Monday.com Integration

Monday.com board management with items and team planning

## Configuration

### Environment Variable

```bash
export MONDAY_TOKEN="your-api-key"
```

### Get API Credentials

https://monday.com → Profile → Developers → My Access Tokens

---

## API Reference

**Base URL:** `https://api.monday.com/v2`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $MONDAY_TOKEN" \
  "https://api.monday.com/v2/endpoint"
```

## GraphQL Queries

**Endpoint:** `https://api.monday.com/v2`

### List boards

```bash
curl -s -X POST \
  -H "Authorization: Bearer $MONDAY_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"query": "{ boards { id name } }"}' \
  "https://api.monday.com/v2"
```

### Get board items

```bash
curl -s -X POST \
  -H "Authorization: Bearer $MONDAY_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"query": "{ boards(ids: [123]) { items_page { items { id name } } } }"}' \
  "https://api.monday.com/v2"
```

### Create item

```bash
curl -s -X POST \
  -H "Authorization: Bearer $MONDAY_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"query": "mutation { create_item(board_id: 123, item_name: \"Task\") { id } }"}' \
  "https://api.monday.com/v2"
```

---

## Author

Monday.com

## Version

1.0.0
