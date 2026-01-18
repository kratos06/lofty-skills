---
name: trello
description: Trello boards, lists, and cards management
---

# Trello Integration

Trello boards, lists, and cards management

## Configuration

### Environment Variables

Set these in your shell profile (`~/.zshrc` or `~/.bashrc`):

```bash
export TRELLO_API_KEY="your-trello-api-key"
export TRELLO_TOKEN="your-trello-token"
```

### Get API Credentials

https://trello.com/app-key

---

## API Reference

**Base URL:** `https://api.trello.com/1`

**Authentication:** API key in query parameters

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/members/me/boards` | List boards |
| GET | `/boards/{id}/lists` | Get lists on board |
| GET | `/lists/{id}/cards` | Get cards in list |
| POST | `/cards` | Create card |
| PUT | `/cards/{id}` | Update card |

## Examples

### 1. List boards

```bash
curl -s \
  "https://api.trello.com/1/members/me/boards?key=$TRELLO_API_KEY&token=$TRELLO_TOKEN"
```

### 2. Get lists on board

```bash
curl -s \
  "https://api.trello.com/1/boards/{id}/lists?key=$TRELLO_API_KEY&token=$TRELLO_TOKEN"
```

### 3. Get cards in list

```bash
curl -s \
  "https://api.trello.com/1/lists/{id}/cards?key=$TRELLO_API_KEY&token=$TRELLO_TOKEN"
```

### 4. Create card

```bash
curl -s -X POST -H "Content-Type: application/json" \
  "https://api.trello.com/1/cards?idList={list_id}&name=Task&key=$TRELLO_API_KEY&token=$TRELLO_TOKEN"
```

### 5. Update card

```bash
curl -s -X PUT -H "Content-Type: application/json" \
  "https://api.trello.com/1/cards/{id}?idList={new_list_id}&key=$TRELLO_API_KEY&token=$TRELLO_TOKEN"
```

---

## Author

atlassian

## Version

1.0.0
