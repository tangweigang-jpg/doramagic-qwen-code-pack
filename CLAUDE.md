# CLAUDE.md — Qwen-Code Pack for Claude Code

Use this file when Claude Code is your agent host. For other hosts, use `AGENTS.md`.

## Loading This Pack

At the start of a session, paste the full text of `AGENTS.md` into the conversation. This gives Claude Code the boundary rules, verification checklist, and failure recovery table for qwen-code.

## Runtime Rules

### Before Every Action
1. Restate the task in one sentence.
2. Check: does this require browser, network, filesystem, or credentials?
3. If yes: name the specific boundary from `04_BOUNDARY_RISK_CARD.md` and ask for explicit approval.
4. If the task involves qwen-code: run the smoke check mentally first — do not claim it works without evidence.

### Permission Protocol
- Never run `npm install -g @qwen-code/qwen-code@latest` without user approval.
- Never send data to external services without approval.
- Never modify host config directories without listing what will change and how to roll back.

### Verification Protocol
```
Did I:
- Read 00_QUICK_START.md?           [ ]
- Check 03_PITFALL_LOG.md?          [ ]
- Name the boundary before external call?  [ ]
- Avoided claiming official endorsement?   [ ]
```

### If Blocked or Fails
1. Open `03_PITFALL_LOG.md`.
2. Find the top 3 pitfalls — they are immediately actionable.
3. Apply the recovery step for the matching failure mode.
4. If unresolved: write the failure to `TEST_LOG.md` and report to user.

### What Not To Do
- Do not claim qwen-code is installed or working because it is in the PATH.
- Do not skip the boundary risk card when making tool calls.
- Do not say "this is the official qwen-code recommendation" — it is not.
- Do not fabricate evidence for capability claims.

## Key Files Reference

| File | Purpose |
|---|---|
| `00_QUICK_START.md` | One-paragraph outcome + install command |
| `01_PROMPT_PREVIEW.md` | Copyable prompt to experience the pack before installing |
| `03_PITFALL_LOG.md` | Top 3 actionable pitfalls + full log |
| `04_BOUNDARY_RISK_CARD.md` | Permissions, hard boundaries, stop conditions |
| `06_EVALS/smoke_check.md` | First verification to run before claiming success |
| `06_EVALS/boundary_check.md` | Confirms agent respects permission gates |
| `06_EVALS/failure_check.md` | Confirms agent can recover from install/step failure |
