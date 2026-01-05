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

## [2025-12-29 16:07] - test(engine): add execution graph unit test suite
- Tested parallel branch resolution and early exit conditions.

## [2025-12-29 19:23] - fix(runner): prevent deadlock in circular dependency resolution
- Added topological sort cycle detection with clear error traceback.

## [2025-12-30 16:40] - perf(tokens): add fast token counting utility using tiktoken
- Pre-calculated prompt sizes to optimize window utilization.

## [2025-12-30 17:25] - chore: set up automated linting and formatting configuration
- Added ruff and black configurations for repository consistency.

## [2025-12-30 19:36] - perf(memory): implement LRU eviction for agent short-term buffer
- Bounded context token usage to prevent out-of-memory errors on long runs.

## [2025-12-30 21:24] - feat(core): initialize workflow execution graph engine
- Created foundational directed acyclic graph runner for autonomous tasks.

## [2026-01-02 15:21] - feat(storage): implement SQLite checkpointing for resumable workflows
- Allowed agents to persist intermediate state across restarts.

## [2026-01-02 21:52] - docs(quickstart): write introductory walkthrough and example usage
- Documented single-agent and multi-agent coordination setup.

## [2026-01-05 21:08] - refactor(tools): standardize tool output schema and status codes
- Normalized tool results into structured Result object.

## [2026-01-05 22:43] - feat(planner): support dynamic step retry on transient failures
- Added exponential backoff policy for flaky external tool invocations.
