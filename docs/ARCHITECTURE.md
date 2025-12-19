# Cosmos Workflow Engine - Architecture & Change Log

Core workflow orchestrator and autonomous agent execution framework.


## [2025-12-17 15:29] - fix(parser): handle unescaped markdown JSON codeblocks cleanly
- Stripped leading/trailing backticks and sanitized raw string payloads.

## [2025-12-17 21:41] - fix(timeout): add execution dead-mans-switch for stuck tool processes
- Killed orphan sub-processes exceeding 120s execution window.

## [2025-12-19 10:42] - perf(tokens): add fast token counting utility using tiktoken
- Pre-calculated prompt sizes to optimize window utilization.
