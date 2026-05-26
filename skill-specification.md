Version: v1

---

# Purpose

This document defines the architectural philosophy, behavioral rules, and implementation standards for all AI skills used within the engineering workflow system.

The goal is to create:
- deterministic AI workflows
- composable skills
- traceable outputs
- maintainable long-term collaboration
- AI-compatible engineering systems

This specification applies to all current and future skills.

---

# Core Philosophy

## Skills Are Self-Contained

Each skill must:
- operate independently
- define its own responsibilities
- define its own rules
- define its own outputs
- avoid assumptions about orchestration

Skills must NOT:
- invoke other skills
- assume workflow topology
- document execution order
- embed orchestration logic

Orchestration belongs outside the skills.

---

# Skills Behave Like Internal APIs

Skills should be treated similarly to:
- software modules
- internal APIs
- deterministic system components

Each skill should have:
- explicit responsibilities
- explicit inputs
- explicit outputs
- explicit failure behavior
- explicit artifact ownership

Avoid:
- vague behavior
- hidden assumptions
- magical orchestration
- implicit coupling

---

# Markdown + Git First

All important outputs must generate durable markdown artifacts.

Artifacts are:
- human-readable
- AI-readable
- Git-versioned
- portable
- reviewable

Chat conversations are NOT canonical memory.

---

# Human Architectural Ownership

AI assists with:
- reasoning
- decomposition
- drafting
- summarization
- structure generation

Humans retain ownership of:
- architecture
- tradeoffs
- business decisions
- approval
- execution direction

---

# Claude / Anthropic Best Practices

The workflow follows Anthropic-recommended prompting principles:

- explicit instructions
- structured outputs
- composable prompts
- role/task separation
- deterministic formatting
- clarification before execution
- allowing uncertainty
- avoiding hidden assumptions
- step-by-step reasoning
- reusable templates
- context-aware prompting

References:
- Anthropic Prompt Engineering Guide
- Context Engineering concepts
- Structured prompt design practices

:contentReference[oaicite:0]{index=0}

---

# Required Skill Structure

Every skill must define:

```txt
Purpose
Responsibilities
Non-Responsibilities
Inputs
Outputs
Artifact Rules
Behavioral Rules
Failure Behavior
Examples
```

This structure is mandatory.

---

# Skill Design Rules

## 1. Single Responsibility

A skill should do one thing well.

Avoid:
- overloaded responsibilities
- mixed concerns
- hidden secondary behaviors

Example:

Bad:
```txt
create-plan
  + task generation
  + email drafting
  + architecture review
```

Good:
```txt
create-plan
  = canonical implementation planning only
```

---

## 2. Explicit Unknowns

Skills must be allowed to say:
- insufficient information
- unresolved assumptions
- ambiguous requirements
- conflicting constraints

Skills must NOT hallucinate missing details.

---

## 3. Structured Outputs

Outputs should:
- follow templates
- generate deterministic artifacts
- preserve readability
- remain machine-friendly

Avoid:
- conversational chaos
- inconsistent formatting
- unstable output structures

---

## 4. Durable Artifact Generation

Important outputs must become markdown artifacts.

Artifacts are preferred over:
- ephemeral chat memory
- long email chains
- undocumented reasoning

---

## 5. Plans Drive Execution

Implementation artifacts must derive from:
- approved PLAN
- accepted ADRs
- finalized RFCs

Avoid implementation-first workflows.

---

# Canonical Artifact Types

| Artifact | Purpose |
|---|---|
| PLAN | Canonical implementation blueprint |
| RFC | Proposal under review |
| ADR | Accepted architectural decision |
| DISCUSSION | Historical reasoning/conversation |
| TASKS | Execution decomposition |
| STATUS | Operational progress snapshot |

---

# Artifact Naming Rules

## PLAN

```txt
PLAN-<feature>-v1.md
```

Example:

```txt
PLAN-recommendation-system-v1.md
```

---

## RFC

```txt
RFC-001-<topic>.md
```

Example:

```txt
RFC-001-anonymous-session-strategy.md
```

---

## ADR

```txt
ADR-001-<topic>.md
```

Example:

```txt
ADR-001-product-snapshotting.md
```

---

## DISCUSSION

```txt
DISCUSSION-YYYY-MM-DD-<topic>.md
```

Example:

```txt
DISCUSSION-2026-05-26-anonymous-users.md
```

---

## TASKS

```txt
TASKS-<feature>-v1.md
```

---

## STATUS

```txt
STATUS.md
```

Single evolving file.

---

# Current Skill Set

```txt
load-feature-context
explore
create-plan
create-rfc
create-adr
task-breakdown
summarize-discussion
draft-email
```

---

# Skill Responsibilities

## load-feature-context

Purpose:
Load all relevant feature artifacts automatically.

Behavior:
- minimal prompting required
- loads all available context
- identifies missing information if needed

Foundational skill.

---

## explore

Purpose:
Conversational exploration assistant.

Responsibilities:
- discuss feature ideas
- surface assumptions
- identify constraints
- uncover unknowns
- refine requirements
- explore possible directions

Outputs:
- exploration artifact

Does NOT:
- generate final implementation plan

---

## create-plan

Purpose:
Generate canonical implementation blueprint.

Behavior:
- structured
- deterministic
- implementation-oriented

Inputs:
- exploration artifacts
- clarified requirements

Outputs:
- PLAN artifact

PLAN becomes:
- execution ground truth
- reference for future implementation
- source for task decomposition

---

## create-rfc

Purpose:
Generate structured proposal under review.

Behavior:
- asks relevant clarifying questions
- explores alternatives
- identifies risks/tradeoffs

Outputs:
- RFC artifact

RFCs precede ADRs.

---

## create-adr

Purpose:
Document finalized architectural decisions.

Behavior:
- records rationale
- records consequences
- captures tradeoffs

Outputs:
- ADR artifact

---

## task-breakdown

Purpose:
Convert PLAN into executable implementation structure.

Behavior:
- derives ONLY from PLAN/RFC/ADR
- preserves dependency ordering
- avoids scope invention

Outputs:
- TASKS artifact

Includes:
- milestones
- phases
- ClickUp-ready tasks
- rollout tasks
- QA tasks

---

## summarize-discussion

Purpose:
Convert discussions into structured durable artifacts.

Sources:
- email
- engineering conversations
- meetings
- AI discussions

Outputs:
- summary artifact
- decisions
- action items
- unresolved questions

May later feed:
- RFCs
- ADRs
- emails

---

## draft-email

Purpose:
Transform structured artifacts into communication format.

Behavior:
- concise
- structured
- async-friendly

Inputs:
- RFCs
- ADRs
- summaries
- STATUS
- discussions

Does NOT:
- perform primary reasoning
- invent architectural decisions

---

# Workflow Hierarchy

```txt
load-feature-context
        ↓

explore
        ↓

create-plan
        ↓

create-rfc
        ↓

create-adr
        ↓

task-breakdown
        ↓

summarize-discussion
        ↓

draft-email
```

This hierarchy is orchestration-level guidance only.

Skills themselves must remain orchestration-independent.

---

# Important Constraints

## Skills Must NOT

- call other skills implicitly
- assume orchestration order
- mutate unrelated artifacts
- invent missing architecture
- silently override decisions
- become autonomous agents

---

# Skills SHOULD

- ask clarifying questions
- identify ambiguity
- produce deterministic outputs
- preserve traceability
- generate durable artifacts
- remain composable
- remain reviewable

---

# Long-Term Goal

```txt
Markdown + Git
        ↓
Structured AI-assisted engineering
        ↓
Durable architectural memory
        ↓
Deterministic execution workflows
        ↓
Scalable async collaboration
```