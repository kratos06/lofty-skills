---
name: pagerduty-mcp
description: PagerDuty incident management
---

# pagerduty-mcp

PagerDuty incident management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "pagerduty-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-pagerduty"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add pagerduty-mcp
```

## Quick Start

After configuration, the pagerduty-mcp tools will be available in Claude Code.

## Features

- pagerduty
- incidents
- alerts





## Author

pagerduty

## Version

1.0.0
