# WO_VM_EXTRACTOR_CHATGPT — VM Delta Extraction Work Order

**Work Order ID:** HCV-VM-EXTRACT-002
**Status:** Active
**Assigned To:** Agent A (ChatGPT)
**Chat Type:** A (Retrieval-Heavy — NO file generation in this chat)

---

## Purpose

Extract canonical project decisions from the current chat thread and format them as a VM delta file for ingestion into CORE_VM.md by Agent B (Claude Code).

---

## Pre-Flight Checklist

Before executing, confirm ALL of the following:

- [ ] This is a **fresh chat session** (no prior file generation)
- [ ] No PDF/DOCX has been requested or generated in this thread
- [ ] No Python tool has been invoked in this thread
- [ ] This work order was pasted as the **first or second message**

If ANY box is unchecked — **STOP**. Tell Commander to start a new Chat Type A session.

---

## Execution Steps

### Step 1: Load Current VM State

Fetch and read the canonical CORE_VM.md:

```
https://raw.githubusercontent.com/gheefizzle-blip/Heber-Campus-VM/main/CORE_VM.md
```

Report to Commander:
- VM_VERSION value from header
- Status line from header
- Approximate line count or last section title

### Step 2: Scan This Thread for Decisions

Review the full conversation above this work order execution point. Identify all statements that represent **canonical project decisions** — choices that are locked, specific, and should persist across sessions.

**Decision indicators:**
- "We'll go with..."
- "Lock that in..."
- "The design is..."
- "Approved..."
- Specific numbers, dimensions, constraints, or parameters
- Architectural choices between alternatives
- Policy or governance rules
- Corrections to previous decisions

**NOT decisions (do not extract):**
- Open questions or explorations
- Tentative discussions ("maybe we could...")
- Commander asking for options (until one is selected)
- Background research or explanations
- Repeated/duplicate content already in CORE_VM.md

### Step 3: Cross-Reference Against Current VM

Before including a decision in the delta, verify it is NOT already present in CORE_VM.md. If a decision modifies or supersedes an existing entry, note the change explicitly (e.g., "Revised biomass output from X to Y").

### Step 4: Format Delta Output

Produce the delta as a **markdown code block** with this exact format:

**Filename suggestion:** `VM_DELTA_[TOPIC]_[YYYYMMDD]-[HHMM].md`

```markdown
## DELTA BEGIN

[YYYY-MM-DD] First canonical decision — specific, declarative, permanent.

[YYYY-MM-DD] Second canonical decision — one per entry, blank line between.

[YYYY-MM-DD] Third canonical decision — include numbers, names, constraints.

## DELTA END
```

**Formatting rules:**
- `## DELTA BEGIN` and `## DELTA END` markers are mandatory
- One decision per line
- Date prefix in `[YYYY-MM-DD]` format
- Blank line between each decision entry
- Declarative past tense voice: "Established...", "Locked...", "Adopted...", "Defined...", "Approved...", "Formalized..."
- Be specific — numbers, dimensions, names, citations, not vague summaries
- No commentary, rationale, questions, or narrative — just the decision
- No markdown formatting within decision lines (no bold, no bullets, no headers)

### Step 5: Report to Commander

After outputting the delta, tell Commander:

1. **Decision count**: "Extracted N decisions"
2. **Topic summary**: One-line description for the delta filename
3. **Conflicts**: Any decisions that modify existing CORE_VM.md entries
4. **Suggested filename**: `VM_DELTA_[TOPIC]_[YYYYMMDD]-[HHMM].md`

Commander will then deliver the delta to Agent B (Claude Code) for ingestion into CORE_VM.md and Git commit.

---

## If Retrieval Fails

If you cannot fetch the GitHub URL (error, timeout, "cannot load external URLs"):

1. **STOP** — do not attempt workarounds
2. Tell Commander: "Lane transition detected — retrieval is disabled in this thread"
3. Recommend: "Start a new Chat Type A session and paste this work order as the first message"
4. If Commander provides CORE_VM.md content as pasted text, you may proceed with that as the reference

---

## Quality Gates

Before finalizing the delta output, verify:

- [ ] Every entry is a genuine canonical decision (not exploration or discussion)
- [ ] No duplicates of existing CORE_VM.md content
- [ ] All numbers and constraints match what was actually decided (not rounded or paraphrased)
- [ ] Date prefixes are accurate (date the decision was made, not today's date, unless made today)
- [ ] DELTA BEGIN / DELTA END markers are present
- [ ] Blank line between every decision entry

---

## Coordination with Agent B

After Commander delivers the delta to Claude Code, Agent B will:

1. Save the delta file to NAS (`Z:\SE_T1\GOVERNANCE\Claude Atlas Virtual Memory\02_VM_DELTAS\2026-02\`)
2. Save to GitHub clone (`C:\Users\Gary\Heber-Campus-VM\02_VM_DELTAS\2026-02\`)
3. Append decisions to CORE_VM.md with source attribution
4. Update REBUILD_INDEX.md with commit hash
5. Push to GitHub
6. Sync NAS REBUILD_INDEX

The delta you produce here is the **input** to that pipeline. Your job is extraction and formatting only.

---

*Last Updated: 2026-02-10*
