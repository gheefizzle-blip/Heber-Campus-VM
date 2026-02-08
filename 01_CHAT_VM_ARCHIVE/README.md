# Chat VM Archive

Immutable snapshots of VM state after each chat thread.

## File Naming Convention

`CHAT_<THREADNAME>_<YYYYMMDD-HHMM>.md`

## Organization

Files are organized by month (`YYYY-MM/`) to prevent directory bloat.

All snapshots are append-only. Once created, never modified.
