---
name: summarize-discussion
description: Convert discussions, conversations, meetings, and communication threads into deterministic, durable, traceable discussion summary artifacts.
---

# Purpose

Convert discussions into structured, durable, operationally useful summary artifacts.

This skill transforms:
- engineering discussions
- emails
- meetings
- async conversations
- AI-assisted discussions
- architecture discussions
- operational conversations

into:
- deterministic discussion summaries
- decision tracking artifacts
- action item tracking
- unresolved concern tracking
- durable historical context

The DISCUSSION artifact becomes:
- the durable historical reasoning record
- the discussion traceability layer
- the source for future RFCs/ADRs/emails
- the operational discussion reference

This skill intentionally separates:
- discussion summarization
from
- decision finalization
and
- communication drafting

---

# Responsibilities

This skill is responsible for:

- summarizing discussions deterministically
- extracting decisions
- extracting unresolved concerns
- extracting action items
- identifying blockers
- identifying assumptions
- identifying operational implications
- identifying architectural implications
- identifying follow-up requirements
- preserving discussion traceability
- preserving reasoning continuity
- preserving historical continuity
- producing deterministic DISCUSSION artifacts

---

# Non-Responsibilities

This skill must NOT:

- finalize unresolved decisions
- create ADRs automatically
- create RFCs automatically
- generate implementation plans
- invent discussion outcomes
- fabricate consensus
- silently reinterpret discussions
- mutate accepted ADRs
- mutate PLAN artifacts
- generate implementation code
- draft outbound communication
- collapse nuanced disagreements into artificial alignment

This skill summarizes discussions only.

---

# When To Use

Use this skill when:

- important engineering discussions occurred
- architectural discussions need preservation
- meetings require durable summaries
- email discussions require traceability
- implementation discussions require history
- operational discussions need preservation
- async discussions need structured tracking
- unresolved concerns need visibility
- action items require extraction

---

# When NOT To Use

Do NOT use this skill:

- for finalized architectural decisions
- for implementation planning
- for execution decomposition
- for outbound communication drafting
- for speculative brainstorming without operational value

Use:
- ADRs for finalized decisions
- PLAN for implementation planning
- TASKS for execution decomposition
- draft-email for communication formatting

---

# Inputs

Expected inputs may include:

- email threads
- engineering discussions
- meeting notes
- AI-assisted discussions
- architectural conversations
- operational discussions
- implementation conversations
- async collaboration discussions

Preferred invocation style:

```txt
Summarize recommendation-system architecture discussion
```

or

```txt
Summarize email discussion about recommendation persistence
```

---

# Required Context Sources

This skill should prioritize:

```txt
Discussion source material
    ↓
Related PLAN artifacts
    ↓
Accepted ADRs
    ↓
Relevant RFCs
    ↓
Existing DISCUSSION artifacts
```

Discussion source material remains authoritative.

Accepted ADRs remain authoritative architectural constraints.

---

# Discussion Summary Areas

This skill should attempt to define and synthesize:

---

## 1. Discussion Context

Define:
- what discussion occurred
- who/what systems were involved
- why the discussion occurred
- operational or architectural relevance

---

## 2. Key Discussion Points

Summarize:
- major discussion topics
- competing viewpoints
- important concerns
- operational implications
- implementation implications

---

## 3. Decisions Identified

Identify:
- tentative decisions
- finalized decisions mentioned
- alignment reached during discussion

This section must distinguish:
- finalized decisions
vs
- unresolved discussions

---

## 4. Open Questions

Identify:
- unresolved concerns
- pending decisions
- ambiguous requirements
- operational unknowns
- architectural unknowns

Mandatory section.

---

## 5. Action Items

Identify:
- follow-up tasks
- investigation requirements
- operational follow-ups
- architectural follow-ups
- ownership expectations if explicitly discussed

---

## 6. Risks / Concerns

Identify:
- operational concerns
- implementation concerns
- rollout concerns
- scaling concerns
- dependency concerns

---

## 7. Follow-Up Recommendations

Where relevant, identify:
- RFC candidates
- ADR candidates
- planning follow-ups
- operational reviews
- additional discussions needed

This skill should recommend, not execute.

---

# Discussion State

Discussion summaries may exist in different maturity levels:

- raw discussion summary
- structured engineering summary
- architecture-aware summary
- operationally actionable summary

This skill should help move discussions toward durable operational clarity without fabricating certainty.

---

# Required Output

This skill must produce a deterministic DISCUSSION artifact.

The artifact should include:

---

## 1. Summary Context

High-level discussion overview.

---

## 2. Key Discussion Points

Major discussion topics and concerns.

---

## 3. Decisions Identified

Tentative or finalized decisions discussed.

Must distinguish certainty levels.

---

## 4. Open Questions

Unresolved concerns and ambiguities.

Mandatory section.

---

## 5. Action Items

Follow-up requirements and ownership references if explicitly discussed.

---

## 6. Risks / Concerns

Operational and architectural concerns identified.

---

## 7. Recommended Follow-Ups

Potential RFCs, ADRs, planning updates, or future discussions.

---

# Artifact Rules

This skill must generate:

```txt
DISCUSSION-YYYY-MM-DD-<topic>.md
```

Example:

```txt
DISCUSSION-2026-05-26-anonymous-users.md
```

DISCUSSION artifacts:
- are historical reasoning artifacts
- preserve discussion continuity
- remain traceable
- may feed future RFCs/ADRs/PLAN updates
- must preserve discussion integrity
- must preserve historical ambiguity where relevant

---

# Behavioral Rules

## Summarization Over Interpretation

This skill should:
- summarize discussions faithfully
- preserve uncertainty explicitly
- preserve competing viewpoints where relevant

This skill must NOT:
- invent agreement
- silently resolve ambiguity
- fabricate architectural certainty
- reinterpret accepted decisions

---

## Explicitness Over Assumption

If discussion outcomes are unclear:
- preserve ambiguity explicitly
- identify unresolved concerns
- avoid fabricated conclusions

Example:

```txt
No clear agreement was reached regarding recommendation archival ownership.
Operational migration sequencing remains unresolved.
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

When discussion history becomes large:

- preserve unresolved concerns
- preserve important reasoning
- preserve operationally important decisions
- preserve active follow-up requirements

Deprioritize:
- repetitive conversational iterations
- resolved conversational branches
- stale low-relevance discussion detail

Discussion synthesis should optimize for future operational relevance.

---

## Preserve Historical Integrity

Discussions are historical reasoning artifacts.

This skill must:
- preserve discussion continuity
- preserve ambiguity where appropriate
- preserve important reasoning context
- preserve competing viewpoints where operationally relevant

Avoid silent discussion drift.

---

## Progressive Discussion Refinement

Discussion summaries may evolve over time.

As discussions mature:
- ambiguity may reduce
- decisions may stabilize
- operational clarity may improve

Avoid permanently unstable discussion summaries.

---

## Decision Traceability Awareness

Where discussions reference:
- finalized decisions
- RFC outcomes
- implementation constraints
- architectural direction

the summary should preserve traceability back to authoritative artifacts where possible.

Avoid shadow architectural history.

---

# Failure Behavior

If insufficient discussion context exists:

- identify missing discussion sources explicitly
- identify unresolved ambiguity
- identify missing operational context
- avoid fabricated conclusions

Do NOT fabricate discussion outcomes.

Example:

```txt
Insufficient discussion context exists regarding recommendation migration strategy.
Discussion synthesis cannot reliably proceed.
```

---

# Output Style

Outputs should be:

- deterministic
- historically accurate
- concise
- structured
- operationally aware
- artifact-backed

Avoid:
- excessive prose
- fabricated certainty
- reinterpretation of decisions
- implementation hallucination

---

# Example Invocation

```txt
Summarize recommendation-system architecture discussion
```

---

# Example Output Structure

```txt
Summary Context
Key Discussion Points
Decisions Identified
Open Questions
Action Items
Risks / Concerns
Recommended Follow-Ups
```

---

# Important Principles

- historical accuracy over convenience
- traceability over conversational memory
- explicit ambiguity over fabricated certainty
- deterministic synthesis over creativity
- operational continuity over fragmented discussion history

---

# Long-Term Goal

Provide stable, repeatable, high-quality discussion summarization and historical reasoning preservation for long-running AI-assisted engineering workflows while maintaining traceability, operational continuity, and architectural integrity.