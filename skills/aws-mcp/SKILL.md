---
name: aws-mcp
description: AWS comprehensive integration with documentation and best practices (Official)
---

# aws-mcp

AWS comprehensive integration with documentation and best practices (Official)

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "aws-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-aws"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add aws-mcp
```

## Quick Start

After configuration, the aws-mcp tools will be available in Claude Code.

## Features

- aws
- cloud
- infrastructure



## Source

GitHub: https://github.com/awslabs/mcp

## Author

AWS

## Version

1.2.0
