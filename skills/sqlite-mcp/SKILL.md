---
name: sqlite
description: SQLite local database operations
---

# SQLite Integration

SQLite local database operations

## Configuration

## Database Commands

### Query data

```bash
sqlite3 "$SQLITE_PATH" "SELECT * FROM users LIMIT 10;"
```

### List tables

```bash
sqlite3 "$SQLITE_PATH" ".tables"
```

### Show schema

```bash
sqlite3 "$SQLITE_PATH" ".schema users"
```

### Insert data

```bash
sqlite3 "$SQLITE_PATH" "INSERT INTO users (name) VALUES ('John');"
```

---

## Author

Anthropic

## Version

1.0.0
