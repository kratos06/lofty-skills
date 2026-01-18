---
name: hubspot
description: HubSpot CRM, marketing, and sales automation
---

# HubSpot Integration

HubSpot CRM, marketing, and sales automation

## Configuration

### Environment Variable

```bash
export HUBSPOT_TOKEN="your-api-key"
```

### Get API Credentials

https://app.hubspot.com → Settings → Integrations → Private Apps

---

## API Reference

**Base URL:** `https://api.hubapi.com`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $HUBSPOT_TOKEN" \
  "https://api.hubapi.com/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/crm/v3/objects/contacts` | List contacts |
| POST | `/crm/v3/objects/contacts` | Create contact |
| GET | `/crm/v3/objects/deals` | List deals |
| POST | `/crm/v3/objects/deals` | Create deal |
| GET | `/crm/v3/objects/companies` | List companies |

## Examples

### 1. List contacts

```bash
curl -s -H "Authorization: Bearer $HUBSPOT_TOKEN" \
  "https://api.hubapi.com/crm/v3/objects/contacts"
```

### 2. Create contact

```bash
curl -s -H "Authorization: Bearer $HUBSPOT_TOKEN" -X POST -H "Content-Type: application/json" -d '{"properties":{"email":"test@example.com","firstname":"John"}}' \
  "https://api.hubapi.com/crm/v3/objects/contacts"
```

### 3. List deals

```bash
curl -s -H "Authorization: Bearer $HUBSPOT_TOKEN" \
  "https://api.hubapi.com/crm/v3/objects/deals"
```

### 4. Create deal

```bash
curl -s -H "Authorization: Bearer $HUBSPOT_TOKEN" -X POST -H "Content-Type: application/json" -d '{"properties":{"dealname":"New Deal","amount":"1000"}}' \
  "https://api.hubapi.com/crm/v3/objects/deals"
```

### 5. List companies

```bash
curl -s -H "Authorization: Bearer $HUBSPOT_TOKEN" \
  "https://api.hubapi.com/crm/v3/objects/companies"
```

---

## Author

hubspot

## Version

1.0.0
