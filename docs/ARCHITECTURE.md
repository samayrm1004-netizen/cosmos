# Cosmos Workflow Engine - Architecture & Change Log

Core workflow orchestrator and autonomous agent execution framework.


## [2025-12-17 15:29] - fix(parser): handle unescaped markdown JSON codeblocks cleanly
- Stripped leading/trailing backticks and sanitized raw string payloads.

## [2025-12-17 21:41] - fix(timeout): add execution dead-mans-switch for stuck tool processes
- Killed orphan sub-processes exceeding 120s execution window.

## [2025-12-19 10:42] - perf(tokens): add fast token counting utility using tiktoken
- Pre-calculated prompt sizes to optimize window utilization.

## [2025-12-19 22:14] - feat(planner): support dynamic step retry on transient failures
- Added exponential backoff policy for flaky external tool invocations.

## [2025-12-23 15:41] - perf(tokens): add fast token counting utility using tiktoken
- Pre-calculated prompt sizes to optimize window utilization.

## [2025-12-25 18:55] - docs(arch): add sequence diagram for subagent dispatch mechanism
- Outlined communication protocol between coordinator and workers.

## [2025-12-25 19:36] - fix(runner): prevent deadlock in circular dependency resolution
- Added topological sort cycle detection with clear error traceback.
