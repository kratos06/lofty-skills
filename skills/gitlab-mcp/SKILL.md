---
name: gitlab
description: GitLab projects, merge requests, and CI/CD
---

# GitLab Integration

GitLab projects, merge requests, and CI/CD

## Configuration

### Environment Variable

```bash
export GITLAB_TOKEN="your-api-key"
```

### Get API Credentials

https://gitlab.com/-/profile/personal_access_tokens

---

## API Reference

**Base URL:** `https://gitlab.com/api/v4`

**Authentication:** API key in `PRIVATE-TOKEN` header

```bash
curl -H "PRIVATE-TOKEN: $GITLAB_TOKEN" \
  "https://gitlab.com/api/v4/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/projects` | List projects |
| GET | `/projects/{id}` | Get project |
| GET | `/projects/{id}/issues` | List issues |
| POST | `/projects/{id}/issues` | Create issue |
| GET | `/projects/{id}/merge_requests` | List MRs |
| POST | `/projects/{id}/merge_requests` | Create MR |

## Examples

### 1. List projects

```bash
curl -s -H "PRIVATE-TOKEN: $GITLAB_TOKEN" \
  "https://gitlab.com/api/v4/projects?membership=true"
```

### 2. Get project

```bash
curl -s -H "PRIVATE-TOKEN: $GITLAB_TOKEN" \
  "https://gitlab.com/api/v4/projects/{id}"
```

### 3. List issues

```bash
curl -s -H "PRIVATE-TOKEN: $GITLAB_TOKEN" \
  "https://gitlab.com/api/v4/projects/{id}/issues"
```

### 4. Create issue

```bash
curl -s -H "PRIVATE-TOKEN: $GITLAB_TOKEN" -X POST -H "Content-Type: application/json" -d '{"title":"Bug","description":"Details"}' \
  "https://gitlab.com/api/v4/projects/{id}/issues"
```

### 5. List MRs

```bash
curl -s -H "PRIVATE-TOKEN: $GITLAB_TOKEN" \
  "https://gitlab.com/api/v4/projects/{id}/merge_requests"
```

### 6. Create MR

```bash
curl -s -H "PRIVATE-TOKEN: $GITLAB_TOKEN" -X POST -H "Content-Type: application/json" -d '{"source_branch":"feature","target_branch":"main","title":"Feature"}' \
  "https://gitlab.com/api/v4/projects/{id}/merge_requests"
```

---

## Author

gitlab

## Version

1.0.0
