---
name: discord
description: Discord bot and messaging integration
---

# Discord Integration

Discord bot and messaging integration

## Configuration

### Environment Variable

```bash
export DISCORD_BOT_TOKEN="your-api-key"
```

### Get API Credentials

https://discord.com/developers/applications → Bot → Token

---

## API Reference

**Base URL:** `https://discord.com/api/v10`

**Authentication:** Bot token

```bash
curl -H "Authorization: Bot $DISCORD_BOT_TOKEN" \
  "https://discord.com/api/v10/endpoint"
```

## Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/guilds/{guild_id}/channels` | List channels |
| POST | `/channels/{channel_id}/messages` | Send message |
| GET | `/channels/{channel_id}/messages` | Get messages |
| POST | `/guilds/{guild_id}/channels` | Create channel |

## Examples

### 1. List channels

```bash
curl -s -H "Authorization: Bot $DISCORD_BOT_TOKEN" \
  "https://discord.com/api/v10/guilds/{guild_id}/channels"
```

### 2. Send message

```bash
curl -s -H "Authorization: Bot $DISCORD_BOT_TOKEN" -X POST -H "Content-Type: application/json" -d '{"content":"Hello!"}' \
  "https://discord.com/api/v10/channels/{channel_id}/messages"
```

### 3. Get messages

```bash
curl -s -H "Authorization: Bot $DISCORD_BOT_TOKEN" \
  "https://discord.com/api/v10/channels/{channel_id}/messages?limit=50"
```

### 4. Create channel

```bash
curl -s -H "Authorization: Bot $DISCORD_BOT_TOKEN" -X POST -H "Content-Type: application/json" -d '{"name":"new-channel","type":0}' \
  "https://discord.com/api/v10/guilds/{guild_id}/channels"
```

---

## Author

discord

## Version

1.0.0
