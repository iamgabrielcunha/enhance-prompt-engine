# Installation Guide

## Prerequisites

You need [Claude Code](https://www.anthropic.com/claude-code) installed and authenticated. If you don't have it yet, install it from Anthropic's documentation first.

## Quick install — one command

```bash
mkdir -p ~/.claude/commands && curl -o ~/.claude/commands/enhance.md \
  https://raw.githubusercontent.com/iamgabrielcunha/enhance-prompt-engine/main/commands/enhance.md
```

That's it. The command is now available in any Claude Code session.

## Manual install

If you prefer to inspect the file before installing:

1. Download `commands/enhance.md` from this repository
2. Create the Claude Code commands directory if it doesn't exist:
   ```bash
   mkdir -p ~/.claude/commands
   ```
3. Copy the file:
   ```bash
   cp /path/to/downloaded/enhance.md ~/.claude/commands/enhance.md
   ```

## Verify installation

Open Claude Code and type:

```
/enhance hello world
```

You should see Claude Code start running the enhancement pipeline. If the command is not recognised, check that the file is in the exact path `~/.claude/commands/enhance.md` and that it has read permissions:

```bash
ls -la ~/.claude/commands/enhance.md
chmod 644 ~/.claude/commands/enhance.md
```

## Optional — customise for your ecosystem

The default `enhance.md` includes a scan for an Obsidian vault at `~/Documents/My Mind/`. If your vault is elsewhere or you don't use Obsidian, edit the file and update the path under "Phase 1A — Ecosystem Scan".

You can also add custom skill directories. Open `~/.claude/commands/enhance.md` and modify the `ls` and `find` commands in Phase 1A to point to your own folders.

## Updating

To pull the latest version:

```bash
curl -o ~/.claude/commands/enhance.md \
  https://raw.githubusercontent.com/iamgabrielcunha/enhance-prompt-engine/main/commands/enhance.md
```

This overwrites your existing file. If you have customised it, back it up first:

```bash
cp ~/.claude/commands/enhance.md ~/.claude/commands/enhance.md.backup
```

## Uninstall

```bash
rm ~/.claude/commands/enhance.md
```
