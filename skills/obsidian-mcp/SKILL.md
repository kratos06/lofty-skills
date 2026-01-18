---
name: obsidian
description: Obsidian notes and knowledge base
---

# Obsidian Integration

Obsidian notes and knowledge base

## Configuration

## Commands

### Read note

```bash
cat "$OBSIDIAN_VAULT_PATH/note.md"
```

### Create note

```bash
echo "# Title

Content" > "$OBSIDIAN_VAULT_PATH/new-note.md"
```

### List notes

```bash
find "$OBSIDIAN_VAULT_PATH" -name "*.md" | head -20
```

### Search notes

```bash
grep -r "search term" "$OBSIDIAN_VAULT_PATH"
```

---

## Author

obsidian

## Version

1.0.0
