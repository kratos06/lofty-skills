---
name: clickup
description: ClickUp project and task management
---

# ClickUp Integration

ClickUp project and task management

## Configuration

### Environment Variable

```bash
export CLICKUP_TOKEN="your-api-key"
```

### Get API Credentials

https://app.clickup.com/settings/apps → Generate API Token

---

## API Reference

**Base URL:** `https://api.clickup.com/api/v2`

**Authentication:** API key in `Authorization` header

```bash
curl -H "Authorization: $CLICKUP_TOKEN" \
  "https://api.clickup.com/api/v2/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/team` | Get workspaces |
| GET | `/team/{team_id}/space` | List spaces |
| GET | `/list/{list_id}/task` | List tasks |
| POST | `/list/{list_id}/task` | Create task |
| PUT | `/task/{task_id}` | Update task |

## Examples

### 1. Get workspaces

```bash
curl -s -H "Authorization: $CLICKUP_TOKEN" \
  "https://api.clickup.com/api/v2/team"
```

### 2. List spaces

```bash
curl -s -H "Authorization: $CLICKUP_TOKEN" \
  "https://api.clickup.com/api/v2/team/{team_id}/space"
```

### 3. List tasks

```bash
curl -s -H "Authorization: $CLICKUP_TOKEN" \
  "https://api.clickup.com/api/v2/list/{list_id}/task"
```

### 4. Create task

```bash
curl -s -H "Authorization: $CLICKUP_TOKEN" -X POST -H "Content-Type: application/json" -d '{"name":"Task","description":"Details"}' \
  "https://api.clickup.com/api/v2/list/{list_id}/task"
```

### 5. Update task

```bash
curl -s -H "Authorization: $CLICKUP_TOKEN" -X PUT -H "Content-Type: application/json" -d '{"status":"complete"}' \
  "https://api.clickup.com/api/v2/task/{task_id}"
```

---

## Author

clickup

## Version

1.0.0
