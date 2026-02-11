# WO_VM_COMMITTER_CLAUDE — VM Delta Commit Work Order

**Work Order ID:** HCV-VM-COMMIT-001
**Status:** Active
**Assigned To:** Agent B (Claude Code)
**Purpose:** Ingest delta files into CORE_VM.md, commit to Git, push to GitHub, sync NAS

---

## Trigger

Commander pastes a delta file (produced by Agent A / ChatGPT) into the Claude Code session. The delta file follows the naming convention `VM_DELTA_[TOPIC]_[YYYYMMDD]-[HHMM].md` and contains `## DELTA BEGIN` / `## DELTA END` markers.

---

## 10-Step Deterministic Protocol

### Step 1: Save Delta to NAS
Save the delta file to:
```
Z:\SE_T1\GOVERNANCE\Claude Atlas Virtual Memory\02_VM_DELTAS\2026-02\[filename].md
```

### Step 2: Save Delta to GitHub Clone
Save the same file to:
```
C:\Users\Gary\Heber-Campus-VM\02_VM_DELTAS\2026-02\[filename].md
```

### Step 3: Collision Detection
- **Filename collision**: If a file with the same name already exists but different content, rename with `-B` suffix and ask Commander to confirm
- **VM_VERSION collision**: If the timestamp matches an existing REBUILD_INDEX entry, append `-2` suffix to the VM_VERSION
- **Exact duplicate**: If filename AND content match an existing delta, reject and report "DUPLICATE — already ingested as Delta N"

### Step 4: Read CORE_VM.md Tail
Read the last 20 lines of `C:\Users\Gary\Heber-Campus-VM\CORE_VM.md` to confirm current state.

### Step 5: Update Metadata Header
Update the top of CORE_VM.md:
- `**Last Updated:**` → date/time from delta
- `**VM_VERSION:**` → timestamp from delta filename (YYYYMMDD-HHMM format)
- `**Status:**` → "Delta applied - [topic description]"

### Step 6: Append Decisions
Append a new section to CORE_VM.md:
```markdown
---

## [Section Title] ([Date])

**Source:** [delta filename]

[Each decision entry from the delta, with blank lines between]
```

### Step 7: Update REBUILD_INDEX (Pending)
Append a new row to `03_REBUILD_MANIFESTS/REBUILD_INDEX.md`:
```
| [timestamp] | [thread name] | — | [delta filename] | [VM_VERSION] | <pending> |
```

### Step 8: Git Commit
```bash
cd C:\Users\Gary\Heber-Campus-VM
git add .
git commit -m "Delta NN: [topic] (VM_VERSION [version])"
```

### Step 9: Resolve Pending Hash
Replace `<pending>` in REBUILD_INDEX.md with the actual commit hash from Step 8. Then:
```bash
git add 03_REBUILD_MANIFESTS/REBUILD_INDEX.md
git commit -m "Finalize Delta NN commit hash"
```

### Step 10: Push and Sync
```bash
git push origin main
```
Then copy the updated REBUILD_INDEX.md to NAS:
```
Z:\SE_T1\GOVERNANCE\Claude Atlas Virtual Memory\03_REBUILD_MANIFESTS\REBUILD_INDEX.md
```

---

## Verification

After completion, report to Commander:
- Delta number (sequential)
- VM_VERSION applied
- Git commit hash
- REBUILD_INDEX row count
- Any collisions or anomalies

---

*Last Updated: 2026-02-10*
