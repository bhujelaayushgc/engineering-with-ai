---
description: Initialize a minimal feature-oriented workspace for AI-assisted engineering workflows.
argument-hint: <feature-name> [optional short context]
---

# Feature Init Command

Initialize a lightweight feature workspace for long-running AI-assisted engineering workflows.

Feature input:
`$ARGUMENTS`

This command creates:
- deterministic feature structure
- canonical context anchors
- AI-readable operational boundaries

This command does NOT:
- create git branches
- create git worktrees
- generate plans
- generate RFCs
- generate ADRs
- generate tasks
- invent architecture
- perform implementation reasoning

This command initializes structure only.

---

# Responsibilities

This command should:

1. Create the minimal feature-oriented folder structure
2. Create baseline context anchor artifacts
3. Establish deterministic operational boundaries
4. Prepare the feature for future workflow skills
5. Preserve feature traceability

---

# Feature Structure

Create:

```text
/features/<feature-name>/
    README.md
    STATUS.md

    /explore
    /plans
    /rfc
    /adr
    /tasks
    /discussions
```

Do not create additional folders unless explicitly requested.

---

# README.md

Generate a minimal README.md.

Requirements:
- feature title
- optional short purpose if provided
- current state
- canonical artifact placeholders

Template:

```md
# <Feature Name>

## Purpose
<optional-context-or-placeholder>

## Current State
Initialized

## Canonical Artifacts

### Explore
- None

### Plans
- None

### RFCs
- None

### ADRs
- None

### Tasks
- None

## Notes
- Feature initialized using engineering-with-ai workflow
```

If no context is provided:
- do NOT invent feature purpose
- leave placeholder text

---

# STATUS.md

Generate a minimal STATUS.md.

Template:

```md
# Current State
Initialized

# Current Phase
Exploration

# Active Workstreams
- None

# Active Blockers
- None

# Active RFCs
- None

# Active ADRs
- None

# Active Plans
- None

# Active Tasks
- None
```

Do not invent blockers, plans, or workstreams.

---

# Behavioral Rules

## Minimal Initialization

This command should remain lightweight.

Avoid:
- speculative structure
- architecture invention
- implementation assumptions
- workflow expansion
- operational overengineering

---

## Feature-Oriented Context

The feature directory becomes the canonical operational context boundary for:
- discussions
- plans
- RFCs
- ADRs
- tasks
- future AI context loading

---

## Deterministic Structure

Naming and structure should remain:
- predictable
- traceable
- human-readable
- AI-readable

Avoid:
- creative naming
- inconsistent folder structures
- hidden context locations

---

## Explicitness Over Assumption

If context is not provided:
- preserve placeholders
- avoid fabrication
- avoid inferred architecture

---

## Context Anchoring

This command establishes:
- canonical feature context
- operational traceability anchors
- AI-readable workflow boundaries

The goal is:
- long-running operational continuity
- stable context loading
- artifact traceability

---

# Example Invocation

```bash
/feature-init recommendation-system
```

or

```bash
/feature-init recommendation-system "User-managed recommendation containers for StageGear"
```

---

# Expected Result

```text
/features/recommendation-system/
    README.md
    STATUS.md

    /explore
    /plans
    /rfc
    /adr
    /tasks
    /discussions
```

---

# Important Principles

- feature-oriented organization
- artifacts over conversational memory
- deterministic operational structure
- AI-readable context boundaries
- explicitness over assumptions
- operational continuity over chat memory

---

# Long-Term Goal

Create stable, lightweight, deterministic feature workspaces for AI-assisted engineering workflows.