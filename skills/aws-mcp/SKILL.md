---
name: aws-mcp
description: AWS comprehensive integration with documentation and best practices (Official)
---

# aws-mcp

AWS comprehensive integration with documentation and best practices (Official)

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-aws
```

### Step 2: Get API Credentials

Get your credentials from: https://console.aws.amazon.com/iam/home#/security_credentials

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "aws": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-aws"],
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
User: "List available aws commands"
```

---

## Environment Variables

- `AWS_ACCESS_KEY_ID`: Required - Your access-key
- `AWS_SECRET_ACCESS_KEY`: Required - Your secret-key
- `AWS_REGION`: us-east-1

## Available Tools

- `s3_list`
- `s3_get`
- `s3_put`
- `lambda_invoke`
- `ec2_describe`

## Quick Start Examples

### Example 1
```
User: "Help me with aws"
```

## Documentation

See @anthropic/mcp-aws documentation for more details.

## Source

GitHub: https://github.com/awslabs/mcp

## Author

AWS

## Version

1.2.0
