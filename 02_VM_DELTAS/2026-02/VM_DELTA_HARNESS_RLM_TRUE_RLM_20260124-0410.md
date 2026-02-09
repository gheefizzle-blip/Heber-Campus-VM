## DELTA BEGIN

[2026-01-22] The RLM engine was formally determined to be operating in a RAG-style prompt-stuffing pattern and not a true MIT-style Recursive Language Model, based on empirical harness evidence showing 200K+ token prompts and immediate rate limiting.

[2026-01-22] A decision was made to pause further harness runs until the engine architecture was corrected to a true MIT-style RLM pattern to prevent unnecessary token expenditure.

[2026-01-23] The RLM engine was rewritten to implement a true MIT-style Recursive Language Model, enforcing tool-based document navigation with bounded snippet retrieval and prohibiting full document injection into prompt context.

[2026-01-23] Environment-configurable hard caps were introduced for RLM execution, including maximum context tokens, documents accessed, snippets retrieved, snippet size, recursion depth, and tool call count.

[2026-01-23] Token estimation using tiktoken was implemented in the RLM engine to provide prompt token estimates for downstream throttle and observability systems.

[2026-01-23] A server-side citation collection system was implemented, producing structured citation objects in the API response payload instead of narrative-only references.

[2026-01-23] Structured citations were standardized to include doc_id, path, category, section identifier, bounded excerpt, and confidence level, and are now returned as an array in all RLM query responses.

[2026-01-23] The harness smart throttle system was corrected to use prompt_tokens_est as the primary throttle signal, with tokens_used as fallback, ensuring throttle effectiveness even during RATE_LIMIT responses.

[2026-01-23] A critical defect in the throttle ledger sliding window was identified and fixed by enforcing script-scope persistence and UTC-normalized timestamps, enabling accurate token window accumulation.

[2026-01-23] Verification confirmed that tokens_window and peak_window_tokens now accumulate and decay correctly according to the 60-second sliding window design.

[2026-01-24] Test Harness Run 004 achieved a measured 80 percent pass rate (16 of 20 tests passing), representing a validated operational RLM system with bounded token usage and structured citations.

[2026-01-24] Remaining non-pass harness results were formally attributed to corpus gaps and document accessibility issues rather than engine or harness defects.

[2026-01-24] A baseline strategy was established to complete the Claude-based RLM implementation to a >=90 percent pass rate before conducting comparative evaluation against OpenAI, Gemini, Grok, or local agent implementations.

## DELTA END
