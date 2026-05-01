Filename: VM_DELTA_VM_DELTA_LOGGING_DOCTRINE_20260430-0005.md

## DELTA BEGIN

[2026-04-30] Established VM Delta Logging Doctrine requiring a dedicated append-only VM delta log to track every generated, committed, applied, failed, or remediated VM delta file.

[2026-04-30] Locked requirement that VM delta logging include both machine-readable CSV and human-readable Markdown formats.

[2026-04-30] Defined VM_DELTA_LOG.csv as the machine-readable delta ledger with required fields: timestamp, thread_name, chat_file, delta_file, vm_version, commit_hash, status, notes.

[2026-04-30] Defined VM_DELTA_LOG.md as the human-readable delta audit log summarizing each delta entry, status, associated VM version, and commit hash.

[2026-04-30] Established that VM delta logs are append-only governance artifacts and may be written only by Claude Code as execution authority.

[2026-04-30] Established permitted delta status values: GENERATED, COMMITTED, APPLIED, FAILED, REMEDIATED.

[2026-04-30] Required Claude Code to append VM_DELTA_LOG.csv and VM_DELTA_LOG.md during every VM delta workflow after saving the delta, committing it, applying it to CORE_VM.md, or recording a failure condition.

[2026-04-30] Established that VM delta logs supplement but do not replace REBUILD_INDEX.md, CORE_VM.md metadata, chat archives, or individual VM_DELTA files.

## DELTA END
