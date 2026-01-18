---
name: github
description: GitHub repository management, PRs, issues, and CI/CD workflows (Official)
---

# GitHub Integration

GitHub repository management, PRs, issues, and CI/CD workflows (Official)

## Configuration

### Environment Variable

```bash
export GITHUB_TOKEN="your-api-key"
```

### Get API Credentials

https://github.com/settings/tokens → Generate new token (classic)

---

## API Reference

**Base URL:** `https://api.github.com`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $GITHUB_TOKEN" \
  "https://api.github.com/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/repos/{owner}/{repo}` | Get repository info |
| GET | `/repos/{owner}/{repo}/issues` | List issues |
| POST | `/repos/{owner}/{repo}/issues` | Create issue |
| GET | `/repos/{owner}/{repo}/pulls` | List pull requests |
| POST | `/repos/{owner}/{repo}/pulls` | Create PR |
| GET | `/repos/{owner}/{repo}/contents/{path}` | Get file contents |
| GET | `/search/repositories` | Search repos |
| GET | `/user/repos` | List your repos |

## Examples

### 1. Get repository info

```bash
curl -s -H "Authorization: Bearer $GITHUB_TOKEN" -H "Accept: application/vnd.github+json" -H "X-GitHub-Api-Version: 2022-11-28" \
  "https://api.github.com/repos/{owner}/{repo}"
```

### 2. List issues

```bash
curl -s -H "Authorization: Bearer $GITHUB_TOKEN" -H "Accept: application/vnd.github+json" -H "X-GitHub-Api-Version: 2022-11-28" \
  "https://api.github.com/repos/{owner}/{repo}/issues?state=open"
```

### 3. Create issue

```bash
curl -s -H "Authorization: Bearer $GITHUB_TOKEN" -H "Accept: application/vnd.github+json" -H "X-GitHub-Api-Version: 2022-11-28" -X POST -H "Content-Type: application/json" -d '{"title":"Bug report","body":"Description"}' \
  "https://api.github.com/repos/{owner}/{repo}/issues"
```

### 4. List pull requests

```bash
curl -s -H "Authorization: Bearer $GITHUB_TOKEN" -H "Accept: application/vnd.github+json" -H "X-GitHub-Api-Version: 2022-11-28" \
  "https://api.github.com/repos/{owner}/{repo}/pulls"
```

### 5. Create PR

```bash
curl -s -H "Authorization: Bearer $GITHUB_TOKEN" -H "Accept: application/vnd.github+json" -H "X-GitHub-Api-Version: 2022-11-28" -X POST -H "Content-Type: application/json" -d '{"title":"Feature","head":"feature-branch","base":"main"}' \
  "https://api.github.com/repos/{owner}/{repo}/pulls"
```

### 6. Get file contents

```bash
curl -s -H "Authorization: Bearer $GITHUB_TOKEN" -H "Accept: application/vnd.github+json" -H "X-GitHub-Api-Version: 2022-11-28" \
  "https://api.github.com/repos/{owner}/{repo}/contents/{path}"
```

### 7. Search repos

```bash
curl -s -H "Authorization: Bearer $GITHUB_TOKEN" -H "Accept: application/vnd.github+json" -H "X-GitHub-Api-Version: 2022-11-28" \
  "https://api.github.com/search/repositories?q=keyword"
```

### 8. List your repos

```bash
curl -s -H "Authorization: Bearer $GITHUB_TOKEN" -H "Accept: application/vnd.github+json" -H "X-GitHub-Api-Version: 2022-11-28" \
  "https://api.github.com/user/repos"
```

## Common Workflows

### Create an issue

1. POST /repos/{owner}/{repo}/issues with title and body

### Create a pull request

1. Ensure branch exists
2. POST /repos/{owner}/{repo}/pulls

---

## Author

GitHub

## Version

1.5.0
