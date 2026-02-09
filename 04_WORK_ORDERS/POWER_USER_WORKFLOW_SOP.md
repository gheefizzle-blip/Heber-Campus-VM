# Heber Campus Virtual Memory Extraction — Power User Workflow SOP

**Classification:** Internal Operating Procedure  
**Effective Date:** 2026-02-08  
**Owner:** Operations / Protocol Engineering  
**Status:** Formalized Best Practice

---

## Executive Summary

This SOP codifies session management for multi-LLM orchestrated workflows that combine:
- Virtual Memory extraction (GitHub canonical reads)
- Document artifact generation (PDF, DOCX, markdown)
- Governance continuity (cross-chat referencing)
- Multi-system integration (NAS ↔ Git ↔ local files)

**Core Principle:** File generation and external retrieval are orthogonal capabilities in constrained environments. Proper session pipelining eliminates silent capability loss.

---

## Session Classification

### Chat Type A: VM Extraction (Retrieval-Heavy)
**Purpose:** Load canonical VM, scan chat thread, generate append-only deltas

**Constraints:**
- No file generation before extraction
- No Python tool invocation
- No sandbox execution
- No NAS references in prompt context

**Execution Lane:** Lane 1 (unrestricted retrieval enabled)

**Steps:**
1. Start fresh chat
2. Paste WORK ORDER HCV-VM-EXTRACT-002 verbatim as first message
3. Say: "Execute HCV-VM-EXTRACT-002"
4. Wait for delta output only
5. Copy delta into local NAS directory manually
6. Do NOT attempt CORE_VM.md append in this chat

### Chat Type B: Document Production (Mutating-Heavy)
**Purpose:** Draft, refine, generate artifacts (PDF, DOCX, markdown, reports)

**Constraints:**
- No external GitHub raw URL reads
- No assumption of prior canonical access
- No VM extraction in same chat
- Treat file generation as terminal for retrieval

**Execution Lane:** Lane 2 (write-enabled, retrieval disabled)

**Steps:**
1. Prepare all reference documents (copy CORE_VM.md from NAS if needed)
2. Paste reference content into chat if external URLs are needed
3. Draft and refine text
4. Confirm content
5. Generate file as final step
6. Stop. Move to Chat Type C for next task.

### Chat Type C: Engineering / Design (Read-Only Drafting)
**Purpose:** Conceptual design, governance language, architecture planning

**Constraints:**
- Text-only output
- No file generation
- No external retrieval
- No Python execution

**Steps:**
1. Draft all governance language, architecture decisions, policy statements
2. Iterate until locked
3. Only when finalized, move to Chat Type B for document generation
4. Do NOT generate files in this chat

---

## Critical Boundaries (Non-Negotiable)

### Boundary 1: VM Extraction Must Be Isolated
**Rule:** Never execute VM extraction in a chat that contains file generation.

**Why:** Lane transition is irreversible and prevents subsequent delta extraction.

**Operational Reality:**
- PDF generation → Lane 2 (retrieval disabled)
- Once in Lane 2, all subsequent GitHub reads fail
- No escape without new chat session

**Compliance:**
- VM extraction = dedicated Chat Type A session
- Document generation = separate Chat Type B session
- Cross-reference via NAS paths, not URL sharing

### Boundary 2: File Generation Is Terminal for Retrieval
**Rule:** After requesting a file (PDF/DOCX/any generated output), assume retrieval is gone.

**Consequence:**
- Do not expect new GitHub reads in that chat
- Do not attempt new VM extracts in that chat
- Move all subsequent work to new sessions

### Boundary 3: Declare Intent Before Crossing Lanes

**Pattern (Before Any Mutating Action):**

```
[Action you want to take]

Before I do this, confirm:
- Will this disable external retrieval? (Y/N)
- Should I warn you before proceeding? (Y/N)
```

If yes to either → I will recommend session boundary.

---

## Operational Checklist: VM Extraction (Type A Chat)

Use this before every HCV-VM-EXTRACT-002 execution:

- [ ] Fresh chat session (do not reuse prior chats)
- [ ] WORK ORDER pasted as first message
- [ ] No prior file generation in this chat
- [ ] No PDF/DOCX requests in this chat
- [ ] No Python tool invocation yet
- [ ] Confirm "Execute HCV-VM-EXTRACT-002" is the immediate follow-up
- [ ] Expect output: Delta file (markdown code block) + SENSITIVE file (if needed)
- [ ] Save deltas to NAS manually post-extraction
- [ ] Do NOT append CORE_VM.md in this chat
- [ ] Move to separate chat for CORE_VM.md updates (type B)

---

## Operational Checklist: Document Production (Type B Chat)

Use this before generating any deliverable file:

- [ ] All reference materials copied into chat (or pasted from NAS)
- [ ] No external GitHub reads attempted
- [ ] Draft completed and locked
- [ ] Content approved by governance review
- [ ] File generation requested as final step in chat
- [ ] Output downloaded and saved to NAS
- [ ] Chat marked as terminal (no further retrieval work in this session)
- [ ] Next task moves to new chat session

---

## Workflow Pattern: Complete Multi-Step Project

**Scenario:** Full VM delta extraction + CORE_VM.md update + snapshot generation + GitHub push

### Phase 1: Extract Delta (Chat A - Type A)
```
New chat → Paste work order → Execute → Get delta file → Copy to NAS
```

### Phase 2: Create Snapshot & Update Index (This Chat or New Chat B)
```
New chat (Type B or local execution) → Snapshot markdown → Index update → Git commit
```

### Phase 3: Generate Governance Document (Chat C - Type B)
```
New chat → Draft policy language → Refine → Generate PDF → Save to NAS
```

### Phase 4: Create Visual Summary (Chat D - Type B)
```
New chat → Design tables/diagrams → Refine → Export → Save to NAS
```

**Key:** Each major capability shift = new chat session.

---

## Guardrails: What NOT to Do

❌ **Do NOT:** Start VM extraction, then ask for a PDF in the same chat  
❌ **Do NOT:** Invoke Python tools before VM extraction  
❌ **Do NOT:** Paste CORE_VM.md, then ask for file generation, then expect new GitHub reads  
❌ **Do NOT:** Reference NAS paths in work order context before retrieval is locked  
❌ **Do NOT:** Assume retrieval survives file generation  

---

## When Lane Transition Happens (And What To Do)

**You will know if you've crossed a boundary when:**

1. You request a GitHub read
2. System returns:  
   ```
   ERROR: Cannot load external URLs in this environment
   ```

**If this happens:**
- Do NOT continue in same chat
- Do NOT try workarounds
- Do NOT assume it will resolve
- **Action:** Start new Chat Type A session with fresh work order

---

## Why This SOP Exists

The underlying platform (OpenAI's Claude/GPT lane system) enforces implicit constraints:

- Lane 1: Retrieval enabled, file writing forbidden
- Lane 2: File writing enabled, retrieval disabled
- Transition: Automatic, irreversible, silent

This SOP makes that implicit system explicit, giving you:

- Predictable session behavior
- No silent capability loss
- Operator control over lane selection
- Deterministic, reproducible workflows

---

## Success Metrics

✅ **This SOP is working if:**
- VM extracts always complete on first attempt
- No "cannot load external URL" errors in work-order chats
- File generation never blocks downstream retrieval
- Each task uses the correct chat type first time
- Cross-chat referencing works reliably

❌ **This SOP failed if:**
- You need to restart a chat mid-work
- Retrieval unexpectedly disappears
- You're switching between chats more than the pipeline requires
- File generation and extraction happen in the same session

---

## Questions & Exceptions

**Q: What if I need to reference CORE_VM.md in a document-generation chat?**  
A: Copy the relevant section from NAS into the document chat as text. Do not try to load the GitHub URL.

**Q: What if extraction takes two chats?**  
A: Use Chat Type A → extract delta → save to NAS → if you need to extract from same chat again, start new Type A chat.

**Q: Can I do engineering design and document production in the same chat?**  
A: Yes. Both are read-only or write-only. Just do design first (draft only), then generate file as final step (terminal action).

**Q: What about quick fixes or small edits?**  
A: If it requires external retrieval, new chat. If it requires file generation, assume terminal. When in doubt, new session.

---

## Feedback & Updates

This SOP will be updated when:
- OpenAI exposes explicit session modes
- Lane transitions become visible/reversible
- New tools change retrieval/write boundaries
- Operational experience reveals edge cases

Last Updated: **2026-02-08**  
Next Review: **2026-03-08**

---

