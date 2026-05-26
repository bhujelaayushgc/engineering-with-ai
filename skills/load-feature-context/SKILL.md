---
name: load-feature-context
description: Load and synthesize all relevant feature context and identify missing or conflicting information before feature-related work begins.
---

# Purpose

Load and synthesize all relevant feature context for a specific feature or initiative.

This skill helps establish coherent understanding of:
- current feature state
- architectural decisions
- implementation progress
- unresolved discussions
- operational risks
- missing information

The goal is to reduce context fragmentation across long-running feature development efforts.

---

# Responsibilities

This skill is responsible for:

- loading feature-related artifacts
- synthesizing current feature state
- identifying active implementation areas
- identifying accepted architectural decisions
- identifying unresolved proposals/discussions
- identifying missing or conflicting context
- identifying stale or outdated artifacts
- producing deterministic context summaries

---

# Non-Responsibilities

This skill must NOT:

- create implementation plans
- create RFCs
- create ADRs
- create tasks
- make architectural decisions
- invent missing information
- generate implementation details
- assume unresolved behaviors
- mutate existing artifacts

This skill loads and synthesizes context only.

---

# When To Use

Use this skill when:

- beginning work on an existing feature
- resuming paused feature work
- validating current feature state
- reviewing architectural history
- synthesizing fragmented context
- preparing for technical discussions
- preparing for implementation planning
- onboarding into feature work
- auditing feature consistency
- reviewing implementation progress

---

# When NOT To Use

Do NOT use this skill:

- for isolated coding questions
- for unrelated technical tasks
- when sufficient context already exists in the current session
- for generating new architecture or implementation direction

---

# Inputs

Expected inputs may include:

- feature name
- feature path
- repo path
- artifact locations
- optional implementation references
- optional discussion references

Preferred invocation style:

```txt
Load recommendation-system context
```

or

```txt
Load checkout feature context
```

This skill should require minimal prompting whenever possible.

---

# Context Sources

This skill should attempt to load and synthesize:

## Core Artifacts

```txt
README.md
STATUS.md
PLAN-*.md
TASKS-*.md
```

---

## Architecture Artifacts

```txt
architecture/
api/
workflows/
```

---

## Decision Artifacts

```txt
adr/
rfc/
```

---

## Historical Reasoning

```txt
discussions/
```

---

## Optional Sources

If available:

- implementation code
- pull requests
- issue/ticket references
- communication summaries

---

# Context Loading Strategy

This skill should prioritize:
1. Canonical artifacts first
2. Most recent accepted decisions
3. Active implementation status
4. Unresolved/open discussions last

The skill should avoid overweighting:
- stale discussions
- exploratory RFCs
- outdated plans
- orphaned tasks

---

# Artifact Authority Hierarchy

When conflicts exist, prioritize artifacts in the following order:

```txt
PLAN
    ↓
ADR
    ↓
RFC
    ↓
TASKS
    ↓
DISCUSSIONS
```

Older discussions or unresolved proposals must NOT override accepted decisions.

---

# Required Output

This skill must produce a structured context synthesis.

The synthesis should include:

---

## 1. Feature Summary

High-level understanding of:
- feature purpose
- current maturity
- major workflows
- implementation scope

---

## 2. Current Status

Current implementation state, including:
- active phase
- rollout status
- blockers
- paused work
- incomplete areas

---

## 3. Active Work

Identify:
- active implementation areas
- ongoing discussions
- unresolved work
- pending reviews
- incomplete deliverables

---

## 4. Architectural Decisions

Summarize:
- accepted ADRs
- architectural constraints
- important tradeoffs
- important invariants

---

## 5. Active RFCs / Open Proposals

Summarize:
- unresolved proposals
- pending decisions
- active tradeoffs
- review requirements

---

## 6. Risks / Missing Context

Explicitly identify:
- missing artifacts
- stale documents
- conflicting information
- unclear ownership
- unresolved technical concerns
- implementation ambiguity

This section is mandatory.

---

## 7. Recommended Next Investigation Areas

If context gaps exist, identify:
- missing decisions
- missing plans
- missing implementation details
- unresolved architectural concerns

Do NOT invent resolutions.

---

# Behavioral Rules

## Context Compression

When context volume becomes large:
- preserve canonical decisions
- preserve active implementation state
- preserve unresolved blockers
- deprioritize historical exploratory discussions

Context synthesis should optimize for operational relevance.

## Explicitness Over Assumption

If information is missing:
- explicitly state it
- avoid speculative synthesis

Example:

```txt
Recommendation regeneration strategy not found.
No accepted ADR exists for recommendation versioning.
```

---

## Deterministic Synthesis

Outputs should:
- reflect actual artifacts
- avoid creativity
- avoid speculative architecture
- avoid implementation invention

---

## Detect Stale State

This skill should identify:
- outdated plans
- orphaned tasks
- contradictory artifacts
- stale discussions
- unfinished RFCs

---

## Preserve Decision Integrity

Only accepted ADRs represent finalized architectural decisions.

RFCs and discussions must be treated as:
- exploratory
- unresolved
- proposal-oriented

unless explicitly finalized elsewhere.

---

# Failure Behavior

If insufficient context exists:

- identify missing artifacts explicitly
- explain why context is insufficient
- recommend missing investigation areas
- avoid speculative reconstruction

Example:

```txt
No PLAN artifact found.
Feature implementation scope cannot be reliably synthesized.
```

---

# Output Style

Outputs should be:

- concise
- structured
- deterministic
- artifact-referenced
- implementation-aware

Avoid:
- excessive prose
- implementation invention
- speculative architecture
- hidden assumptions

---

# Example Invocation

```txt
Load recommendation-system context
```

---

# Example Output Structure

```txt
Feature Summary
Current Status
Active Work
Architectural Decisions
Open RFCs
Risks / Missing Context
Recommended Investigation Areas
```

---

# Important Principles

- context before execution
- explicitness before assumptions
- deterministic synthesis over creativity
- artifact-backed reasoning
- visibility over hidden state
- canonical artifacts over transient discussion

---

# Long-Term Goal

Provide stable, repeatable, high-quality feature context synthesis for long-running AI-assisted engineering workflows.