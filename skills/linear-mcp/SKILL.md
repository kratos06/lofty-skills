---
name: linear
description: Linear issue tracking with cycles, projects, and high-velocity workflows
---

# Linear Integration

Linear issue tracking with cycles, projects, and high-velocity workflows

## Configuration

### Environment Variable

```bash
export LINEAR_API_KEY="your-api-key"
```

### Get API Credentials

https://linear.app/settings/api → Personal API keys

---

## API Reference

**Base URL:** `https://api.linear.app/graphql`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $LINEAR_API_KEY" \
  "https://api.linear.app/graphql/endpoint"
```

## GraphQL Queries

**Endpoint:** `https://api.linear.app/graphql`

### List issues

```bash
curl -s -X POST \
  -H "Authorization: Bearer $LINEAR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"query": "{ issues { nodes { id title state { name } } } }"}' \
  "https://api.linear.app/graphql"
```

### Get issue

```bash
curl -s -X POST \
  -H "Authorization: Bearer $LINEAR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"query": "{ issue(id: \"xxx\") { id title description } }"}' \
  "https://api.linear.app/graphql"
```

### Create issue

```bash
curl -s -X POST \
  -H "Authorization: Bearer $LINEAR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"query": "mutation { issueCreate(input: { teamId: \"xxx\", title: \"Bug\" }) { issue { id } } }"}' \
  "https://api.linear.app/graphql"
```

### List projects

```bash
curl -s -X POST \
  -H "Authorization: Bearer $LINEAR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"query": "{ projects { nodes { id name } } }"}' \
  "https://api.linear.app/graphql"
```

---

## Author

Linear

## Version

1.0.0
