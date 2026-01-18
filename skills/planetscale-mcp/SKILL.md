---
name: planetscale-mcp
description: PlanetScale serverless MySQL
---

# planetscale-mcp

PlanetScale serverless MySQL

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "planetscale-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-planetscale"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add planetscale-mcp
```

## Quick Start

After configuration, the planetscale-mcp tools will be available in Claude Code.

## Features

- planetscale
- mysql
- serverless





## Author

planetscale

## Version

1.0.0
