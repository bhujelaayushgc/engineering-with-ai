---
name: create-rfc
description: Generate a structured proposal artifact for unresolved or review-required technical, architectural, operational, or workflow decisions.
---

# Purpose

Generate a structured RFC (Request For Comments) artifact for proposals requiring structured review before commitment or implementation.

This skill exists to:
- formalize unresolved proposals
- evaluate alternatives
- surface tradeoffs
- identify risks
- structure technical discussions
- prepare proposals for review and alignment

RFCs intentionally precede:
- finalized decisions
- ADR creation
- implementation commitment

RFCs are exploratory but structured.

---

# Responsibilities

This skill is responsible for:

- structuring unresolved proposals
- identifying alternatives
- identifying tradeoffs
- identifying risks
- surfacing implementation implications
- surfacing operational implications
- identifying review requirements
- identifying unresolved concerns
- documenting proposal rationale
- producing deterministic RFC artifacts

---

# Non-Responsibilities

This skill must NOT:

- finalize architectural decisions
- create ADRs
- silently resolve tradeoffs
- generate implementation tasks
- generate rollout sequencing
- mutate accepted ADRs
- invent missing architecture
- fabricate implementation certainty
- generate speculative implementation details
- create implementation code

This skill structures proposals under review only.

---

# When To Use

Use this skill when:

- a proposal requires review
- architectural direction remains unresolved
- multiple viable approaches exist
- tradeoffs require evaluation
- operational implications require discussion
- implementation direction needs alignment
- workflow/process changes require review
- migration strategy requires review
- cross-team alignment is needed
- unresolved concerns remain before implementation

---

# When NOT To Use

Do NOT use this skill:

- for finalized decisions
- for implementation planning
- for execution tracking
- for isolated coding questions
- for already accepted architecture
- for casual clarification discussions

Use ADRs for finalized decisions.

---

# Inputs

Expected inputs may include:

- proposal topic
- unresolved architectural concerns
- exploration artifacts
- implementation concerns
- operational concerns
- competing approaches
- migration concerns
- scaling concerns
- workflow proposals
- existing ADRs
- existing PLAN artifacts
- existing discussions

Preferred invocation style:

```txt
Create RFC for recommendation persistence strategy
```

or

```txt
Generate RFC for anonymous checkout session ownership
```

---

# Required Context Sources

This skill should prioritize:

```txt
EXPLORE
    ↓
PLAN
    ↓
Accepted ADRs
    ↓
Relevant DISCUSSIONS
```

Accepted ADRs remain authoritative constraints.

RFCs must NOT silently override accepted decisions.

---

# RFC Areas

This skill should attempt to define and synthesize:

---

## 1. Problem Statement

Clearly define:
- the unresolved problem
- why review is required
- why existing approaches are insufficient

---

## 2. Goals

Define:
- desired outcomes
- operational goals
- architectural goals
- workflow goals

---

## 3. Non-Goals

Explicitly identify:
- excluded scope
- deferred concerns
- unrelated work

Mandatory section.

---

## 4. Current Constraints

Identify:
- architectural constraints
- operational constraints
- migration constraints
- organizational constraints
- compatibility concerns

---

## 5. Proposed Approaches

Explore:
- primary proposal
- alternative proposals
- tradeoffs between approaches

Approaches should remain review-oriented.

---

## 6. Tradeoffs

Identify:
- complexity tradeoffs
- operational tradeoffs
- maintainability tradeoffs
- scalability tradeoffs
- ownership implications
- migration implications

---

## 7. Risks

Identify:
- operational risks
- rollout risks
- migration risks
- scaling risks
- architectural risks
- support risks

---

## 8. Open Questions

Explicitly identify:
- unresolved concerns
- pending validation
- unclear ownership
- review blockers
- required decisions

Mandatory section.

---

## 9. Review Requirements

Identify:
- stakeholders requiring review
- required technical validation
- operational validation needs
- dependency alignment requirements

---

# RFC State

RFCs may exist in different maturity levels:

- exploratory RFC
- architecture-aware RFC
- implementation-aware RFC
- review-ready RFC

RFCs remain proposals until decisions are finalized elsewhere.

---

# Required Output

This skill must produce a deterministic RFC artifact.

The artifact should include:

---

## 1. Executive Summary

High-level proposal overview.

---

## 2. Problem Statement

The unresolved concern requiring review.

---

## 3. Goals

Desired outcomes and expectations.

---

## 4. Non-Goals

Explicitly excluded concerns.

---

## 5. Constraints

Known implementation and operational constraints.

---

## 6. Proposed Approaches

Possible approaches and alternatives.

---

## 7. Tradeoffs

Tradeoff analysis between approaches.

---

## 8. Risks

Operational and architectural risks.

---

## 9. Open Questions

Remaining unresolved concerns.

Mandatory section.

---

## 10. Review Requirements

Required reviewers, validation, and alignment needs.

---

# Artifact Rules

This skill must generate:

```txt
RFC-001-<topic>.md
```

Example:

```txt
RFC-001-anonymous-session-strategy.md
```

RFC artifacts:
- are proposal-oriented
- are mutable
- evolve during review
- may eventually lead to ADRs
- do NOT represent finalized decisions

RFC artifacts may:
- supersede older RFCs
- consolidate earlier exploratory proposals
- evolve significantly during review

Major proposal shifts should preserve traceability.

---

# Behavioral Rules

## Proposal Over Finalization

This skill should:
- preserve unresolved tradeoffs
- preserve competing approaches
- surface ambiguity explicitly

This skill must NOT:
- prematurely finalize architecture
- force artificial certainty
- silently resolve open concerns

---

## Progressive Convergence

RFCs should progressively reduce ambiguity as review maturity increases.

As RFC maturity evolves:
- unresolved concerns should narrow
- infeasible approaches should be eliminated
- review blockers should become explicit
- implementation feasibility should improve

RFCs should avoid remaining permanently exploratory without convergence signals.

---

## Explicitness Over Assumption

If information is missing:
- identify missing information explicitly
- preserve unresolved concerns
- avoid fabricated certainty

Example:

```txt
Recommendation archival ownership remains unresolved.
Operational rollback expectations are currently undefined.
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

When RFC history becomes large:

- preserve unresolved tradeoffs
- preserve active constraints
- preserve important risks
- preserve review blockers

Deprioritize:
- abandoned proposal branches
- resolved iterations
- stale discussions

RFC synthesis should optimize for review relevance.

---

## Preserve Architectural Integrity

Accepted ADRs remain authoritative constraints.

This skill must NOT:
- silently override accepted decisions
- reinterpret finalized architecture
- mutate accepted constraints

---

# Failure Behavior

If insufficient context exists:

- identify missing artifacts explicitly
- identify unresolved proposal areas
- identify missing decisions
- identify review blockers

Do NOT fabricate proposal clarity.

Example:

```txt
No accepted ADR exists for recommendation ownership lifecycle.
RFC synthesis cannot reliably proceed.
```

---

# Output Style

Outputs should be:

- deterministic
- proposal-oriented
- concise
- structured
- operationally aware
- artifact-backed

Avoid:
- excessive prose
- speculative certainty
- implementation hallucination
- execution decomposition

---

# Example Invocation

```txt
Create RFC for recommendation persistence strategy
```

---

# Example Output Structure

```txt
Executive Summary
Problem Statement
Goals
Non-Goals
Constraints
Proposed Approaches
Tradeoffs
Risks
Open Questions
Review Requirements
```

---

# Important Principles

- proposals before commitment
- explicit tradeoffs over hidden assumptions
- deterministic synthesis over creativity
- architectural integrity over convenience
- reviewability over premature certainty
- visibility over hidden state

---

# Long-Term Goal

Provide stable, repeatable, high-quality proposal structuring and review preparation for long-running AI-assisted engineering workflows while preserving architectural traceability and decision integrity.