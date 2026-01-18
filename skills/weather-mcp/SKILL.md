---
name: weather-mcp
description: Weather data and forecasts
---

# weather-mcp

Weather data and forecasts

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-weather
```

### Step 2: Get API Credentials

Get your credentials from: https://home.openweathermap.org/api_keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "weather": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-weather"],
      "env": {
            "OPENWEATHER_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available weather commands"
```

---

## Environment Variables

- `OPENWEATHER_API_KEY`: Required - Your api-key

## Available Tools

- `get_current`
- `get_forecast`
- `get_historical`

## Quick Start Examples

### Example 1
```
User: "Help me with weather"
```

## Documentation

See @anthropic/mcp-weather documentation for more details.



## Author

community

## Version

1.0.0
