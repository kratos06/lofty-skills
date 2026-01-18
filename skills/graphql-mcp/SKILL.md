---
name: graphql-mcp
description: GraphQL query and schema management
---

# graphql-mcp

GraphQL query and schema management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-graphql
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "graphql": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-graphql"],
      "env": {
            "GRAPHQL_ENDPOINT": "https://api.example.com/graphql",
            "GRAPHQL_TOKEN": "your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available graphql commands"
```

---

## Environment Variables

- `GRAPHQL_ENDPOINT`: https://api.example.com/graphql
- `GRAPHQL_TOKEN`: Required - Your token

## Available Tools

- `query`
- `mutate`
- `introspect`

## Quick Start Examples

### Example 1
```
User: "Help me with graphql"
```

## Documentation

See @anthropic/mcp-graphql documentation for more details.



## Author

graphql

## Version

1.0.0
