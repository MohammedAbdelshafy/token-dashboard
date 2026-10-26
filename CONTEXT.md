---
type: repository
status: active
owner_repo: MohammedAbdelshafy/token-dashboard
product_name: Token Dashboard
source_of_truth: https://github.com/MohammedAbdelshafy/token-dashboard
---

# Token Dashboard CONTEXT

One job: summarize local Claude Code session usage and cost estimates without sending the user's prompt history to a remote service.

## Inputs
- Setup, data paths and safety notes: [README](README.md)
- CLI: [cli.py](cli.py)
- Tests: [tests](tests/)
- Price settings: [pricing.json](pricing.json)

## Process
1. Read session JSONL files from the configured local directory.
2. Calculate token/cost estimates using the local pricing configuration.
3. Display per-project and per-session summaries.
4. Keep the HTTP server bound to localhost unless a security review explicitly approves other exposure.
5. Never alter the source transcripts.

## Output
A local dashboard and summaries of recorded sessions.

## Check
Run the documented tests and verify that source transcripts remain unchanged and no API calls are made to upload user prompt content. The result depends on the local transcript data and pricing configuration.
