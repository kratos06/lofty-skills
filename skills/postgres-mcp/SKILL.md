---
name: postgres
description: PostgreSQL database with schema inspection and read-only queries (Official Anthropic)
---

# PostgreSQL Integration

PostgreSQL database with schema inspection and read-only queries (Official Anthropic)

## Configuration

## Database Commands

### Connection String

```bash
export DATABASE_URL="postgresql://user:password@localhost:5432/database"
```

### Query data

```bash
psql "$DATABASE_URL" -c "SELECT * FROM users LIMIT 10;"
```

### List tables

```bash
psql "$DATABASE_URL" -c "\dt"
```

### Describe table

```bash
psql "$DATABASE_URL" -c "\d users"
```

### Insert data

```bash
psql "$DATABASE_URL" -c "INSERT INTO users (name, email) VALUES ('John', 'john@example.com');"
```

---

## Author

Anthropic

## Version

1.0.0
