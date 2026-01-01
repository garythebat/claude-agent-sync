# Claude Code Agents

A collection of custom agents for [Claude Code](https://claude.com/claude-code) that extend its capabilities with reusable workflows.

## Agents

| Agent | Description | Model |
|-------|-------------|-------|
| `agents-sync` | Sync agents folder with GitHub (push/pull/status) | Haiku |
| `agent-sync-pi` | Same as above, with Linux-specific init for Raspberry Pi | Haiku |
| `project-init` | Initialize any project type with proper structure and documentation | Opus |
| `script-session-closer` | End-of-session summaries, context sync, and commit management | Sonnet |

## Installation

Clone this repo to your Claude Code agents folder:

```bash
cd ~/.claude/agents
git init
git remote add origin https://github.com/garythebat/claudesync.git
git pull origin main
```

## Usage

Reference any agent in Claude Code by mentioning the file:

```
@agents-sync.md push my changes
@project-init.md set up a new Python project
@script-session-closer.md wrap up this session
```

## Syncing Across Machines

These agents are designed to sync across multiple machines. After making changes:

```bash
# Push changes
cd ~/.claude/agents && git add -A && git commit -m "description" && git push

# Pull on another machine
cd ~/.claude/agents && git pull
```

## License

MIT
