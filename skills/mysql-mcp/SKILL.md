---
name: mysql
description: MySQL database operations
---

# MySQL Integration

MySQL database operations

## Configuration

### Environment Variables

```bash
export MYSQL_HOST="your-value"
export MYSQL_USER="your-value"
export MYSQL_PASSWORD="your-value"
export MYSQL_DATABASE="your-value"
```

## Database Commands

### Query data

```bash
mysql -h "$MYSQL_HOST" -u "$MYSQL_USER" -p"$MYSQL_PASSWORD" "$MYSQL_DATABASE" -e "SELECT * FROM users LIMIT 10;"
```

### List tables

```bash
mysql -h "$MYSQL_HOST" -u "$MYSQL_USER" -p"$MYSQL_PASSWORD" "$MYSQL_DATABASE" -e "SHOW TABLES;"
```

### Describe table

```bash
mysql -h "$MYSQL_HOST" -u "$MYSQL_USER" -p"$MYSQL_PASSWORD" "$MYSQL_DATABASE" -e "DESCRIBE users;"
```

---

## Author

mysql

## Version

1.0.0
