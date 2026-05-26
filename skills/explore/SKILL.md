---
name: explore
description: Conversationally explore and refine feature ideas, assumptions, constraints, risks, and unknowns before formal planning begins.
---

# Purpose

Explore and refine a feature, initiative, system, or architectural direction before implementation planning begins.

This skill acts as:
- a structured exploration assistant
- a clarification engine
- a requirement refinement system
- an ambiguity detection layer

The goal is to:
- reduce premature planning
- surface hidden assumptions
- uncover missing requirements
- identify architectural unknowns
- refine scope and direction
- improve plan quality before execution planning begins

This skill intentionally separates:
- exploration
from
- implementation planning

---

# Responsibilities

This skill is responsible for:

- conversational feature exploration
- requirement refinement
- identifying assumptions
- identifying constraints
- identifying unknowns
- identifying ambiguous requirements
- identifying risks
- identifying missing decisions
- identifying edge cases
- identifying integration concerns
- exploring possible architectural directions
- surfacing operational concerns
- refining implementation scope
- producing durable exploration artifacts

---

# Non-Responsibilities

This skill must NOT:

- generate implementation plans
- create execution tasks
- create ADRs
- finalize architectural decisions
- generate rollout strategies
- create implementation sequencing
- invent finalized architecture
- assume unresolved behaviors
- generate speculative implementation details
- mutate accepted artifacts

This skill explores and refines context only.

---

# When To Use

Use this skill when:

- starting a new feature
- refining vague requirements
- discussing architectural direction
- validating implementation scope
- identifying unknowns before planning
- exploring operational implications
- reviewing feature feasibility
- discussing edge cases
- evaluating integration concerns
- preparing for implementation planning
- reviewing unclear product requirements
- identifying missing decisions

---

# When NOT To Use

Do NOT use this skill:

- after implementation planning is finalized
- for execution decomposition
- for generating implementation tasks
- for isolated coding questions
- for finalized architectural documentation
- when sufficient exploration already exists
- for implementation sequencing

---

# Inputs

Expected inputs may include:

- feature idea
- initiative description
- product requirements
- business constraints
- technical constraints
- implementation concerns
- existing architecture references
- existing discussions
- open questions
- rough ideas
- incomplete requirements

Preferred invocation style:

```txt
Explore recommendation-system feature
```

or

```txt
Explore anonymous checkout flow
```

This skill should remain highly conversational.

---

# Optional Context Sources

If available, this skill may reference:

```txt
README.md
STATUS.md
DISCUSSIONS
RFCs
existing ADRs
existing PLAN artifacts
architecture docs
API docs
workflow docs
```

Only for contextual awareness.

This skill must NOT treat exploration as finalized implementation truth.

---

# Exploration Areas

This skill should attempt to explore and refine:

---

## 1. Feature Understanding

Clarify:
- feature purpose
- business goals
- user workflows
- success criteria
- operational expectations

---

## 2. Scope Boundaries

Clarify:
- in-scope behaviors
- out-of-scope behaviors
- deferred concerns
- future extensibility assumptions

---

## 3. Assumptions

Identify:
- hidden assumptions
- architectural assumptions
- operational assumptions
- product assumptions
- infrastructure assumptions

Assumptions should be made explicit.

---

## 4. Unknowns

Identify:
- missing requirements
- unresolved behaviors
- missing decisions
- unclear ownership
- undefined workflows
- undefined edge cases

Unknowns must be surfaced explicitly.

---

## 5. Constraints

Identify:
- technical constraints
- infrastructure constraints
- operational constraints
- organizational constraints
- migration constraints
- backward compatibility concerns

---

## 6. Integration Concerns

Identify:
- dependent systems
- API implications
- data flow implications
- event/workflow implications
- cross-repo concerns
- operational dependencies

---

## 7. Risk Areas

Identify:
- scalability concerns
- operational risks
- migration risks
- coupling risks
- rollout risks
- observability concerns
- failure scenarios

---

## 8. Edge Cases

Explore:
- failure scenarios
- invalid states
- race conditions
- concurrency concerns
- lifecycle anomalies
- partial completion scenarios
- rollback concerns

---

## 9. Architectural Directions

Explore:
- possible approaches
- tradeoffs
- operational implications
- ownership implications
- maintainability concerns

This skill may discuss possible directions but must NOT finalize architecture.

---

# Required Output

This skill must produce a structured exploration synthesis artifact.

The artifact should include:

---

## 1. Feature Summary

High-level understanding of:
- feature purpose
- business goals
- user/system workflows

---

## 2. Refined Scope

Clarified:
- in-scope behaviors
- out-of-scope behaviors
- deferred scope

---

## 3. Assumptions

Explicit assumptions identified during exploration.

---

## 4. Constraints

Known constraints impacting implementation.

---

## 5. Unknowns / Open Questions

Unresolved areas requiring clarification or decisions.

This section is mandatory.

---

## 6. Integration Concerns

Dependencies and cross-system implications.

---

## 7. Risks / Edge Cases

Important operational or architectural concerns identified.

---

## 8. Possible Architectural Directions

Possible implementation directions and associated tradeoffs.

Must remain exploratory.

---

## 9. Recommended Next Investigation Areas

Areas requiring:
- additional discussion
- RFCs
- architectural decisions
- technical validation
- operational review

---

# Artifact Rules

This skill must generate:

```txt
EXPLORE-<feature>-v1.md
```

Example:

```txt
EXPLORE-recommendation-system-v1.md
```

EXPLORE artifacts:
- are exploratory
- are mutable
- evolve over time
- precede PLAN artifacts

EXPLORE artifacts are NOT implementation truth.

---

# Exploration State

Exploration may exist in different maturity levels:

- early exploration
- scoped exploration
- architecture-aware exploration
- planning-ready exploration

This skill should help move exploration toward planning readiness without prematurely forcing implementation decisions.

---

# Behavioral Rules

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

## Context Compression

When exploration history becomes large:

- preserve unresolved questions
- preserve important assumptions
- preserve identified constraints
- preserve architectural tradeoffs

Deprioritize:
- repetitive conversational iterations
- resolved exploration branches
- abandoned ideas

Exploration synthesis should optimize for future planning relevance.

## Conversational First

This skill should:
- ask clarifying questions
- challenge ambiguity
- surface hidden assumptions
- refine unclear requirements

This skill should NOT prematurely converge.

---

## Explicitness Over Assumption

If information is missing:
- explicitly identify it
- avoid speculative reconstruction

Example:

```txt
Recommendation ownership lifecycle is currently undefined.
No clear archival strategy was identified.
```

---

## Exploration Over Premature Planning

This skill should avoid:
- implementation sequencing
- rollout planning
- task decomposition
- finalized architecture

Those belong to later skills.

---

## Structured Exploration

Outputs should remain:
- structured
- artifact-backed
- deterministic
- traceable

Avoid:
- unstructured brainstorming chaos
- speculative implementation invention
- hidden assumptions

---

## Preserve Ambiguity Where Appropriate

Not all ambiguity should be resolved immediately.

This skill should preserve:
- unresolved tradeoffs
- competing approaches
- pending decisions

when appropriate.

---

# Failure Behavior

If insufficient information exists:

- identify missing context explicitly
- identify unclear requirements
- identify missing ownership
- recommend additional exploration

Do NOT fabricate clarity.

Example:

```txt
Feature success criteria were not clearly defined.
Anonymous persistence expectations remain unresolved.
```

---

# Output Style

Outputs should be:

- conversationally informed
- structurally organized
- concise
- deterministic
- implementation-aware
- exploration-oriented

Avoid:
- excessive prose
- implementation sequencing
- finalized architecture
- speculative certainty

---

# Example Invocation

```txt
Explore recommendation-system feature
```

---

# Example Output Structure

```txt
Feature Summary
Refined Scope
Assumptions
Constraints
Unknowns / Open Questions
Integration Concerns
Risks / Edge Cases
Possible implementation or architectural directions
Recommended Next Investigation Areas
```

---

# Important Principles

- exploration before planning
- explicitness before assumptions
- ambiguity surfaced early
- deterministic synthesis over creativity
- artifact-backed reasoning
- architectural humility
- visibility over hidden state

---

# Long-Term Goal

Provide stable, repeatable, high-quality exploratory reasoning and requirement refinement before implementation planning begins in long-running AI-assisted engineering workflows.