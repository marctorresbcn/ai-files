# Handoff — {{task_title}}

> Title: one line that identifies the task unambiguously.
> Ex: "Refactor auth module", "Prototype Stripe SDK integration", "Fix pagination bug"

**Source session:** {{source_session}}  
**Purpose:** {{purpose_one_sentence}}  
**Pattern:** {{pattern}}

> Pattern: choose one:
> - Pure delegation — the source session does not need results back
> - Round trip — the new session should generate a return handoff with what was learned

---

## Context

> Only what the receiving agent needs to understand the situation.
> Do not copy what is already in other files — use pointers (see "Relevant files").
> Answer: where does this task come from? what decisions or prior work are relevant?
> 3-6 lines are usually enough. If you need more, the scope may not be clear.

**Last known state:** {{last_known_state}}

> Where the previous session left off exactly. What was attempted, what failed, where is the blocker.
> Ex: "I attempted to start the container but the DB handshake failed (see log in logs/docker.out)"
> Ex: "The /refresh endpoint returns intermittent 401. Suspected race condition in the refresh handler."
> This prevents the new agent from stumbling over the same issue before understanding where the problem was.

---

## Task

> What exactly needs to be done. Be specific: the agent does not have your mental context.
>
> Include:
> - What is expected as a result (feature, file, PR, analysis...)
> - Relevant technical constraints (versions, conventions, dependencies)
> - Edge cases or conditions the agent should consider
>
> Also include what is NOT in scope. This is as important as what is in scope:
> it prevents the agent from doing work that belongs to another session or task.

---

## Relevant files

> List files, documents, or resources the agent should read.
> Do not copy their contents here — use the path or link and let the agent read them.
>
> Ex:
> - `src/auth/index.ts` — main module to refactor
> - `docs/architecture.md` — context for the current architecture
> - github.com/org/repo/issues/42 — related issue
>
> If there are resources that MUST NOT be touched, state that explicitly.

---

## Decisions already made

> What is decided and should not be questioned in this session.
> Saves the agent time and prevents reopening closed debates.
>
> Ex:
> - Stack: Node.js + TypeScript (no changes)
> - New service port: 3001
> - Shared database for now, no schema changes
>
> If nothing is decided yet, remove this section.

---

## Suggested skills

> Skills the agent should invoke at the start of the session.
> This orients the tone and working conventions from the beginning.
>
> Ex:
> - `skill: diagnostics` — to analyze dependencies before touching code
> - `skill: typescript` — project conventions
> - `skill: bbq` — if the new session is planning-focused
>
> Remove this section if it does not apply.

---

## Expected output

> What this session should produce when finished. Be concrete.
> Always include a validation criterion: how does the agent demonstrate it is done successfully.
>
> Ex:
> - Branch `feat/auth-service` with the extracted service
> - PR opened against `main`
> - Validation: `npm run test:auth` green and linter clean
>
> For round trip pattern, specify that a new handoff.md is expected with:
> - What worked and what did not
> - Decisions made during the prototype
> - What was not captured in code but is relevant to the parent session

---

*Generated from {{source_session}} — saved in /tmp, disposable*
