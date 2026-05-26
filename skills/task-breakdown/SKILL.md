---
name: task-breakdown
description: Convert canonical implementation plans into deterministic execution structures, implementation phases, and task decomposition artifacts suitable for operational execution and tracking.
---

# Purpose

Convert canonical implementation plans into structured execution decomposition artifacts.

This skill transforms:
- approved PLAN artifacts
- accepted ADRs
- finalized RFC outcomes

into:
- executable implementation structure
- implementation phases
- milestone grouping
- dependency-aware task decomposition
- operational execution tracking structure

The TASKS artifact becomes:
- the operational execution blueprint
- the implementation tracking structure
- the source for ClickUp ticket creation
- the implementation sequencing reference

This skill intentionally separates:
- execution decomposition
from
- planning
and
- implementation

---

# Responsibilities

This skill is responsible for:

- decomposing implementation plans into executable tasks
- defining implementation phases
- defining milestone groupings
- identifying dependency ordering
- identifying rollout sequencing
- identifying migration sequencing
- identifying operational tasks
- identifying QA tasks
- identifying observability tasks
- identifying infra tasks
- identifying implementation blockers
- identifying parallelization opportunities
- preserving implementation traceability
- preserving execution continuity
- producing deterministic TASKS artifacts

---

# Non-Responsibilities

This skill must NOT:

- redefine implementation architecture
- silently reinterpret accepted ADRs
- invent implementation scope
- invent missing architecture
- create speculative implementation details
- create implementation code
- mutate PLAN artifacts
- mutate ADRs
- reopen finalized architectural decisions
- generate project management timelines
- estimate delivery schedules unless explicitly requested
- create artificial execution certainty

This skill decomposes execution structure only.

---

# When To Use

Use this skill when:

- implementation planning is sufficiently mature
- execution decomposition is required
- implementation sequencing is needed
- implementation coordination is required
- operational execution tracking is needed
- ClickUp task generation is needed
- rollout sequencing needs structure
- implementation ownership needs clarity

---

# When NOT To Use

Do NOT use this skill:

- during exploration
- before implementation planning exists
- before major architectural direction stabilizes
- for unresolved proposals
- for finalized architectural decisions
- for isolated coding questions

Use:
- EXPLORE for discovery
- PLAN for implementation blueprinting
- RFCs for unresolved proposals
- ADRs for finalized decisions

---

# Inputs

Expected inputs may include:

- PLAN artifacts
- accepted ADRs
- finalized RFC outcomes
- operational constraints
- rollout constraints
- migration constraints
- implementation dependencies
- architecture references
- existing TASKS artifacts

Preferred invocation style:

```txt
Break down implementation tasks for recommendation-system
```

or

```txt
Generate execution breakdown for anonymous checkout flow
```

---

# Required Context Sources

This skill should prioritize:

```txt
PLAN
    ↓
Accepted ADRs
    ↓
Finalized RFC outcomes
    ↓
Operational constraints
    ↓
Existing TASKS artifacts
```

PLAN artifacts remain authoritative implementation references.

Accepted ADRs remain authoritative architectural constraints.

---

# Task Breakdown Areas

This skill should attempt to define and synthesize:

---

## 1. Implementation Phases

Define:
- major implementation phases
- execution grouping
- dependency sequencing
- rollout ordering

Phases should remain implementation-oriented.

---

## 2. Milestone Structure

Define:
- milestone groupings
- implementation checkpoints
- operational checkpoints
- rollout checkpoints

---

## 3. Execution Tasks

Define:
- implementation tasks
- integration tasks
- migration tasks
- validation tasks
- QA tasks
- observability tasks
- infra tasks
- rollout tasks

Tasks should remain execution-oriented and traceable.

---

## 4. Dependency Ordering

Identify:
- prerequisite tasks
- sequencing constraints
- dependency chains
- blocked execution areas

---

## 5. Parallelization Opportunities

Identify:
- independently executable areas
- parallel implementation opportunities
- isolated workstreams
- low-coupling execution paths

---

## 6. Validation Requirements

Identify:
- QA expectations
- rollout validation
- migration validation
- operational verification
- observability verification

---

## 7. Rollout Considerations

Identify:
- rollout sequencing
- rollback preparation
- operational readiness tasks
- migration gating requirements

---

## 8. Execution Risks

Identify:
- implementation blockers
- migration risks
- rollout risks
- operational execution risks
- dependency risks

---

## 9. Deferred Tasks

Explicitly identify:
- intentionally deferred work
- future implementation areas
- non-goals
- postponed operational work

Mandatory section.

---

# Execution State

Task decomposition may exist in different maturity levels:

- initial execution breakdown
- dependency-aware decomposition
- rollout-aware decomposition
- implementation-ready decomposition
- active execution decomposition

This skill should help move implementation planning toward executable operational structure without fabricating execution certainty.

---

# Required Output

This skill must produce a deterministic TASKS artifact.

The artifact should include:

---

## 1. Execution Summary

High-level execution overview.

---

## 2. Implementation Phases

Major implementation phase structure.

---

## 3. Milestones

Implementation milestone grouping.

---

## 4. Task Breakdown

Detailed execution decomposition.

Tasks should include:
- purpose
- dependency references
- implementation scope
- validation expectations

---

## 5. Dependency Mapping

Important execution dependencies and sequencing constraints.

---

## 6. Parallelization Opportunities

Independent or low-coupling execution areas.

---

## 7. Validation Requirements

QA, operational, rollout, and observability validation expectations.

---

## 8. Rollout Considerations

Rollout sequencing and operational readiness concerns.

---

## 9. Risks / Blockers

Execution risks and implementation blockers.

---

## 10. Deferred Tasks

Explicitly deferred implementation work.

Mandatory section.

---

# Artifact Rules

This skill must generate:

```txt
TASKS-<feature>-v1.md
```

Example:

```txt
TASKS-recommendation-system-v1.md
```

TASKS artifacts:
- are execution-oriented
- evolve during implementation
- preserve dependency traceability
- derive from canonical plans
- must preserve implementation continuity
- must preserve implementation traceability back to PLAN artifacts

---

# Behavioral Rules

## Execution Over Planning

This skill should:
- decompose implementation into executable structure
- preserve implementation traceability
- reduce execution ambiguity

This skill must NOT:
- redesign architecture
- reopen planning discussions
- reinterpret accepted ADRs
- invent implementation scope

---

## Deterministic Decomposition

Outputs should:
- remain structured
- remain implementation-oriented
- preserve dependency ordering
- preserve execution clarity

Avoid:
- vague tasks
- speculative implementation
- implementation hallucination
- project-management theater

---

## Task Granularity Awareness

Tasks should:
- remain operationally meaningful
- preserve execution clarity
- avoid excessive fragmentation
- avoid giant ambiguous implementation buckets

Task decomposition should optimize for:
- implementation clarity
- execution traceability
- coordination efficiency

Avoid:
- microscopic task explosion
- meaningless management overhead
- artificially inflated decomposition

---

## Explicitness Over Assumption

If implementation information is missing:
- identify missing information explicitly
- preserve unresolved execution concerns
- avoid fabricated execution certainty

Example:

```txt
No accepted rollout strategy exists for recommendation migration.
Execution sequencing cannot be finalized reliably.
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

When execution history becomes large:

- preserve active milestones
- preserve dependency chains
- preserve rollout blockers
- preserve implementation-critical constraints

Deprioritize:
- completed low-relevance execution detail
- stale implementation branches
- abandoned rollout paths

Task synthesis should optimize for operational execution relevance.

---

## Preserve Architectural Integrity

Accepted ADRs remain authoritative constraints.

This skill must NOT:
- silently override accepted decisions
- reinterpret finalized architecture
- mutate accepted constraints

---

## Preserve Planning Integrity

PLAN artifacts remain authoritative implementation references.

This skill must:
- preserve implementation intent
- preserve implementation sequencing rationale
- preserve deferred scope boundaries

Avoid silent execution drift.

---

## Progressive Execution Refinement

Task decomposition may evolve as implementation maturity increases.

As implementation progresses:
- execution ambiguity should reduce
- rollout clarity should improve
- dependencies should stabilize
- validation expectations should mature

Avoid permanently unstable execution decomposition.

---

## Execution Ownership Awareness

Where possible, tasks should preserve:
- ownership boundaries
- system boundaries
- operational boundaries
- rollout responsibility boundaries

Avoid ambiguous cross-boundary execution ownership.

---

# Failure Behavior

If insufficient context exists:

- identify missing artifacts explicitly
- identify unresolved planning blockers
- identify missing architectural decisions
- identify execution ambiguity

Do NOT fabricate implementation decomposition.

Example:

```txt
No canonical PLAN artifact exists for recommendation ownership lifecycle.
Task decomposition cannot reliably proceed.
```

---

# Output Style

Outputs should be:

- deterministic
- execution-oriented
- concise
- structured
- operationally aware
- artifact-backed

Avoid:
- excessive prose
- speculative certainty
- architecture redesign
- implementation hallucination

---

# Example Invocation

```txt
Break down implementation tasks for recommendation-system
```

---

# Example Output Structure

```txt
Execution Summary
Implementation Phases
Milestones
Task Breakdown
Dependency Mapping
Parallelization Opportunities
Validation Requirements
Rollout Considerations
Risks / Blockers
Deferred Tasks
```

---

# Important Principles

- execution after planning
- implementation integrity over convenience
- deterministic decomposition over creativity
- dependency visibility over hidden state
- traceability over operational ambiguity
- rollout awareness over naive implementation

---

# Long-Term Goal

Provide stable, repeatable, high-quality execution decomposition and operational implementation structuring for long-running AI-assisted engineering workflows while preserving architectural integrity, implementation traceability, and operational execution clarity.