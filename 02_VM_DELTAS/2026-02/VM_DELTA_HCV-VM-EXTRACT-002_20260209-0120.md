## DELTA BEGIN

[2026-02-08] Canonical governance decision ratified establishing a Hybrid Architecture for project execution: a shared platform sandbox (SE_T1) for agents, templates, and tooling, with fully isolated per-project tenant roots for all client and project data, artifacts, and governance files.

[2026-02-08] Project onboarding pipeline formally adopted as a canonical operational doctrine, defining deterministic intake, validation, provisioning, execution, validation, release, and closeout phases, with no cross-project data access permitted at any stage.

[2026-02-08] Mandatory project identifier format formalized as PRJ-<CLIENT_SLUG>-<YYYY>-<NNNN>, enforced at intake and provisioning layers to prevent cross-project collision and enable deterministic routing, auditing, and archival.

[2026-02-08] Router authority formally designated as the sole component authorized to provision project tenants, create canonical governance artifacts (CTX, PRI, MANIFEST), apply access controls, generate cryptographic hashes, and emit PROJECT_READY lifecycle events.

[2026-02-08] Governance spine doctrine formalized requiring every project to instantiate three canonical artifacts at provisioning: Context Anchor (CTX), Project Reference Index (PRI), and Machine Manifest, with all subsequent execution bound to these artifacts.

[2026-02-08] Schema-per-project database isolation adopted as the default operational mode, with explicit allowance for database-per-project escalation for high-risk or high-sensitivity projects; mandatory project_id scoping enforced on all retrieval and write operations.

[2026-02-08] Risk-based validation gates codified requiring mandatory Agent R security validation for all projects classified as HIGH or CRITICAL risk prior to provisioning or execution.

[2026-02-08] Emergency project control doctrine established authorizing immediate PAUSE, FREEZE, or TERMINATE actions at the Router level to halt execution, preserve state, or initiate controlled shutdown in response to security, scope, or client-driven events.

[2026-02-08] Canonical JSON schema contracts ratified for project intake, project provisioning request, provisioning response, and project-ready event payloads, establishing machine-verifiable governance interfaces between orchestration, routing, and agent execution layers.

[2026-02-08] Operational separation rule reinforced: VM extraction, governance validation, and canonical memory mutation are retrieval-only activities and must remain isolated from sandboxed generation or execution environments.

## DELTA END
