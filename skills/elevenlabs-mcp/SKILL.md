---
name: elevenlabs-mcp
description: ElevenLabs AI voice synthesis
---

# elevenlabs-mcp

ElevenLabs AI voice synthesis

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-elevenlabs
```

### Step 2: Get API Credentials

Get your credentials from: https://elevenlabs.io/app/settings/api-keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "elevenlabs": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-elevenlabs"],
      "env": {
            "ELEVENLABS_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available elevenlabs commands"
```

---

## Environment Variables

- `ELEVENLABS_API_KEY`: Required - Your api-key

## Available Tools

- `text_to_speech`
- `list_voices`
- `clone_voice`

## Quick Start Examples

### Example 1
```
User: "Help me with elevenlabs"
```

## Documentation

See @anthropic/mcp-elevenlabs documentation for more details.



## Author

elevenlabs

## Version

1.0.0
