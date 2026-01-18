---
name: paypal
description: PayPal payment integration
---

# PayPal Integration

PayPal payment integration

## Configuration

### Get API Credentials

https://developer.paypal.com/dashboard/applications/sandbox

---

## API Reference

**Base URL:** `https://api-m.sandbox.paypal.com/v2`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $undefined" \
  "https://api-m.sandbox.paypal.com/v2/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/checkout/orders` | Create order |
| POST | `/checkout/orders/{id}/capture` | Capture payment |
| GET | `/checkout/orders/{id}` | Get order |

## Examples

### 1. Create order

```bash
curl -s -H "Authorization: Bearer $undefined" -X POST -H "Content-Type: application/json" -d '{"intent":"CAPTURE","purchase_units":[{"amount":{"currency_code":"USD","value":"10.00"}}]}' \
  "https://api-m.sandbox.paypal.com/v2/checkout/orders"
```

### 2. Capture payment

```bash
curl -s -H "Authorization: Bearer $undefined" -X POST -H "Content-Type: application/json" \
  "https://api-m.sandbox.paypal.com/v2/checkout/orders/{id}/capture"
```

### 3. Get order

```bash
curl -s -H "Authorization: Bearer $undefined" \
  "https://api-m.sandbox.paypal.com/v2/checkout/orders/{id}"
```

---

## Author

paypal

## Version

1.0.0
