---
name: translate
description: Translation services integration
---

# DeepL Translate Integration

Translation services integration

## Configuration

### Environment Variable

```bash
export DEEPL_API_KEY="your-api-key"
```

### Get API Credentials

https://www.deepl.com/pro-api

---

## API Reference

**Base URL:** `https://api-free.deepl.com/v2`

**Authentication:** API key in `Authorization` header

```bash
curl -H "Authorization: $DEEPL_API_KEY" \
  "https://api-free.deepl.com/v2/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/translate` | Translate text |
| GET | `/languages` | List languages |
| GET | `/usage` | Check usage |

## Examples

### 1. Translate text

```bash
curl -s -H "Authorization: $DEEPL_API_KEY" -X POST -H "Content-Type: application/json" -d '{"text":["Hello"],"target_lang":"DE"}' \
  "https://api-free.deepl.com/v2/translate"
```

### 2. List languages

```bash
curl -s -H "Authorization: $DEEPL_API_KEY" \
  "https://api-free.deepl.com/v2/languages"
```

### 3. Check usage

```bash
curl -s -H "Authorization: $DEEPL_API_KEY" \
  "https://api-free.deepl.com/v2/usage"
```

---

## Author

community

## Version

1.0.0
