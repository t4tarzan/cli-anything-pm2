# PM2 CLI Tests

Test files for the PM2 CLI-Anything harness. Add test modules here.

## Test Plan

- [ ] Test pm2_backend.py subprocess wrapper with mocked subprocess
- [ ] Test process list/describe/metrics parsing
- [ ] Test lifecycle commands (start, stop, restart, delete)
- [ ] Test log retrieval and flush
- [ ] Test system commands (save, startup, version)
- [ ] Test JSON output flag across all commands
- [ ] Test REPL mode entry and exit
- [ ] Test error handling when PM2 is not installed
