---
name: twilio
description: Twilio SMS and voice communication
---

# Twilio Integration

Twilio SMS and voice communication

## Configuration

### Environment Variables

Set these in your shell profile (`~/.zshrc` or `~/.bashrc`):

```bash
export TWILIO_ACCOUNT_SID="your-twilio-account-sid"
export TWILIO_AUTH_TOKEN="your-twilio-auth-token"
```

### Get API Credentials

https://console.twilio.com → Account → API keys

---

## API Reference

**Base URL:** `https://api.twilio.com/2010-04-01/Accounts/{TWILIO_ACCOUNT_SID}`

**Authentication:** Basic Auth

```bash
curl -u "{TWILIO_ACCOUNT_SID}:{TWILIO_AUTH_TOKEN}" \
  "https://api.twilio.com/2010-04-01/Accounts/{TWILIO_ACCOUNT_SID}/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/Messages.json` | Send SMS |
| GET | `/Messages.json` | List messages |
| POST | `/Calls.json` | Make call |

## Examples

### 1. Send SMS

```bash
curl -s -u "$TWILIO_ACCOUNT_SID:$TWILIO_AUTH_TOKEN" -X POST -H "Content-Type: application/json" -d '{"To":"+1234567890","From":"+0987654321","Body":"Hello!"}' \
  "https://api.twilio.com/2010-04-01/Accounts/{TWILIO_ACCOUNT_SID}/Messages.json"
```

### 2. List messages

```bash
curl -s -u "$TWILIO_ACCOUNT_SID:$TWILIO_AUTH_TOKEN" \
  "https://api.twilio.com/2010-04-01/Accounts/{TWILIO_ACCOUNT_SID}/Messages.json"
```

### 3. Make call

```bash
curl -s -u "$TWILIO_ACCOUNT_SID:$TWILIO_AUTH_TOKEN" -X POST -H "Content-Type: application/json" -d '{"To":"+1234567890","From":"+0987654321","Url":"http://demo.twilio.com/docs/voice.xml"}' \
  "https://api.twilio.com/2010-04-01/Accounts/{TWILIO_ACCOUNT_SID}/Calls.json"
```

---

## Author

Twilio

## Version

1.0.0
