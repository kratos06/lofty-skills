---
name: weather-mcp
description: Weather data and forecasts
---

# weather-mcp

Weather data and forecasts

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "weather-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-weather"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add weather-mcp
```

## Quick Start

After configuration, the weather-mcp tools will be available in Claude Code.

## Features

- weather
- forecast
- climate





## Author

community

## Version

1.0.0
