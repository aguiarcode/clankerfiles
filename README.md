# clankerfiles

Claude Code config. Only the hand-written parts are tracked — plugins reinstall
themselves from the marketplaces recorded in `settings.json`.

```
.claude/settings.json   theme, model, enabled plugins + marketplaces
.claude/skills/         personal skills
```

## Install

Symlink into `~/.claude` (repo stays the source of truth):

```sh
# Linux / macOS
ln -sf ~/clankerfiles/.claude/settings.json ~/.claude/settings.json
ln -sfn ~/clankerfiles/.claude/skills       ~/.claude/skills
```

```powershell
# Windows (needs Developer Mode or an admin shell)
New-Item -ItemType SymbolicLink -Force -Path ~\.claude\settings.json -Target ~\clankerfiles\.claude\settings.json
New-Item -ItemType SymbolicLink -Force -Path ~\.claude\skills        -Target ~\clankerfiles\.claude\skills
```

Not tracked, and shouldn't be: `.credentials.json` (auth token), `history.jsonl`,
`projects/`, `sessions/`, `shell-snapshots/`, `file-history/`, `backups/`,
`cache/`, `paste-cache/`, `session-env/`, `plugins/`.
