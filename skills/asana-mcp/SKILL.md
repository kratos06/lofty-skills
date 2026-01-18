---
name: asana
description: Asana task management with project tracking and team collaboration
---

# Asana Integration

Asana task management with project tracking and team collaboration

## Configuration

### Environment Variable

```bash
export ASANA_TOKEN="your-api-key"
```

### Get API Credentials

https://app.asana.com/0/developer-console → Personal access tokens

---

## API Reference

**Base URL:** `https://app.asana.com/api/1.0`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $ASANA_TOKEN" \
  "https://app.asana.com/api/1.0/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/workspaces` | List workspaces |
| GET | `/projects` | List projects |
| GET | `/tasks` | List tasks |
| POST | `/tasks` | Create task |
| PUT | `/tasks/{task_gid}` | Update task |

## Examples

### 1. List workspaces

```bash
curl -s -H "Authorization: Bearer $ASANA_TOKEN" \
  "https://app.asana.com/api/1.0/workspaces"
```

### 2. List projects

```bash
curl -s -H "Authorization: Bearer $ASANA_TOKEN" \
  "https://app.asana.com/api/1.0/projects?workspace={workspace_gid}"
```

### 3. List tasks

```bash
curl -s -H "Authorization: Bearer $ASANA_TOKEN" \
  "https://app.asana.com/api/1.0/tasks?project={project_gid}"
```

### 4. Create task

```bash
curl -s -H "Authorization: Bearer $ASANA_TOKEN" -X POST -H "Content-Type: application/json" -d '{"data":{"name":"Task","projects":["xxx"]}}' \
  "https://app.asana.com/api/1.0/tasks"
```

### 5. Update task

```bash
curl -s -H "Authorization: Bearer $ASANA_TOKEN" -X PUT -H "Content-Type: application/json" -d '{"data":{"completed":true}}' \
  "https://app.asana.com/api/1.0/tasks/{task_gid}"
```

---

## Author

Asana

## Version

1.0.0
