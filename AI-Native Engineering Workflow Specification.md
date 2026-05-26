# AI-Native Engineering Workflow Specification

Version: v2

---

# Philosophy

This workflow is designed for:

- AI-assisted engineering
- async collaboration
- architecture-first execution
- deterministic planning
- long-running feature development
- low cognitive overhead
- markdown-first documentation
- Git-native workflows

The system prioritizes:
- portability
- traceability
- maintainability
- explicit decisions
- evolving plans
- human architectural ownership

---

# Core Principles

## 1. Markdown First

All important artifacts must exist as markdown files.

Avoid:
- proprietary systems
- isolated documentation silos
- hidden knowledge

---

## 2. Git Is Canonical

Git is the source of truth for:
- plans
- RFCs
- ADRs
- discussions
- status tracking

Obsidian is an interface, not the source of truth.

---

## 3. Feature-Oriented Structure

Documentation should be grouped by feature/domain.

Avoid documentation structures grouped purely by technical layer.

---

## 4. Plans Drive Execution

Implementation must derive from:
- approved plans
- accepted ADRs
- finalized RFCs

Avoid implementation-first workflows.

---

## 5. Explicit Artifact Separation

Different artifacts serve different purposes.

Avoid mixing:
- planning
- decisions
- discussions
- execution
- communication

---

## 6. Skills Are Self-Contained

Each skill must:
- operate independently
- define explicit responsibilities
- define explicit outputs
- avoid orchestration assumptions

Skills must NOT:
- invoke other skills
- assume execution order
- embed workflow topology
- contain orchestration logic

Workflow orchestration belongs outside the skills.

---

# Repository Structure

```txt
docs/
  features/
    <feature-name>/
      README.md
      STATUS.md

      explore/
      plans/
      architecture/
      api/
      workflows/
      discussions/
      rfc/
      adr/
      tasks/
```

Example:

```txt
docs/
  features/
    recommendation-system/
      README.md
      STATUS.md

      explore/
        EXPLORE-recommendation-system-v1.md

      plans/
        PLAN-recommendation-system-v1.md

      architecture/
        entity-model.md
        lifecycle.md

      api/
        recommendation-endpoints.md

      workflows/
        recommendation-flow.md

      discussions/
        DISCUSSION-2026-05-26-anonymous-users.md

      rfc/
        RFC-001-anonymous-session-strategy.md

      adr/
        ADR-001-product-snapshotting.md

      tasks/
        TASKS-recommendation-system-v1.md
```

---

# Artifact Definitions

## EXPLORE

Purpose:
Capture exploratory feature discussions before formal planning.

Contains:
- feature discussions
- assumptions
- constraints
- unknowns
- possible directions
- open questions
- requirement refinement

EXPLORE artifacts precede PLAN artifacts.

Naming:

```txt
EXPLORE-<feature>-v1.md
```

Example:

```txt
EXPLORE-recommendation-system-v1.md
```

---

## PLAN

Purpose:
Canonical evolving implementation blueprint.

Contains:
- requirements
- entities
- APIs
- workflows
- dependencies
- rollout strategy
- migration strategy
- operational concerns
- risks
- deferred scope
- QA considerations

Properties:
- evolves over time
- implementation-oriented
- single source of implementation truth

Naming:

```txt
PLAN-<feature>-v1.md
```

Example:

```txt
PLAN-recommendation-system-v1.md
```

---

## RFC

Purpose:
Structured proposal requiring review before commitment.

RFCs may contain:
- alternatives
- tradeoffs
- risks
- proposed direction
- unresolved questions

RFCs precede ADRs.

RFCs are NOT:
- casual clarifications
- operational updates
- finalized decisions

Naming:

```txt
RFC-001-<topic>.md
```

Example:

```txt
RFC-001-anonymous-session-strategy.md
```

---

## ADR

Purpose:
Accepted architectural decision.

ADRs document:
- what was decided
- why
- tradeoffs
- consequences

ADRs are created after decisions are finalized.

Naming:

```txt
ADR-001-<topic>.md
```

Example:

```txt
ADR-001-product-snapshotting.md
```

ADR Template:

```md
# Context
# Decision
# Tradeoffs
# Consequences
# Status
```

---

## DISCUSSION

Purpose:
Preserve historical engineering reasoning and conversations.

Examples:
- technical discussions
- edge-case exploration
- unresolved concerns
- async reasoning

Naming:

```txt
DISCUSSION-YYYY-MM-DD-<topic>.md
```

Example:

```txt
DISCUSSION-2026-05-26-anonymous-users.md
```

---

## TASKS

Purpose:
Execution decomposition derived from PLAN.

Contains:
- phases
- milestones
- implementation order
- dependencies
- acceptance criteria
- QA tasks
- infra tasks
- rollout tasks

Tasks must derive ONLY from:
- approved PLAN
- accepted ADRs
- finalized RFCs

Naming:

```txt
TASKS-<feature>-v1.md
```

Example:

```txt
TASKS-recommendation-system-v1.md
```

---

## STATUS

Purpose:
Operational progress snapshot.

Tracks:
- current phase
- blockers
- active RFCs
- active ADRs
- completed milestones
- rollout state

Naming:

```txt
STATUS.md
```

Single continuously updated file.

---

# Skill Architecture Rules

## Skills Behave Like Internal APIs

Each skill should have:
- explicit responsibilities
- explicit inputs
- explicit outputs
- explicit failure behavior

Avoid:
- hidden behavior
- magical orchestration
- implicit coupling

---

## Skills Must Allow Unknowns

Skills must be allowed to state:
- insufficient information
- unresolved assumptions
- conflicting constraints
- ambiguous requirements

Skills must NOT hallucinate missing architecture.

---

## Skills Produce Durable Artifacts

Important outputs must become markdown artifacts.

Chat conversations are not canonical memory.

---

# AI Skill Definitions

## load-feature-context

Purpose:
Load all relevant feature context automatically.

Behavior:
- requires minimal prompting
- loads all available feature artifacts
- identifies missing context if necessary

Loads:
- EXPLORE
- PLAN
- RFCs
- ADRs
- TASKS
- STATUS
- discussions
- APIs
- workflows

This is the foundational skill.

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

Behavior:
- conversational
- exploratory
- clarification-oriented
- must challenge ambiguity
- must identify missing information

Outputs:
- EXPLORE markdown artifact

Does NOT:
- generate implementation plans
- generate execution tasks
- finalize architectural decisions

---

## create-plan

Purpose:
Generate canonical implementation blueprint.

Behavior:
- deterministic
- implementation-oriented
- structured
- converts exploration into executable blueprint

Inputs:
- EXPLORE artifacts
- clarified requirements
- existing architectural constraints

Outputs:
- PLAN markdown artifact

The PLAN becomes:
- implementation ground truth
- reference for discussions
- source for task decomposition

---

## create-rfc

Purpose:
Create structured proposal requiring review.

Behavior:
- asks relevant clarifying questions
- explores alternatives
- identifies tradeoffs
- surfaces risks

Outputs:
- RFC markdown artifact

---

## create-adr

Purpose:
Document finalized architectural decisions.

Behavior:
- references accepted decisions
- documents rationale
- records consequences
- captures tradeoffs

Outputs:
- ADR markdown artifact

---

## task-breakdown

Purpose:
Convert PLAN into executable implementation structure.

Behavior:
- derives ONLY from PLAN/RFC/ADR
- preserves dependency order
- avoids inventing scope

Outputs:
- TASKS markdown artifact

Includes:
- milestones
- phases
- ClickUp-ready tasks
- acceptance criteria
- rollout tasks

TASKS may evolve as PLAN evolves.

---

## summarize-discussion

Purpose:
Convert discussions into structured historical artifacts.

Sources:
- email
- engineering discussions
- AI conversations
- meetings

Outputs:
- summary markdown artifact
- action items
- decisions
- open questions

May later feed:
- RFCs
- ADRs
- emails

---

## draft-email

Purpose:
Transform structured information into communication format.

Inputs:
- summaries
- RFCs
- ADRs
- status updates
- discussions

Behavior:
- concise
- structured
- async-friendly

Email is communication layer, NOT source of truth.

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

Skills themselves remain orchestration-independent.

---

# Claude / Anthropic Prompting Principles

This workflow follows Anthropic-recommended practices:

- explicit instructions
- structured outputs
- composable prompts
- role/task separation
- deterministic formatting
- clarification before execution
- allowing uncertainty
- minimizing hidden assumptions
- reusable templates
- context-aware prompting

References:
- Anthropic Prompt Engineering Guide
- Context Engineering concepts

---

# Tool Responsibilities

| Tool | Responsibility |
|---|---|
| Git + Markdown | Canonical source |
| Cursor / VSCode | Primary editing |
| Obsidian | Thinking/navigation |
| Claude / ChatGPT | Reasoning/drafting |
| Email | Async communication |
| ClickUp | Execution tracking |

---

# Important Rules

## Single Source of Truth

| Artifact | Canonical Source |
|---|---|
| Architecture | Markdown docs |
| Decisions | ADRs |
| Plans | PLAN |
| Tasks | TASKS |
| Progress | STATUS |
| Implementation | Code |

---

## Human Ownership

AI assists:
- reasoning
- decomposition
- drafting
- summarization

Humans retain:
- architectural authority
- tradeoff ownership
- final decisions
- business judgment

---

# Avoid

- autonomous AI orchestration
- hidden state systems
- duplicated knowledge
- implementation without planning
- stale plans
- email as architecture storage
- ClickUp as documentation system
- plugin-heavy proprietary workflows

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