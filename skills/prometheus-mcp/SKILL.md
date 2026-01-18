---
name: prometheus
description: Prometheus metrics and alerting
---

# Prometheus Integration

Prometheus metrics and alerting

## Configuration

No authentication required.

---

## API Reference

**Base URL:** `http://localhost:9090/api/v1`

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/query` | Instant query |
| GET | `/query_range` | Range query |
| GET | `/label/__name__/values` | List metrics |
| GET | `/alerts` | List alerts |

## Examples

### 1. Instant query

```bash
curl -s \
  "http://localhost:9090/api/v1/query?query=up"
```

### 2. Range query

```bash
curl -s \
  "http://localhost:9090/api/v1/query_range?query=up&start=2024-01-01T00:00:00Z&end=2024-01-02T00:00:00Z&step=15m"
```

### 3. List metrics

```bash
curl -s \
  "http://localhost:9090/api/v1/label/__name__/values"
```

### 4. List alerts

```bash
curl -s \
  "http://localhost:9090/api/v1/alerts"
```

---

## Author

prometheus

## Version

1.0.0
