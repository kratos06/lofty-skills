---
name: aws-lambda-mcp
description: AWS Lambda function management
---

# aws-lambda-mcp

AWS Lambda function management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-aws-lambda
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "aws-lambda": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-aws-lambda"],
      "env": {
            "AWS_ACCESS_KEY_ID": "your-access-key",
            "AWS_SECRET_ACCESS_KEY": "your-secret-key",
            "AWS_REGION": "us-east-1"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available aws-lambda commands"
```

---

## Environment Variables

- `AWS_ACCESS_KEY_ID`: Required - Your access-key
- `AWS_SECRET_ACCESS_KEY`: Required - Your secret-key
- `AWS_REGION`: us-east-1

## Available Tools

- `list_functions`
- `invoke`
- `get_function`
- `create_function`

## Quick Start Examples

### Example 1
```
User: "Help me with aws-lambda"
```

## Documentation

See @anthropic/mcp-aws-lambda documentation for more details.



## Author

aws

## Version

1.0.0
