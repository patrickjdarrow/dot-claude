# dot-claude

Personal [Claude Code](https://claude.ai/code) user configuration, shared across machines.

## Contents

| File | Purpose |
|------|---------|
| `CLAUDE.md` | User-level instructions loaded by Claude Code in every project |

## Setup on a new machine

```bash
git clone https://github.com/patrickjdarrow/dot-claude ~/git/dot-claude
ln -s ~/git/dot-claude/CLAUDE.md ~/.claude/CLAUDE.md
```

## Keeping it updated

Edit `~/git/dot-claude/CLAUDE.md` directly (the symlink means changes are live immediately), then commit and push:

```bash
cd ~/git/dot-claude
git add CLAUDE.md
git commit -m "Update user instructions"
git push
```

On other machines: `git pull` inside `~/git/dot-claude`.

## How it fits with project-level CLAUDE.md

| File | Scope | Versioned where |
|------|-------|----------------|
| `~/.claude/CLAUDE.md` | All projects, personal only | This repo |
| `<project>/CLAUDE.md` | One project, shared with team | Project repo |

Project-level instructions take precedence over user-level when both exist.