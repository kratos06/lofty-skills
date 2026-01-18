---
name: swagger-mcp
description: OpenAPI/Swagger documentation generation
---

# swagger-mcp

OpenAPI/Swagger documentation generation

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "swagger-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-swagger"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add swagger-mcp
```

## Quick Start

After configuration, the swagger-mcp tools will be available in Claude Code.

## Features

- swagger
- openapi
- documentation





## Author

swagger

## Version

1.0.0
