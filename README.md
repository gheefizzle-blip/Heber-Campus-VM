# Claude Atlas Virtual Memory

Governed filesystem for Virtual Memory snapshots, deltas, and canonical state.

## Directory Structure

- **00_CANON/**: Authoritative CORE_VM.md
- **01_CHAT_VM_ARCHIVE/**: Immutable per-chat snapshots
- **02_VM_DELTAS/**: Change records (deltas) applied to CORE_VM.md
- **03_REBUILD_MANIFESTS/**: Deterministic rebuild index
- **04_WORK_ORDERS/**: Infrastructure and operational directives

All directories are append-only. No deletions. No renames.
