---
name: translate-mcp
description: Translation services integration
---

# translate-mcp

Translation services integration

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "translate-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-translate"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add translate-mcp
```

## Quick Start

After configuration, the translate-mcp tools will be available in Claude Code.

## Features

- translate
- languages
- i18n





## Author

community

## Version

1.0.0
