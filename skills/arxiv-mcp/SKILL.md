---
name: arxiv
description: arXiv academic papers search
---

# arXiv Integration

arXiv academic papers search

## Configuration

No authentication required.

---

## API Reference

**Base URL:** `http://export.arxiv.org/api`

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/query` | Search papers |

## Examples

### 1. Search papers

```bash
curl -s \
  "http://export.arxiv.org/api/query?search_query=all:machine+learning&max_results=10"
```

---

## Author

arxiv

## Version

1.0.0
