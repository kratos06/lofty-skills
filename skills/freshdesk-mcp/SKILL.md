---
name: freshdesk
description: Freshdesk helpdesk ticketing system integration
---

# Freshdesk Integration

Freshdesk helpdesk ticketing system integration

## Configuration

### Environment Variable

```bash
export FRESHDESK_API_KEY="your-api-key"
```

### Get API Credentials

Profile Settings → Your API Key

---

## API Reference

**Base URL:** `https://{domain}.freshdesk.com/api/v2`

**Authentication:** Basic Auth

```bash
curl -u "{FRESHDESK_API_KEY}:X" \
  "https://{domain}.freshdesk.com/api/v2/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/tickets` | List tickets |
| GET | `/tickets/{id}` | Get ticket |
| POST | `/tickets` | Create ticket |
| PUT | `/tickets/{id}` | Update ticket |
| GET | `/contacts` | List contacts |

## Examples

### 1. List tickets

```bash
curl -s -u "$FRESHDESK_API_KEY:X" \
  "https://{domain}.freshdesk.com/api/v2/tickets"
```

### 2. Get ticket

```bash
curl -s -u "$FRESHDESK_API_KEY:X" \
  "https://{domain}.freshdesk.com/api/v2/tickets/{id}"
```

### 3. Create ticket

```bash
curl -s -u "$FRESHDESK_API_KEY:X" -X POST -H "Content-Type: application/json" -d '{"subject":"Issue","description":"Details","email":"customer@example.com","priority":1,"status":2}' \
  "https://{domain}.freshdesk.com/api/v2/tickets"
```

### 4. Update ticket

```bash
curl -s -u "$FRESHDESK_API_KEY:X" -X PUT -H "Content-Type: application/json" -d '{"status":4}' \
  "https://{domain}.freshdesk.com/api/v2/tickets/{id}"
```

### 5. List contacts

```bash
curl -s -u "$FRESHDESK_API_KEY:X" \
  "https://{domain}.freshdesk.com/api/v2/contacts"
```

---

## Author

Freshworks

## Version

1.0.0
