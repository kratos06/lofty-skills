---
name: swagger-mcp
description: OpenAPI/Swagger documentation generation
---

# swagger-mcp

OpenAPI/Swagger documentation generation

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-swagger
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "swagger": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-swagger"],
      "env": {
            "SWAGGER_URL": "https://api.example.com/swagger.json"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available swagger commands"
```

---

## Environment Variables

- `SWAGGER_URL`: https://api.example.com/swagger.json

## Available Tools

- `get_spec`
- `list_endpoints`
- `try_endpoint`

## Quick Start Examples

### Example 1
```
User: "Help me with swagger"
```

## Documentation

See @anthropic/mcp-swagger documentation for more details.



## Author

swagger

## Version

1.0.0
