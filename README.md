# qq_bot OpenAI Trace Samples

Public sample payloads exported from qq_bot admin trace pages.

## Samples

- `samples/run_1777082039566_23393023/index.json`
- `samples/run_1777082039566_23393023/round_01/input.json`
- `samples/run_1777082039566_23393023/round_01/output.json`
- `samples/run_1777082039566_23393023/round_02/input.json`
- `samples/run_1777082039566_23393023/round_02/output.json`
- `samples/run_1777082039566_23393023/round_03/input.json`
- `samples/run_1777082039566_23393023/round_03/output.json`
- `samples/run_1777082039566_23393023/round_04/input.json`
- `samples/run_1777082039566_23393023/round_04/output.json`

## Source

- Page: `https://qqbot-admin.liahuas.top/runs/run_1777082039566_23393023/trace`
- Run ID: `run_1777082039566_23393023`
- Trace ID: `runtrace_1777082039566_e0660bbd`

The trace contains four `llm.generation` spans. This sample exports all four
spans in `started_at` order.

Each round directory has:

- `input.json`: actual `wire_request` sent through the OpenAI Responses-style provider contract
- `output.json`: actual `wire_response` captured for that request
- `metadata.json`: sequence, `llm_call_id`, `agent_turn`, timestamps, model, and token usage

`index.json` lists all four rounds and their file paths.

Credential-like object keys are redacted. Token count fields and request/response
bodies are otherwise preserved.
