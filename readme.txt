This project provides a simple local sync script named ./sync.
It syncs files from SOURCE (SSD) to DESTINATION (HDD) and makes DESTINATION match SOURCE exactly.

Prerequisites
- bash
- rsync

Project Files
- sync: main script
- config.conf: source and destination paths

Configuration
1. Edit config.conf and set absolute paths:
	 SOURCE="/absolute/path/to/source"
	 DESTINATION="/absolute/path/to/destination"
2. Or run interactive setup:
	 ./sync --config

Usage
- Show help:
	./sync --help
- Preview changes only (no write):
	./sync --dry-run
- Run sync (with confirmation step):
	./sync --run

Behavior
- SOURCE is never modified.
- DESTINATION is updated to match SOURCE.
- Files in DESTINATION that do not exist in SOURCE are deleted.

Notes
- Use absolute paths in config.conf.
- Run dry-run first to review planned changes.
