---
name: planetscale-mcp
description: PlanetScale serverless MySQL
---

# planetscale-mcp

PlanetScale serverless MySQL

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-planetscale
```

### Step 2: Get API Credentials

Get your credentials from: https://app.planetscale.com/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "planetscale": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-planetscale"],
      "env": {
            "PLANETSCALE_HOST": "your-host.psdb.cloud",
            "PLANETSCALE_USERNAME": "your-username",
            "PLANETSCALE_PASSWORD": "your-password"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available planetscale commands"
```

---

## Environment Variables

- `PLANETSCALE_HOST`: Required - Your host.psdb.cloud
- `PLANETSCALE_USERNAME`: Required - Your username
- `PLANETSCALE_PASSWORD`: Required - Your password

## Available Tools

- `query`
- `list_tables`
- `describe_table`

## Quick Start Examples

### Example 1
```
User: "Help me with planetscale"
```

## Documentation

See @anthropic/mcp-planetscale documentation for more details.



## Author

planetscale

## Version

1.0.0
