# Claude Code Global Configuration

Version-controlled global settings for Claude Code that can be synced across machines.

## What's Included

- `CLAUDE.md` - Global instructions and preferences
- `settings.json` - User settings (enabled plugins, preferences)
- `PLUGINS.md` - Documentation of which plugins to install
- `.gitignore` - Excludes logs, cache, and machine-specific data

## What's Excluded

All machine-specific data is excluded:
- Session logs and history (may contain sensitive data)
- Cached plugin metadata with absolute paths
- Project-specific cache
- Debug logs and session state

## Setup on New Machine

1. Clone this repo to `~/.claude`:
   ```bash
   git clone <your-repo-url> ~/.claude
   ```

2. Install marketplaces and plugins as documented in `PLUGINS.md`

3. Claude Code will regenerate machine-specific metadata automatically

## Maintenance

- Update `PLUGINS.md` when installing/removing plugins
- Commit changes to `CLAUDE.md` and `settings.json` as needed
- The `.gitignore` ensures sensitive data never gets committed
