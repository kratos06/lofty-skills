---
name: stripe
description: Stripe payment processing, subscriptions, and invoicing
---

# Stripe Integration

Stripe payment processing, subscriptions, and invoicing

## Configuration

### Environment Variable

```bash
export STRIPE_SECRET_KEY="your-api-key"
```

### Get API Credentials

https://dashboard.stripe.com/apikeys

---

## API Reference

**Base URL:** `https://api.stripe.com/v1`

**Authentication:** Bearer token in `Authorization` header

```bash
curl -H "Authorization: Bearer $STRIPE_SECRET_KEY" \
  "https://api.stripe.com/v1/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/customers` | List customers |
| POST | `/customers` | Create customer |
| GET | `/charges` | List charges |
| POST | `/charges` | Create charge |
| GET | `/subscriptions` | List subscriptions |
| POST | `/payment_intents` | Create payment intent |

## Examples

### 1. List customers

```bash
curl -s -H "Authorization: Bearer $STRIPE_SECRET_KEY" \
  "https://api.stripe.com/v1/customers"
```

### 2. Create customer

```bash
curl -s -H "Authorization: Bearer $STRIPE_SECRET_KEY" -X POST -H "Content-Type: application/json" -d '{"email":"customer@example.com","name":"John Doe"}' \
  "https://api.stripe.com/v1/customers"
```

### 3. List charges

```bash
curl -s -H "Authorization: Bearer $STRIPE_SECRET_KEY" \
  "https://api.stripe.com/v1/charges"
```

### 4. Create charge

```bash
curl -s -H "Authorization: Bearer $STRIPE_SECRET_KEY" -X POST -H "Content-Type: application/json" -d '{"amount":2000,"currency":"usd","source":"tok_visa"}' \
  "https://api.stripe.com/v1/charges"
```

### 5. List subscriptions

```bash
curl -s -H "Authorization: Bearer $STRIPE_SECRET_KEY" \
  "https://api.stripe.com/v1/subscriptions"
```

### 6. Create payment intent

```bash
curl -s -H "Authorization: Bearer $STRIPE_SECRET_KEY" -X POST -H "Content-Type: application/json" -d '{"amount":2000,"currency":"usd"}' \
  "https://api.stripe.com/v1/payment_intents"
```

---

## Author

Stripe

## Version

1.0.0
