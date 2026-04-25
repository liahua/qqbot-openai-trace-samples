# qq_bot OpenAI Trace Samples

Private sample payloads exported from qq_bot admin trace pages.

## Samples

- `samples/run_1777082039566_23393023/openai_requests_first3.json`
- `samples/run_1777082039566_23393023/openai_requests_first3.min.json`

## Source

- Page: `https://qqbot-admin.liahuas.top/runs/run_1777082039566_23393023/trace`
- Run ID: `run_1777082039566_23393023`
- Trace ID: `runtrace_1777082039566_e0660bbd`

The trace contains four `llm.generation` spans. This sample exports the first
three spans in `started_at` order because the request was for the three triggered
OpenAI rounds. The fourth span is recorded in sample metadata under
`selection.excluded_llm_call_ids`.

Each item in `requests[]` has:

- `order`: sequence within the exported sample
- `input`: actual `wire_request` sent through the OpenAI Responses-style provider contract
- `output`: actual `wire_response` captured for that request
- run metadata such as `llm_call_id`, `agent_turn`, timestamps, model, and token usage

Credential-like object keys are redacted. Token count fields and request/response
bodies are otherwise preserved.
