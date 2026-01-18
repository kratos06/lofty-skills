---
name: aws-s3-mcp
description: AWS S3 bucket and object operations
---

# aws-s3-mcp

AWS S3 bucket and object operations

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "aws-s3-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-aws-s3"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add aws-s3-mcp
```

## Quick Start

After configuration, the aws-s3-mcp tools will be available in Claude Code.

## Features

- aws
- s3
- storage





## Author

aws

## Version

1.0.0
