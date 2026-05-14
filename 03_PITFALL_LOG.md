# Pitfall Log — Qwen-Code Pack

## Top 3 Actionable Pitfalls

These are the most likely failure modes. Check here first when something breaks.

---

### Pitfall 1: Installs to Host AI Config Directory

**Symptom:** Agent install command writes to `~/.claude/`, `~/.cursor/`, `~/.codex/`, or similar host config dirs.
**Likely cause:** qwen-code targets multiple AI hosts; its install script may modify host configuration.
**Recovery:** Stop. Run `ls -la ~/.claude/` and `~/.config/` to see what changed. Provide uninstall/rollback steps before continuing.
**When to stop:** Host compatibility is unclear, or rollback is not available.

---

### Pitfall 2: Capability Claim Without Evidence

**Symptom:** Agent states qwen-code "works" or "is installed" without running a verification command.
**Likely cause:** Assumption that package-on-PATH means capability-verified.
**Recovery:** Require the agent to run the actual skill or command and report the literal output. Do not accept "it seems to work."
**When to stop:** No eval evidence; user is making a production decision.

---

### Pitfall 3: No Sandbox / Install Evidence

**Symptom:** No demo has been run; agent cannot show actual output from qwen-code.
**Likely cause:** Upstream has `no_demo` flagged; verification was not completed before pack was assembled.
**Recovery:** Run in an isolated environment (tmpdir, container, VM). Do not use production config or credentials.
**When to stop:** User requests production use without isolation.

---

## Full Pitfall Index

| # | Pitfall | Severity | Status |
|---|---|---|---|
| 1 | Installs to host AI config dir | medium | top-3 |
| 2 | Capability claim without evidence | medium | top-3 |
| 3 | No sandbox / install evidence | medium | top-3 |
| 4 | Maintenance activity unknown | medium | known |
| 5 | Downstream validation risk found | medium | known |
| 6 | Security注意事项未确认 | medium | known |
| 7 | Scoring risk flagged | medium | known |
| 8 | Issue/PR response quality unknown | low | known |
| 9 | Release cadence unclear | low | known |

---

## Pitfall 4: Maintenance Activity Unknown

- **Severity:** medium
- **Evidence:** `last_activity_observed` is not recorded in upstream
- **Impact:** New, dormant, and active projects are mixed; recommendation trust degrades
- **Recovery:** Check GitHub for recent commits, releases, and issue/PR response time. Downgrade trust if >6 months no activity.
- **When to stop:** User expects active maintenance support

---

## Pitfall 5: Downstream Validation Risk Found

- **Severity:** medium
- **Evidence:** `downstream_validation.risk_items` flagged in upstream audit
- **Impact:** Page should not soft-pedal the risk finding
- **Recovery:** Route to security/permissions review queue before recommending
- **When to stop:** Risk is unresolved and user wants production use

---

## Pitfall 6: Security Notes Require Confirmation

- **Severity:** medium
- **Evidence:** `risks.safety_notes` — no sandbox install confirmed yet; downstream must verify
- **Impact:** User needs to know permission boundaries before install
- **Recovery:** Convert to explicit permissions checklist and security review prompt
- **When to stop:** Production environment requested without isolation

---

## Pitfall 7: Scoring Risk Flagged

- **Severity:** medium
- **Evidence:** `risks.scoring_risks` with `no_demo`; severity=medium
- **Impact:** Risk affects fitness for general user installation
- **Recovery:** Document in boundary card; confirm whether human review is needed
- **When to stop:** Human review not completed and user deploys

---

## Pitfall 8: Issue/PR Response Quality Unknown

- **Severity:** low
- **Evidence:** `issue_or_pr_quality=unknown`
- **Impact:** User cannot know if problems will get maintainer attention
- **Recovery:** Sample recent issues/PRs; note if none are answered
- **When to stop:** User needs guaranteed support

---

## Pitfall 9: Release Cadence Unclear

- **Severity:** low
- **Evidence:** `release_recency=unknown`; install commands may drift from code
- **Impact:** Docs and commands may be stale; user more likely to hit surprises
- **Recovery:** Verify latest release tag matches README install command
- **When to stop:** User wants bleeding-edge; install docs are >3 months old

---

## Doramagic Source Extract

Project: QwenLM/qwen-code
Summary: 9 potential pitfalls found; 3 are high-priority (top-3 above); 0 are blocking without user approval.
Last updated: 2026-05-14
