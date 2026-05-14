# AGENTS.md — Qwen-Code Capability Pack

## Goal

Use this pack to help an AI coding agent work with `QwenLM/qwen-code` safely and verifiably.

---

## When To Load — Concrete Examples

Load this pack when any of these apply:

| Scenario | Why This Pack Helps |
|---|---|
| User asks "can you use qwen-code to fix this bug?" | Provides boundary rules and smoke check before claiming it works |
| User wants the agent to install or run qwen-code | Forces verification step; prevents unverified install claims |
| Agent is about to call external tools / network / filesystem | Enforces permission gate; names the specific boundary from risk card |
| Agent's first eval step fails | Points directly to pitfall log with recovery steps |
| User is evaluating qwen-code for their team | Gives reproducible acceptance checks, not just vibes |
| Agent encounters an unclear setup step | Pitfall log has the specific failure mode documented |

Do NOT load this pack if:
- The agent is already past setup and has passed smoke checks
- The task has nothing to do with qwen-code or terminal coding agents

---

## How To Use — Step By Step

### Step 1: Load the host instructions
```
Copy the full text of AGENTS.md into the agent's context.
```

### Step 2: Run the smoke check conceptually
```
Using this pack, identify the first safe verification step for qwen-code.
Do not call external tools unless explicitly approved.
```

### Step 3: If smoke check passes, proceed with the task
- State the task clearly
- Identify required tools (browser, network, filesystem, credentials)
- Ask for explicit user approval before any risky action
- Reference the boundary risk card before touching external systems

### Step 4: If smoke check fails or agent is blocked
1. Open `03_PITFALL_LOG.md`
2. Find the matching failure mode in the top 3 pitfalls
3. Apply the recovery step
4. If still blocked, stop and report

---

## Allowed / Disallowed Actions

### Allowed
- Read files in this pack
- Ask clarifying questions before acting
- Produce a plan and wait for confirmation
- Run only user-approved verification commands
- Record new failure patterns in the pitfall log format

### Disallowed
- Claim official endorsement — this is an independent Doramagic pack
- Access secrets by default
- Send messages, publish, purchase, delete, or modify external systems without explicit approval
- Claim qwen-code is installed or working without passing an acceptance check

---

## Failure Recovery Table

| Failure Mode | Symptom | Recovery Step | When To Stop |
|---|---|---|---|
| Config pitfall | Installs to user AI config dir; agent behavior changes | Stop. List files written. Provide uninstall/rollback steps before continuing. | Host compatibility unclear |
| Assumption pitfall | Agent claims capability without evidence | Force eval run before stating outcome. Add the failing assumption to pitfall log. | No eval evidence |
| Maintenance pitfall | No recent commits / releases visible | Downgrade trust level. Do not claim active maintenance. | User expects active support |
| Sandbox pitfall | No demo / install evidence available | Require user to run in an isolated environment first. | Production environment requested |
| Boundary pitfall | Agent proceeds without asking | Stop. Re-load AGENTS.md with explicit permission gate. | Agent ignores permission ask |

---

## Verification Checklist

Before the agent claims success:

- [ ] Read `00_QUICK_START.md`
- [ ] Ran smoke check (conceptually or literally)
- [ ] Checked `03_PITFALL_LOG.md` for relevant failure modes
- [ ] Named the specific boundary from `04_BOUNDARY_RISK_CARD.md` before any external call
- [ ] Did not claim official endorsement

---

## Source / Risk Reminder

This is an independent Doramagic pack. See `SOURCE_MAP.md` for evidence and source links. This pack is not affiliated with or endorsed by QwenLM/qwen-code unless explicitly stated.
