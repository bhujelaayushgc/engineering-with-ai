# Engineering With AI

Deterministic, artifact-driven AI-assisted engineering workflows for long-running software projects.

This repository contains:
- workflow architecture
- engineering artifacts
- AI skills
- operational conventions
- planning systems
- async collaboration patterns

designed for:
- long-running engineering projects
- AI-native development workflows
- architectural traceability
- operational continuity
- deterministic collaboration with AI systems

---

# Core Philosophy

This system is built around a few core principles:

- exploration before planning
- planning before execution
- decisions before implementation
- artifacts over conversational memory
- deterministic synthesis over improvisation
- traceability over hidden context
- async continuity over fragmented discussions

The goal is not "AI coding."

The goal is:
- operationally reliable AI-assisted engineering.

---

# Workflow Architecture

```text
explore
    ↓
create-plan
    ↓
task-breakdown
    ↓
implementation
```

Supporting workflows:

```text
create-rfc
create-adr
summarize-discussion
draft-email
load-feature-context
```

---

# Repository Structure

```text
/docs
    /features
    /plans
    /rfc
    /adr
    /tasks
    /discussions

/skills
    /explore
    /create-plan
    /create-rfc
    /create-adr
    /task-breakdown
    /summarize-discussion
    /draft-email
    /load-feature-context
```

---

# Artifact Types

| Artifact | Purpose |
|---|---|
| EXPLORE | Requirement refinement and ambiguity discovery |
| PLAN | Canonical implementation blueprint |
| RFC | Proposal under review |
| ADR | Finalized architectural decision |
| TASKS | Execution decomposition |
| DISCUSSION | Durable discussion summaries |

---

# Skill Philosophy

Skills are designed to be:

- self-contained
- independently executable
- deterministic
- artifact-aware
- composable
- operationally traceable

Skills intentionally avoid:
- hidden orchestration
- implicit assumptions
- conversational-only reasoning
- silent architectural drift

---

# Design Principles

## 1. Artifacts Are The Source Of Truth

Conversation history is temporary.

Artifacts preserve:
- decisions
- rationale
- planning
- execution structure
- operational continuity

---

## 2. Explicitness Over Assumption

Unknowns should remain visible.

The system should avoid:
- fabricated certainty
- hidden assumptions
- silent reinterpretation

---

## 3. Architectural Integrity

Accepted ADRs are authoritative constraints.

Planning and execution workflows should not silently override finalized decisions.

---

## 4. Async-First Collaboration

The workflow is designed for:
- email collaboration
- async engineering
- distributed discussions
- durable operational history

---

# Example Workflow

## 1. Explore Feature

```text
Explore recommendation-system feature
```

Produces:
```text
EXPLORE-recommendation-system-v1.md
```

---

## 2. Generate Implementation Plan

```text
Create implementation plan for recommendation-system
```

Produces:
```text
PLAN-recommendation-system-v1.md
```

---

## 3. Create RFC

```text
Create RFC for recommendation archival lifecycle
```

Produces:
```text
RFC-001-recommendation-archival-lifecycle.md
```

---

## 4. Record Architectural Decision

```text
Create ADR for recommendation snapshot persistence
```

Produces:
```text
ADR-001-recommendation-snapshotting.md
```

---

## 5. Break Down Tasks

```text
Break down implementation tasks for recommendation-system
```

Produces:
```text
TASKS-recommendation-system-v1.md
```

---

# Long-Term Goal

Build AI-assisted engineering systems that remain:
- understandable
- traceable
- maintainable
- operationally reliable

even across:
- long-running projects
- evolving architecture
- async collaboration
- multiple contributors
- AI-assisted implementation workflows
