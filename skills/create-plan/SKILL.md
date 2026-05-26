---
name: create-plan
description: Generate a deterministic, implementation-oriented canonical execution blueprint from refined exploration artifacts and accepted architectural context.
---

# Purpose

Generate a canonical implementation blueprint for a feature, initiative, or system.

This skill converts:
- refined exploration
- clarified requirements
- accepted architectural context
- operational constraints

into:
- a structured
- implementation-oriented
- execution-ready PLAN artifact

The PLAN becomes:
- the canonical implementation reference
- the execution ground truth
- the primary source for task decomposition
- the authoritative implementation blueprint

This skill intentionally separates:
- planning
from
- exploration
and
- execution decomposition

---

# Responsibilities

This skill is responsible for:

- synthesizing refined exploration into executable implementation structure
- defining implementation scope
- defining implementation architecture at planning level
- defining entities and workflows
- defining implementation sequencing at high level
- identifying dependencies
- identifying rollout concerns
- identifying migration concerns
- identifying operational considerations
- identifying observability concerns
- identifying implementation risks
- identifying deferred scope
- identifying implementation assumptions
- identifying unresolved planning blockers
- producing deterministic PLAN artifacts

---

# Non-Responsibilities

This skill must NOT:

- generate execution tasks
- create ClickUp tickets
- finalize unresolved architectural tradeoffs
- create ADRs
- create RFCs
- invent missing architecture
- fabricate unresolved requirements
- generate speculative implementation details
- silently override accepted ADRs
- generate implementation code

This skill creates implementation planning structure only.

---

# When To Use

Use this skill when:

- exploration has matured sufficiently
- feature scope is reasonably understood
- major unknowns have been surfaced
- implementation planning is required
- architectural direction is sufficiently stable
- execution planning needs canonical structure
- long-running implementation work is beginning
- implementation coordination is required

---

# When NOT To Use

Do NOT use this skill:

- during early feature brainstorming
- when major unknowns remain unresolved
- before sufficient exploration exists
- for isolated implementation questions
- for task decomposition
- for finalized architectural decisions
- for execution tracking

---

# Inputs

Expected inputs may include:

- EXPLORE artifacts
- refined requirements
- accepted ADRs
- accepted RFC outcomes
- architecture references
- operational constraints
- migration constraints
- implementation constraints
- existing system references

Preferred invocation style:

```txt
Create implementation plan for recommendation-system
```

or

```txt
Generate plan for anonymous checkout flow
```

---

# Required Context Sources

This skill should prioritize:

```txt
EXPLORE
    ↓
Accepted ADRs
    ↓
Accepted RFC outcomes
    ↓
Existing architecture artifacts
    ↓
Operational constraints
```

Exploration artifacts provide context.

Accepted ADRs provide authoritative architectural constraints.

---

# Planning Areas

This skill should attempt to define and synthesize:

---

## 1. Feature Scope

Define:
- implementation boundaries
- supported workflows
- excluded/deferred scope
- lifecycle expectations
- operational expectations

---

## 2. System Architecture

Define:
- major system components
- ownership boundaries
- workflow interactions
- integration boundaries
- operational interactions

This skill should avoid unresolved architecture invention.

---

## 3. Data / Entity Planning

Define:
- entities
- relationships
- persistence concerns
- lifecycle considerations
- ownership considerations
- versioning considerations

---

## 4. API / Interface Planning

Define:
- major APIs
- contracts
- event boundaries
- interface assumptions
- integration expectations

---

## 5. Workflow Planning

Define:
- primary workflows
- lifecycle transitions
- operational flows
- state transitions
- failure handling expectations

---

## 6. Implementation Phasing

Define:
- high-level implementation phases
- sequencing dependencies
- rollout ordering
- migration ordering

This is NOT task decomposition.

---

## 7. Operational Planning

Define:
- observability expectations
- monitoring concerns
- operational ownership
- support considerations
- rollback expectations
- recovery expectations

---

## 8. Migration / Compatibility Planning

If applicable, define:
- migration expectations
- compatibility constraints
- rollout risks
- backward compatibility assumptions
- coexistence concerns

---

## 9. Risk Areas

Identify:
- architectural risks
- operational risks
- scaling concerns
- coupling concerns
- rollout concerns
- migration risks
- implementation uncertainty

---

## 10. Deferred Scope

Explicitly identify:
- intentionally deferred work
- future extensibility
- unresolved future concerns
- non-goals

This section is mandatory.

---

# Planning State

Planning may exist in different maturity levels:

- early implementation planning
- architecture-aware planning
- execution-ready planning
- rollout-aware planning

This skill should help move planning toward execution readiness without fabricating unresolved implementation certainty.

---

# Required Output

This skill must produce a deterministic PLAN artifact.

The artifact should include:

---

## 1. Executive Summary

High-level implementation overview.

---

## 2. Refined Scope

Implementation scope and boundaries.

---

## 3. Architecture Overview

High-level implementation architecture and interactions.

---

## 4. Entity / Data Model Plan

Planned entities and relationships.

---

## 5. API / Interface Plan

Planned APIs, interfaces, and integration expectations.

---

## 6. Workflow Plan

Primary lifecycle and operational workflows.

---

## 7. Implementation Phases

High-level implementation sequencing.

---

## 8. Operational Considerations

Operational expectations and support concerns.

---

## 9. Migration / Compatibility Considerations

Migration and compatibility planning where applicable.

---

## 10. Risks / Constraints

Important risks and constraints.

---

## 11. Deferred Scope

Explicitly deferred concerns and future work.

Mandatory section.

---

## 12. Open Questions

Remaining unresolved concerns requiring:
- exploration
- RFCs
- ADRs
- operational validation

This section is mandatory.

---

# Artifact Rules

This skill must generate:

```txt
PLAN-<feature>-v1.md
```

Example:

```txt
PLAN-recommendation-system-v1.md
```

PLAN artifacts:
- are canonical implementation references
- evolve over time
- may be revised as discoveries occur
- drive downstream execution decomposition
- must preserve traceability of major planning changes

---

# Behavioral Rules

## Deterministic Planning

Outputs should:
- remain structured
- remain implementation-oriented
- avoid speculative invention
- preserve architectural integrity

Avoid:
- conversational chaos
- speculative architecture
- implementation hallucination
- unnecessary abstraction

---

## Planning Over Exploration

This skill should:
- convert refined exploration into execution structure
- reduce ambiguity where possible
- preserve unresolved concerns explicitly

This skill should NOT:
- reopen broad exploratory discussions
- brainstorm endlessly
- defer all difficult decisions

---

## Explicitness Over Assumption

If information is missing:
- identify missing information explicitly
- preserve unresolved concerns
- avoid fabricated implementation certainty

Example:

```txt
Recommendation regeneration ownership remains unresolved.
No accepted ADR exists for recommendation archival lifecycle.
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

When planning history becomes large:

- preserve canonical decisions
- preserve active implementation constraints
- preserve unresolved blockers
- preserve implementation-critical assumptions

Deprioritize:
- abandoned exploration branches
- resolved exploratory iterations
- stale discussions

Planning synthesis should optimize for implementation relevance.

---

## Preserve Architectural Integrity

Accepted ADRs must be treated as authoritative constraints.

This skill must NOT:
- silently override accepted decisions
- reinterpret finalized architecture
- mutate accepted constraints

---

## Preserve Planning Integrity

Plans may evolve over time.

When modifying existing plans:
- preserve accepted architectural constraints
- preserve implementation traceability
- preserve rationale continuity
- explicitly identify major planning shifts

Avoid silent planning drift.

---

# Failure Behavior

If insufficient context exists:

- identify missing artifacts explicitly
- identify unresolved exploration areas
- identify missing decisions
- identify planning blockers

Do NOT fabricate implementation structure.

Example:

```txt
No EXPLORE artifact exists for recommendation lifecycle expectations.
Implementation planning cannot reliably proceed.
```

---

# Output Style

Outputs should be:

- deterministic
- implementation-oriented
- concise
- structured
- operationally aware
- artifact-backed

Avoid:
- excessive prose
- vague architecture
- speculative certainty
- task-level decomposition

---

# Example Invocation

```txt
Create implementation plan for recommendation-system
```

---

# Example Output Structure

```txt
Executive Summary
Refined Scope
Architecture Overview
Entity / Data Model Plan
API / Interface Plan
Workflow Plan
Implementation Phases
Operational Considerations
Migration / Compatibility Considerations
Risks / Constraints
Deferred Scope
Open Questions
```

---

# Important Principles

- planning after exploration
- implementation structure over brainstorming
- explicitness before assumptions
- deterministic synthesis over creativity
- architectural integrity over convenience
- canonical plans over transient reasoning
- visibility over hidden state

---

# Long-Term Goal

Provide stable, repeatable, high-quality implementation planning for long-running AI-assisted engineering workflows while preserving architectural traceability, operational clarity, and deterministic execution structure.