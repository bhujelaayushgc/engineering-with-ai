---
name: draft-email
description: Transform structured engineering artifacts into concise, professional, traceable async communication drafts.
---

# Purpose

Transform structured engineering artifacts into communication-oriented email drafts.

This skill converts:
- RFCs
- ADRs
- PLAN summaries
- DISCUSSION summaries
- STATUS updates
- operational updates

into:
- concise
- structured
- professional
- async-friendly
- traceable email drafts

This skill intentionally separates:
- communication formatting
from
- reasoning
and
- decision-making

Email is a communication layer, NOT the source of truth.

---

# Responsibilities

This skill is responsible for:

- drafting structured emails
- converting artifacts into async-friendly communication
- preserving traceability references
- preserving discussion continuity
- preserving implementation context
- summarizing operationally relevant information
- adapting tone to communication purpose
- adapting communication structure to audience context
- producing deterministic communication drafts

---

# Non-Responsibilities

This skill must NOT:

- invent architectural decisions
- invent implementation plans
- invent discussion outcomes
- silently reinterpret RFCs/ADRs/PLAN artifacts
- finalize unresolved decisions
- mutate source artifacts
- generate implementation code
- perform primary architectural reasoning
- fabricate consensus
- become the canonical architecture source

This skill formats communication only.

---

# When To Use

Use this skill when:

- sharing RFCs for review
- sharing ADRs for visibility
- sharing implementation updates
- sharing operational updates
- sharing discussion summaries
- sharing milestone progress
- requesting review/alignment
- preserving async collaboration continuity

---

# When NOT To Use

Do NOT use this skill:

- for implementation planning
- for architectural decision-making
- for execution decomposition
- for unresolved reasoning exploration
- for historical discussion preservation

Use:
- DISCUSSION for historical reasoning
- PLAN for implementation planning
- ADR for finalized decisions
- RFC for proposal review

---

# Inputs

Expected inputs may include:

- RFC artifacts
- ADR artifacts
- PLAN summaries
- DISCUSSION summaries
- STATUS updates
- operational updates
- implementation updates
- rollout updates

Preferred invocation style:

```txt
Draft email for recommendation persistence RFC review
```

or

```txt
Draft implementation update email for recommendation-system
```

---

# Required Context Sources

This skill should prioritize:

```txt
Source artifact
    ↓
Related PLAN artifacts
    ↓
Accepted ADRs
    ↓
Relevant RFCs
    ↓
Relevant DISCUSSION artifacts
```

Source artifacts remain authoritative.

---

# Email Draft Areas

This skill should attempt to define and synthesize:

---

## 1. Communication Purpose

Clearly identify:
- why the email exists
- what outcome is expected
- what context recipients need

---

## 2. Context Summary

Summarize:
- relevant implementation context
- relevant operational context
- relevant discussion context

Concise and operationally relevant.

---

## 3. Main Content

Present:
- proposal summary
- implementation update
- operational update
- discussion summary
- review request
- blocker visibility

depending on communication purpose.

---

## 4. Decisions / Status

Clearly identify:
- finalized decisions
- unresolved concerns
- implementation status
- operational blockers

Must preserve certainty levels accurately.

---

## 5. Requested Actions

Clearly identify:
- review expectations
- feedback requests
- alignment requests
- follow-up expectations
- deadlines if explicitly provided

---

# Communication State

Communication drafts may exist in different styles:

- engineering discussion email
- RFC review email
- ADR visibility email
- implementation update email
- operational status email
- escalation/blocker email

This skill should adapt communication structure without mutating source meaning.

---

# Required Output

This skill must produce a deterministic email draft.

The draft should include:

---

## 1. Subject

Clear and traceable.

---

## 2. Context

Concise operational or implementation context.

---

## 3. Main Communication

Primary update, proposal, request, or summary.

---

## 4. Decisions / Status

Relevant finalized decisions, unresolved concerns, or implementation status.

---

## 5. Requested Actions

Review requests, feedback requests, or follow-up expectations.

---

# Artifact Rules

This skill does NOT generate canonical engineering artifacts.

Emails are communication layers only.

However:
- generated emails may reference canonical artifacts
- generated emails should preserve traceability
- generated emails should avoid becoming hidden architecture sources
- important reasoning should remain in canonical artifacts, not only in email threads

---

# Behavioral Rules

## Communication Over Reasoning

This skill should:
- communicate clearly
- preserve source meaning
- remain concise
- remain operationally useful

This skill must NOT:
- invent architectural reasoning
- reinterpret finalized decisions
- silently mutate source meaning
- fabricate alignment

---

## Explicitness Over Assumption

If source artifacts contain ambiguity:
- preserve ambiguity explicitly
- avoid fabricated certainty
- avoid rewriting unresolved concerns

Example:

```txt
Recommendation archival lifecycle remains under review.
Final migration sequencing has not yet been finalized.
```

---

## Related Artifact Awareness

If related artifacts exist, the draft may reference them when operationally useful.

Examples:
- related RFCs
- related ADRs
- related PLAN artifacts
- related DISCUSSION artifacts

References should:
- improve traceability
- reduce duplicate explanations
- preserve async continuity

---

## Context Compression

Emails should:
- preserve operational relevance
- remain concise
- reduce unnecessary conversational detail

Avoid:
- giant historical summaries
- excessive implementation detail
- hidden architectural reasoning

Communication synthesis should optimize for async readability.

---

## Preserve Source Integrity

Source artifacts remain authoritative.

This skill must:
- preserve source meaning
- preserve certainty levels
- preserve unresolved concerns accurately

Avoid silent communication drift.

---

## Audience Awareness

Communication should adapt appropriately for:
- engineering discussions
- architecture review
- operational updates
- async collaboration
- implementation coordination

without mutating factual meaning.

---

## Async Continuity Awareness

Emails should help preserve:
- discussion continuity
- review continuity
- implementation continuity
- operational visibility

without requiring recipients to reconstruct hidden context manually.

---

# Failure Behavior

If insufficient source context exists:

- identify missing artifacts explicitly
- identify unresolved ambiguity
- avoid fabricated communication certainty

Do NOT fabricate conclusions or alignment.

Example:

```txt
No finalized ADR exists for recommendation persistence lifecycle.
Email drafting cannot reliably proceed.
```

---

# Output Style

Outputs should be:

- concise
- professional
- deterministic
- async-friendly
- operationally aware
- traceable

Avoid:
- excessive prose
- vague communication
- fabricated certainty
- hidden architectural reasoning

---

# Example Invocation

```txt
Draft email for recommendation persistence RFC review
```

---

# Example Output Structure

```txt
Subject
Context
Main Communication
Decisions / Status
Requested Actions
```

---

# Important Principles

- communication after reasoning
- traceability over conversational convenience
- explicit ambiguity over fabricated certainty
- concise operational clarity over verbose discussion
- source integrity over communication convenience

---

# Long-Term Goal

Provide stable, repeatable, high-quality async engineering communication drafting for long-running AI-assisted engineering workflows while preserving traceability, operational clarity, and source integrity.