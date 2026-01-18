---
name: firecrawl-mcp
description: Firecrawl web scraping and search capabilities (Official)
---

# firecrawl-mcp

Firecrawl web scraping and search capabilities (Official)

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-firecrawl
```

### Step 2: Get API Credentials

Get your credentials from: https://firecrawl.dev/app/api-keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "firecrawl": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-firecrawl"],
      "env": {
            "FIRECRAWL_API_KEY": "fc-your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available firecrawl commands"
```

---

## Environment Variables

- `FIRECRAWL_API_KEY`: Required - fc-Your api-key

## Available Tools

- `scrape`
- `crawl`
- `map`

## Quick Start Examples

### Example 1
```
User: "Help me with firecrawl"
```

## Documentation

See @anthropic/mcp-firecrawl documentation for more details.

## Source

GitHub: https://github.com/firecrawl/mcp-server

## Author

Firecrawl

## Version

1.0.0
