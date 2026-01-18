---
name: mongodb
description: MongoDB database with Atlas, Community, and vector search support (Official)
---

# MongoDB Integration

MongoDB database with Atlas, Community, and vector search support (Official)

## Configuration

## Database Commands

### Connection String

```bash
export MONGODB_URI="mongodb://localhost:27017/database"
```

### Query data

```bash
mongosh "$MONGODB_URI" --eval "db.users.find().limit(10)"
```

### List collections

```bash
mongosh "$MONGODB_URI" --eval "db.getCollectionNames()"
```

### Insert document

```bash
mongosh "$MONGODB_URI" --eval "db.users.insertOne({name: 'John', email: 'john@example.com'})"
```

### Update document

```bash
mongosh "$MONGODB_URI" --eval "db.users.updateOne({name: 'John'}, {\$set: {status: 'active'}})"
```

---

## Author

MongoDB

## Version

1.0.0
