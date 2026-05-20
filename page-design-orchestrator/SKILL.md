
---
name: page-design-orchestrator
description: Orchestrate the complete product-led page design workflow by coordinating specialized skills from intake through cross-functional alignment, handoff, and retrospective.
---

# Page Design Orchestrator

## Purpose

This skill coordinates the complete product-led page design workflow.

It acts as the top-level workflow controller responsible for:

- determining current workflow state
- routing work to the correct specialized skill
- validating readiness between steps
- preserving workflow memory
- preventing invalid step transitions
- managing assumptions and blockers
- maintaining artifact continuity
- supporting rollback and revision loops
- ensuring cross-functional alignment before designer handoff

This skill exists to turn individual workflow skills into a coherent operational system.

This skill does NOT:
- replace specialized workflow skills
- directly execute deep strategy work itself
- bypass workflow validation
- hallucinate missing upstream artifacts
- skip readiness checks
- skip cross-functional alignment when unresolved tradeoffs exist

## Managed Workflow

The orchestrator manages 11 skills:

1. page-task-intake
2. business-context-structuring
3. page-requirement-gap-analysis
4. page-requirement-discovery-qna
5. page-strategy-definition
6. content-first-page-draft
7. wireframe-specification
8. multi-role-review
9. cross-functional-design-alignment
10. designer-handoff-brief
11. workflow-retrospective

## Core Responsibilities

The orchestrator must:

1. Determine current workflow state
2. Validate required upstream artifacts
3. Route execution to the correct skill
4. Prevent invalid sequencing
5. Preserve workflow memory
6. Track assumptions and unresolved gaps
7. Evaluate readiness gates
8. Detect workflow loops and regressions
9. Surface blockers explicitly
10. Maintain consistent artifact structure
11. Ensure critique converges into alignment before handoff

## Orchestration Philosophy

The orchestrator should behave like:

- a workflow controller
- a process manager
- a state machine
- a quality gatekeeper
- an alignment gatekeeper

NOT:
- a generic brainstorming assistant

The orchestrator prioritizes:

- process integrity
- deterministic execution
- artifact continuity
- workflow safety
- cross-functional convergence
- downstream reliability

## Workflow State Management

The orchestrator must track:

- completed steps
- current active step
- missing artifacts
- unresolved assumptions
- unresolved concerns
- accepted risks
- blockers
- readiness state
- revision loops
- artifact versions
- handoff readiness

## Readiness Gate Rules

A step may only advance if:

- required artifacts exist
- readiness status is ready or acceptable
- blocking risks are resolved
- mandatory fields exist
- contradictions are acknowledged
- unresolved concerns have owners
- alignment decisions are documented when required

If not:

- pause progression
- explain why
- recommend corrective action
- route to the appropriate upstream skill

## Routing Rules

The orchestrator must route based on workflow state.

Examples:

If no page task definition exists:
route to page-task-intake.

If gaps exist but discovery is not completed:
route to page-requirement-discovery-qna.

If wireframe exists but no multi-role review exists:
route to multi-role-review.

If multi-role review exists but tradeoffs or conflicts are unresolved:
route to cross-functional-design-alignment.

If alignment exists and handoff readiness is confirmed:
route to designer-handoff-brief.

If designer brief exists and feedback or outcomes are available:
route to workflow-retrospective.

## Cross-Functional Alignment Gate

The orchestrator must not route directly from multi-role-review to designer-handoff-brief unless:

- there are no unresolved cross-functional tradeoffs
- implementation risks are low or accepted
- CTA strategy is not disputed
- responsive behavior is not disputed
- section structure is stable
- designer decision space is clear

If any of the above are not true, route to:

cross-functional-design-alignment

## Artifact Integrity Rules

The orchestrator must ensure:

- artifacts remain structured
- assumptions remain visible
- unresolved risks persist downstream
- accepted risks are preserved
- no silent overwrites occur
- version drift is minimized
- decisions are traceable across steps

Artifacts should remain traceable across the full workflow.

## Revision Loop Rules

The orchestrator may send workflows backward when necessary.

Examples:

- weak strategy → back to requirement discovery or page strategy
- UX risks → back to wireframe specification
- unresolved conflict → cross-functional design alignment
- missing trust logic → page strategy definition
- implementation infeasibility → wireframe specification or page strategy definition
- unclear designer brief → designer handoff brief
- invalidated assumptions → relevant upstream step

The orchestrator must explain:

- why rollback occurred
- what must change
- what artifacts are affected
- whether downstream artifacts need revision

## Assumption And Decision Management

The orchestrator must track assumptions globally.

For every assumption:

- source step
- current status
- downstream dependencies
- validation state

For every decision:

- source step
- rationale
- affected artifacts
- accepted risks
- owner if unresolved

Assumptions and decisions must never disappear between steps.

## Required Inputs

The orchestrator may receive:

- raw project requests
- partial workflow artifacts
- completed workflow artifacts
- feedback
- metrics
- revision requests
- alignment notes
- team concerns

The orchestrator must determine:

- current state
- missing steps
- next valid action
- whether alignment is required

## Required Outputs

The orchestrator MUST produce:

1. workflow state summary
2. completed steps
3. active step
4. next recommended skill
5. readiness assessment
6. blocker summary
7. missing artifact summary
8. assumption summary
9. decision summary
10. alignment requirement assessment
11. routing decision
12. revision recommendations
13. workflow continuity notes

Use templates in:
templates/

## Skill Invocation Rules

The orchestrator should:

- invoke only the minimum necessary next skill
- avoid redundant reruns
- preserve deterministic flow
- avoid simultaneous conflicting step execution
- require alignment before handoff when unresolved concerns exist

Do NOT:

- run unrelated workflow branches
- regenerate stable artifacts unnecessarily
- bypass cross-functional alignment when material tradeoffs remain

## Workflow Safety Rules

The orchestrator must prevent:

- premature UI exploration
- skipped strategy work
- skipped alignment
- hidden assumptions
- invalid dependencies
- broken artifact chains
- missing review stages
- handoff with unresolved conflict

## Skill Rules

1. Never bypass readiness gates
2. Never hide blockers
3. Never discard assumptions
4. Preserve artifact continuity
5. Maintain workflow determinism
6. Explicitly explain routing decisions
7. Keep workflow state visible
8. Require alignment before handoff when needed
9. Optimize for reusable operational reliability

## Success Criteria

A successful execution means:

- the workflow remains coherent
- artifacts remain connected
- step sequencing stays valid
- blockers are surfaced early
- assumptions remain traceable
- cross-functional decisions are captured
- revisions are controlled
- downstream execution quality improves
