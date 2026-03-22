# CLI-Anything PM2 Harness

A complete CLI harness for managing PM2 processes via subprocess commands.

## Installation

```bash
cd agent-harness
pip install -e .
```

## Usage

### REPL mode (default)
```bash
cli-anything-pm2
```

### Direct commands
```bash
cli-anything-pm2 process list
cli-anything-pm2 --json process list
cli-anything-pm2 process describe seaclip-dev
cli-anything-pm2 lifecycle restart seaclip-dev
cli-anything-pm2 lifecycle stop hub-dashboard
cli-anything-pm2 lifecycle start /path/to/app.js --name my-service
cli-anything-pm2 lifecycle delete old-service
cli-anything-pm2 logs view voice-agent --lines 50
cli-anything-pm2 logs flush voice-agent
cli-anything-pm2 system save
cli-anything-pm2 system startup
cli-anything-pm2 system version
```

## Command Groups

| Group       | Commands                          |
|-------------|-----------------------------------|
| `process`   | list, describe, metrics           |
| `lifecycle` | start, stop, restart, delete      |
| `logs`      | view, flush                       |
| `system`    | save, startup, version            |

## JSON Output

All commands support `--json` flag for machine-readable output.

## Architecture

- **Backend**: PM2 CLI commands executed via `subprocess.run()`
- **Frontend**: Click CLI with prompt-toolkit REPL
- **Skin**: Unified cli-anything REPL skin for consistent branding
