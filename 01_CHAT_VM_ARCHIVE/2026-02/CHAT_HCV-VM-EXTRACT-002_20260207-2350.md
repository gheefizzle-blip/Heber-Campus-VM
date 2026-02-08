# CHAT_HCV-VM-EXTRACT-002_20260207-2350

**Snapshot Timestamp:** 2026-02-07 23:50 UTC  
**Source:** ChatGPT Extraction (HCV-VM-EXTRACT-002)  
**Thread:** HCV-VM-EXTRACT-002  
**VM_VERSION:** 20260207-2350  
**Immutable:** Yes

---

## Media Handling Guidelines

### Facebook Share Links
- **Authentication Requirement:** Share links may still require login after generation
- **Handling Rule:** If video cannot be accessed without authentication, must be provided as direct uploaded media file (MP4/MOV format)
- **Purpose:** Enables transcription/analysis without authentication barriers

### iOS/Facebook Workflow Artifacts
- **Binary Property List (bplist) Artifact:** Apple binary format with file header "bplist00"
- **Content:** Contains metadata/pointers only, not playable video
- **Classification:** Non-media artifact
- **Action:** Request actual video file instead; do not attempt playback or analysis of bplist artifacts
