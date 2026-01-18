---
name: aws-s3-mcp
description: AWS S3 bucket and object operations
---

# aws-s3-mcp

AWS S3 bucket and object operations

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-aws-s3
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "aws-s3": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-aws-s3"],
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
User: "List available aws-s3 commands"
```

---

## Environment Variables

- `AWS_ACCESS_KEY_ID`: Required - Your access-key
- `AWS_SECRET_ACCESS_KEY`: Required - Your secret-key
- `AWS_REGION`: us-east-1

## Available Tools

- `list_buckets`
- `list_objects`
- `get_object`
- `put_object`
- `delete_object`

## Quick Start Examples

### Example 1
```
User: "Help me with aws-s3"
```

## Documentation

See @anthropic/mcp-aws-s3 documentation for more details.



## Author

aws

## Version

1.0.0
