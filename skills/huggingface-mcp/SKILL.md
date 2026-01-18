---
name: huggingface
description: Hugging Face models, datasets, and inference API
---

# Hugging Face Integration

Hugging Face models, datasets, and inference API

## Configuration

### Environment Variable

```bash
export HUGGINGFACE_API_KEY="your-api-key"
```

### Get API Credentials

https://huggingface.co/settings/tokens

---

## API Reference

**Base URL:** `https://api-inference.huggingface.co/models`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $HUGGINGFACE_API_KEY" \
  "https://api-inference.huggingface.co/models/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/{model_id}` | Run inference |
| POST | `/sentence-transformers/all-MiniLM-L6-v2` | Create embeddings |

## Examples

### 1. Run inference

```bash
curl -s -H "Authorization: Bearer $HUGGINGFACE_API_KEY" -X POST -H "Content-Type: application/json" -d '{"inputs":"Hello, how are you?"}' \
  "https://api-inference.huggingface.co/models/{model_id}"
```

### 2. Create embeddings

```bash
curl -s -H "Authorization: Bearer $HUGGINGFACE_API_KEY" -X POST -H "Content-Type: application/json" -d '{"inputs":"text to embed"}' \
  "https://api-inference.huggingface.co/models/sentence-transformers/all-MiniLM-L6-v2"
```

---

## Author

Hugging Face

## Version

1.0.0
