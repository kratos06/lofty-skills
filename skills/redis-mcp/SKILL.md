---
name: redis
description: Redis key-value store with vector search capabilities (Official)
---

# Redis Integration

Redis key-value store with vector search capabilities (Official)

## Configuration

## Database Commands

### Connection String

```bash
export REDIS_URL="redis://localhost:6379"
```

### Get value

```bash
redis-cli -u "$REDIS_URL" GET key
```

### Set value

```bash
redis-cli -u "$REDIS_URL" SET key "value"
```

### List keys

```bash
redis-cli -u "$REDIS_URL" KEYS "*"
```

### Get hash

```bash
redis-cli -u "$REDIS_URL" HGETALL hash_key
```

### Delete key

```bash
redis-cli -u "$REDIS_URL" DEL key
```

---

## Author

Redis

## Version

1.0.0
