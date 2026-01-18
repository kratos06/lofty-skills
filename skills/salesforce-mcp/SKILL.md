---
name: salesforce
description: Salesforce CRM data and operations integration
---

# Salesforce Integration

Salesforce CRM data and operations integration

## Configuration

### Environment Variable

```bash
export SALESFORCE_TOKEN="your-api-key"
```

### Get API Credentials

Setup → Apps → App Manager → Connected App → OAuth

---

## API Reference

**Base URL:** `https://{instance}.salesforce.com/services/data/v58.0`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $SALESFORCE_TOKEN" \
  "https://{instance}.salesforce.com/services/data/v58.0/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/sobjects` | List objects |
| GET | `/query` | SOQL query |
| POST | `/sobjects/Account` | Create account |
| PATCH | `/sobjects/Account/{id}` | Update account |
| GET | `/sobjects/Contact/{id}` | Get contact |

## Examples

### 1. List objects

```bash
curl -s -H "Authorization: Bearer $SALESFORCE_TOKEN" \
  "https://{instance}.salesforce.com/services/data/v58.0/sobjects"
```

### 2. SOQL query

```bash
curl -s -H "Authorization: Bearer $SALESFORCE_TOKEN" \
  "https://{instance}.salesforce.com/services/data/v58.0/query?q=SELECT Id,Name FROM Account LIMIT 10"
```

### 3. Create account

```bash
curl -s -H "Authorization: Bearer $SALESFORCE_TOKEN" -X POST -H "Content-Type: application/json" -d '{"Name":"Acme Corp"}' \
  "https://{instance}.salesforce.com/services/data/v58.0/sobjects/Account"
```

### 4. Update account

```bash
curl -s -H "Authorization: Bearer $SALESFORCE_TOKEN" -X PATCH -H "Content-Type: application/json" -d '{"Name":"New Name"}' \
  "https://{instance}.salesforce.com/services/data/v58.0/sobjects/Account/{id}"
```

### 5. Get contact

```bash
curl -s -H "Authorization: Bearer $SALESFORCE_TOKEN" \
  "https://{instance}.salesforce.com/services/data/v58.0/sobjects/Contact/{id}"
```

---

## Author

salesforce

## Version

1.0.0
