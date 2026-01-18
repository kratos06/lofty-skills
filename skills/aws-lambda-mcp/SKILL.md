---
name: aws-lambda-mcp
description: AWS Lambda function management
---

# aws-lambda-mcp

AWS Lambda function management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "aws-lambda-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-aws-lambda"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add aws-lambda-mcp
```

## Quick Start

After configuration, the aws-lambda-mcp tools will be available in Claude Code.

## Features

- aws
- lambda
- serverless





## Author

aws

## Version

1.0.0
