# Differentiation — Qwen-Code Pack

## What This Pack Adds vs Upstream

| Capability | Upstream README | This Pack |
|---|---|---|
| Host instructions for AI agents | No (CLI docs only) | Yes — AGENTS.md + CLAUDE.md |
| Pre-flight smoke check | No | Yes — smoke_check.md |
| Boundary permission gates | No | Yes — boundary_check.md + 04_BOUNDARY_RISK_CARD.md |
| Failure recovery steps | No | Yes — failure_check.md + 03_PITFALL_LOG.md |
| Top-3 actionable pitfalls | No | Yes — 03_PITFALL_LOG.md (first section) |
| Prompt preview before install | No | Yes — 01_PROMPT_PREVIEW.md |
| Independent eval harness | No | Yes — full 06_EVALS/ suite |
| Upstream risks documented | Generic install notes only | Risk-first: 9 pitfalls with severity + stop conditions |
| Host compatibility check | No | Yes — Pitfall 1 targets config-dir install risk |

## Why This Doramagic Pack Is Different

The upstream qwen-code README explains what qwen-code is and how to install it. It does not tell an AI agent how to behave responsibly with it. This pack fills that gap:

- **For the agent:** boundary rules, permission gates, and verification checklists before touching external tools
- **For the evaluator:** reproducible smoke, boundary, and failure evals that produce pass/fail signals
- **For the user:** pitfall log with specific recovery steps so a blocked agent does not go silent

## What This Pack Deliberately Does Not Do

- Not an official mirror of QwenLM/qwen-code
- Not a generic starter template
- Not an awesome list or resource collection
- Not an SEO backlink repo
- Not a production safety guarantee

## Existing GitHub Assets Found

- Official docs: https://github.com/QwenLM/qwen-code
- Official upstream README covers install and usage
- Release and issue history expose failure modes that a quickstart rarely packages as recovery rules

## Source Attribution

This pack was assembled by [Doramagic](https://doramagic.ai) as a portable capability bundle for QwenLM/qwen-code. It is independent and not affiliated with or endorsed by QwenLM/qwen-code unless explicitly stated.
