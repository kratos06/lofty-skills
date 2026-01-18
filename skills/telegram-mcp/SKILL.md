---
name: telegram
description: Telegram Bot API integration
---

# Telegram Integration

Telegram Bot API integration

## Configuration

### Environment Variable

```bash
export TELEGRAM_BOT_TOKEN="your-api-key"
```

### Get API Credentials

Message @BotFather on Telegram → /newbot

---

## API Reference

**Base URL:** `https://api.telegram.org/bot{TELEGRAM_BOT_TOKEN}`

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/getMe` | Get bot info |
| POST | `/sendMessage` | Send message |
| GET | `/getUpdates` | Get updates/messages |
| POST | `/sendPhoto` | Send photo |

## Examples

### 1. Get bot info

```bash
curl -s \
  "https://api.telegram.org/bot{TELEGRAM_BOT_TOKEN}/getMe"
```

### 2. Send message

```bash
curl -s -X POST -H "Content-Type: application/json" -d '{"chat_id":"123","text":"Hello!"}' \
  "https://api.telegram.org/bot{TELEGRAM_BOT_TOKEN}/sendMessage"
```

### 3. Get updates/messages

```bash
curl -s \
  "https://api.telegram.org/bot{TELEGRAM_BOT_TOKEN}/getUpdates"
```

### 4. Send photo

```bash
curl -s -X POST -H "Content-Type: application/json" -d '{"chat_id":"123","photo":"url_or_file_id"}' \
  "https://api.telegram.org/bot{TELEGRAM_BOT_TOKEN}/sendPhoto"
```

---

## Author

telegram

## Version

1.0.0
