---
name: create-adr
description: Document finalized architectural or operational decisions as deterministic, durable, authoritative ADR artifacts.
---

# Purpose

Document finalized architectural, operational, or workflow decisions as authoritative ADR (Architecture Decision Record) artifacts.

This skill exists to:
- preserve accepted decisions
- preserve rationale
- preserve tradeoffs
- preserve consequences
- preserve architectural history
- provide durable decision traceability

ADRs represent:
- committed decisions
- authoritative constraints
- accepted architectural direction

ADRs intentionally follow:
- exploration
- RFC review
- finalized decision alignment

---

# Responsibilities

This skill is responsible for:

- documenting finalized decisions
- documenting rationale
- documenting tradeoffs
- documenting consequences
- documenting constraints introduced by decisions
- preserving architectural history
- preserving operational implications
- producing deterministic ADR artifacts

---

# Non-Responsibilities

This skill must NOT:

- explore unresolved proposals
- reopen finalized decisions
- generate implementation tasks
- generate implementation plans
- silently reinterpret accepted decisions
- invent architectural rationale
- fabricate unresolved certainty
- generate speculative implementation details
- create implementation code

This skill records finalized decisions only.

---

# When To Use

Use this skill when:

- architectural decisions are finalized
- operational decisions are finalized
- workflow decisions are finalized
- review/alignment has completed
- implementation constraints need durable preservation
- architectural traceability is required
- future implementation must preserve constraints

---

# When NOT To Use

Do NOT use this skill:

- during early exploration
- during unresolved proposal discussions
- before review completion
- for implementation planning
- for execution decomposition
- for isolated coding questions

Use RFCs for unresolved proposals.

---

# Inputs

Expected inputs may include:

- finalized decisions
- accepted proposal outcomes
- accepted RFC conclusions
- architectural constraints
- operational decisions
- workflow decisions
- implementation implications
- existing ADRs
- relevant PLAN artifacts
- relevant discussions

Preferred invocation style:

```txt
Create ADR for recommendation snapshot persistence
```

or

```txt
Generate ADR for worker retry strategy
```

---

# Required Context Sources

This skill should prioritize:

```txt
Accepted RFC outcomes
    ↓
PLAN
    ↓
Accepted ADRs
    ↓
Relevant DISCUSSIONS
```

Existing ADRs remain authoritative constraints.

---

# ADR Areas

This skill should attempt to define and synthesize:

---

## 1. Decision Context

Define:
- why the decision was required
- what constraints existed
- what problem was being solved

---

## 2. Finalized Decision

Clearly document:
- the accepted decision
- the authoritative direction
- the implementation constraint introduced

Mandatory section.

---

## 3. Rationale

Document:
- why the decision was accepted
- why alternatives were rejected
- important influencing constraints

---

## 4. Tradeoffs

Identify:
- operational tradeoffs
- scalability tradeoffs
- complexity tradeoffs
- maintainability tradeoffs
- ownership implications

---

## 5. Consequences

Identify:
- implementation implications
- operational implications
- future constraints
- migration implications
- compatibility implications

---

## 6. Decision Scope

Explicitly identify:
- systems impacted
- workflows impacted
- operational boundaries
- ownership boundaries
- implementation areas constrained by this decision

---

## 7. Related Decisions

Identify:
- dependent ADRs
- superseded ADRs
- related RFCs
- related PLAN artifacts

Where relevant.

---

# ADR State

ADRs may exist in different states:

- proposed
- accepted
- superseded
- deprecated

Accepted ADRs are authoritative.

---

# Required Output

This skill must produce a deterministic ADR artifact.

The artifact should include:

---

## 1. Context

Why the decision was required.

---

## 2. Decision

The finalized accepted decision.

Mandatory section.

---

## 3. Rationale

Why this decision was accepted.

---

## 4. Tradeoffs

Tradeoffs introduced by the decision.

---

## 5. Consequences

Implementation and operational implications.

---

## 6. Re-Evaluation Conditions

Where applicable, identify:
- scaling thresholds
- operational triggers
- architectural triggers
- organizational changes
- migration completion points

that may justify future decision re-evaluation.

---

## 7. Status

ADR lifecycle status.

Examples:
- proposed
- accepted
- superseded
- deprecated

Mandatory section.

---

# Artifact Rules

This skill must generate:

```txt
ADR-001-<topic>.md
```

Example:

```txt
ADR-001-product-snapshotting.md
```

ADR artifacts:
- are authoritative
- are durable
- preserve architectural history
- constrain future implementation
- must not be silently reinterpreted

---

# Behavioral Rules

## Decision Integrity

This skill should:
- preserve finalized decisions accurately
- preserve rationale explicitly
- preserve important tradeoffs

This skill must NOT:
- reopen finalized decisions
- silently reinterpret accepted constraints
- mutate architectural history

---

## Explicitness Over Assumption

If rationale or constraints are unclear:
- identify ambiguity explicitly
- avoid fabricated rationale

Example:

```txt
Operational rollback implications were not fully defined during decision acceptance.
```

---

## Related Artifact Awareness

If related artifacts exist, the skill should reference them when relevant.

Examples:
- related RFCs
- related ADRs
- related PLAN artifacts
- related DISCUSSION artifacts
- related TASKS artifacts

Related artifacts should:
- improve traceability
- preserve context continuity
- avoid duplicate reasoning

The skill should avoid referencing unrelated or stale artifacts.

---

## Context Compression

When ADR history becomes large:

- preserve authoritative decisions
- preserve supersession chains
- preserve operationally important rationale
- preserve important tradeoffs

Deprioritize:
- stale exploratory discussions
- abandoned proposal branches
- redundant historical detail

ADR synthesis should optimize for architectural traceability.

---

## Preserve Historical Integrity

ADRs represent durable architectural history.

This skill must:
- preserve historical continuity
- preserve supersession relationships
- preserve accepted constraints

Avoid silent architectural drift.

---

## ADR Mutation Constraints

Accepted ADRs should not be silently rewritten.

If architectural direction changes:
- create superseding ADRs
- preserve historical rationale
- preserve supersession traceability

Avoid retroactively rewriting architectural history.

---

# Failure Behavior

If insufficient context exists:

- identify missing rationale explicitly
- identify unresolved decisions
- identify missing review outcomes
- avoid fabricated architectural certainty

Example:

```txt
No finalized proposal outcome exists for recommendation regeneration lifecycle.
ADR creation cannot reliably proceed.
```

---

# Output Style

Outputs should be:

- deterministic
- authoritative
- concise
- structured
- operationally aware
- artifact-backed

Avoid:
- excessive prose
- speculative certainty
- unresolved proposal exploration
- implementation decomposition

---

# Example Invocation

```txt
Create ADR for recommendation snapshot persistence
```

---

# Example Output Structure

```txt
Context
Decision
Rationale
Tradeoffs
Consequences
Re-Evaluation Conditions
Status
```

---

# Important Principles

- finalized decisions over exploration
- architectural integrity over convenience
- deterministic synthesis over creativity
- durable history over transient reasoning
- explicit rationale over hidden assumptions
- visibility over hidden state

---

# Long-Term Goal

Provide stable, repeatable, high-quality architectural decision preservation for long-running AI-assisted engineering workflows while maintaining architectural integrity, historical traceability, and implementation continuity.