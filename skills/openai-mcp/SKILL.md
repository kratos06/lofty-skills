---
name: openai
description: OpenAI API integration for GPT models and embeddings
---

# OpenAI Integration

OpenAI API integration for GPT models and embeddings

## Configuration

### Environment Variable

```bash
export OPENAI_API_KEY="your-api-key"
```

### Get API Credentials

https://platform.openai.com/api-keys

---

## API Reference

**Base URL:** `https://api.openai.com/v1`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $OPENAI_API_KEY" \
  "https://api.openai.com/v1/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/chat/completions` | Chat completion |
| POST | `/embeddings` | Create embeddings |
| POST | `/images/generations` | Generate image |
| GET | `/models` | List models |

## Examples

### 1. Chat completion

```bash
curl -s -H "Authorization: Bearer $OPENAI_API_KEY" -X POST -H "Content-Type: application/json" -d '{"model":"gpt-4","messages":[{"role":"user","content":"Hello"}]}' \
  "https://api.openai.com/v1/chat/completions"
```

### 2. Create embeddings

```bash
curl -s -H "Authorization: Bearer $OPENAI_API_KEY" -X POST -H "Content-Type: application/json" -d '{"model":"text-embedding-3-small","input":"text to embed"}' \
  "https://api.openai.com/v1/embeddings"
```

### 3. Generate image

```bash
curl -s -H "Authorization: Bearer $OPENAI_API_KEY" -X POST -H "Content-Type: application/json" -d '{"model":"dall-e-3","prompt":"a cat","n":1}' \
  "https://api.openai.com/v1/images/generations"
```

### 4. List models

```bash
curl -s -H "Authorization: Bearer $OPENAI_API_KEY" \
  "https://api.openai.com/v1/models"
```

---

## Author

OpenAI

## Version

1.0.0
