---
name: datadog
description: Datadog monitoring, logs, traces, and incident response (Official)
---

# Datadog Integration

Datadog monitoring, logs, traces, and incident response (Official)

## Configuration

### Environment Variables

Set these in your shell profile (`~/.zshrc` or `~/.bashrc`):

```bash
export DATADOG_API_KEY="your-datadog-api-key"
export DATADOG_APP_KEY="your-datadog-app-key"
```

### Get API Credentials

https://app.datadoghq.com/organization-settings/api-keys

---

## API Reference

**Base URL:** `https://api.datadoghq.com/api/v1`

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/query` | Query metrics |
| GET | `/monitor` | List monitors |
| POST | `/events` | Create event |
| GET | `/logs/events/search` | Search logs |

## Examples

### 1. Query metrics

```bash
curl -s \
  "https://api.datadoghq.com/api/v1/query?from=now-1h&to=now&query=avg:system.cpu.user{*}"
```

### 2. List monitors

```bash
curl -s \
  "https://api.datadoghq.com/api/v1/monitor"
```

### 3. Create event

```bash
curl -s -X POST -H "Content-Type: application/json" -d '{"title":"Event","text":"Details","priority":"normal"}' \
  "https://api.datadoghq.com/api/v1/events"
```

### 4. Search logs

```bash
curl -s \
  "https://api.datadoghq.com/api/v1/logs/events/search"
```

---

## Author

Datadog

## Version

1.0.0
