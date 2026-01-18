---
name: time
description: Time and timezone operations
---

# Time & Date Integration

Time and timezone operations

## Configuration

## Commands

### Current date/time

```bash
date
```

### UTC time

```bash
date -u
```

### Time in timezone

```bash
TZ="America/New_York" date
```

### Date to timestamp

```bash
date -d "2024-12-25" +%s
```

### Timestamp to date

```bash
date -d @1703462400
```

---

## Author

community

## Version

1.0.0
