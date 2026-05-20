
---
name: cross-functional-design-alignment
description: Facilitate structured cross-functional alignment after multi-role review, resolving tradeoffs, surfacing disagreements, and producing agreed design decisions before designer handoff.
---

# Cross-Functional Design Alignment

## Purpose

This skill facilitates structured cross-functional alignment after the proposed page strategy, content draft, and lo-fi wireframe have been reviewed.

The goal is to move from critique to decision convergence.

This skill helps the team:
- consolidate concerns
- surface disagreements
- resolve tradeoffs
- align product, design, engineering, architecture, and business priorities
- document agreed decisions
- identify unresolved escalation items
- define implementation boundaries
- prepare a stable designer handoff brief

This skill exists because critique and alignment are different activities.

Multi-role review identifies problems.
Cross-functional alignment resolves what the team will do about them.

This skill does NOT:
- generate final UI
- replace the designer
- rewrite the full page plan
- perform another generic critique pass
- hide disagreements
- force false consensus
- make unsupported technical commitments

## Workflow Position

page-task-intake
→ business-context-structuring
→ requirement-gap-analysis
→ requirement-discovery-qna
→ page-strategy-definition
→ content-first-page-draft
→ wireframe-specification
→ multi-role-review
→ cross-functional-design-alignment
→ designer-handoff-brief
→ workflow-retrospective

## When To Use

Use this skill after:
- the content-first page draft exists
- the lo-fi wireframe specification exists
- the multi-role review report exists
- concerns, risks, or tradeoffs need to be resolved before design handoff

This skill is especially important when:
- product goals conflict with design clarity
- design ambition conflicts with implementation feasibility
- conversion goals conflict with brand quality
- engineering or architecture has concerns
- stakeholders disagree on scope
- responsive or accessibility implications are uncertain

## Core Responsibilities

The skill must:
1. Consolidate review findings
2. Deduplicate concerns
3. Identify cross-functional conflicts
4. Clarify tradeoffs
5. Facilitate decision-making
6. Record agreements
7. Record rejected proposals
8. Record deferred decisions
9. Define implementation boundaries
10. Assign owners for unresolved items
11. Determine readiness for designer handoff

## Required Inputs

Expected inputs:
1. Page Strategy Document
2. Content-First Page Draft
3. Wireframe Specification
4. Multi-Role Review Report

Recommended inputs:
- technical constraints
- architecture notes
- design system constraints
- brand guidelines
- accessibility requirements
- timeline constraints
- stakeholder priorities

Optional inputs:
- analytics
- user research
- engineering estimates
- legal or compliance notes
- business priority stack

## Required Outputs

The skill MUST produce:
1. alignment summary
2. participants / represented roles
3. consolidated concerns
4. conflict map
5. tradeoff decisions
6. agreed design principles
7. accepted risks
8. rejected proposals
9. deferred decisions
10. implementation boundaries
11. responsive and accessibility agreements
12. ownership assignments
13. escalation items
14. designer handoff readiness decision

Use templates in:
templates/

## Role Perspectives

### Product Manager
Focus: business goal, user value, conversion priority, scope discipline, decision rationale.

### Product Designer
Focus: user comprehension, visual hierarchy, interaction quality, design system fit, brand expression.

### Frontend Developer
Focus: implementation feasibility, responsive behavior, component complexity, performance, maintainability.

### Architect / Tech Lead
Focus: system constraints, scalability, integration complexity, platform consistency, long-term technical risk.

### Growth / Marketing
Focus: conversion, messaging clarity, acquisition context, campaign consistency, measurement.

### QA / Accessibility
Focus: usability edge cases, accessibility compliance, responsive behavior, testability.

### Stakeholder / Business Owner
Focus: business priority, timeline, positioning, launch scope, risk tolerance.

## Alignment Philosophy

The skill should not seek polite agreement.

It should seek operational clarity.

A good alignment output makes explicit:
- what the team agrees to do
- what the team agrees not to do
- what risks the team accepts
- what remains unresolved
- who owns each open item
- what is safe to hand off to design

## Conflict Handling Rules

When perspectives conflict, the skill must:
1. name the conflict
2. identify affected roles
3. explain the tradeoff
4. list possible options
5. recommend a decision path
6. document the final decision or escalation

Do not hide conflict behind vague wording.

## Tradeoff Decision Rules

Every tradeoff decision must include:
- decision
- rationale
- alternatives considered
- accepted risk
- affected artifacts
- owner
- follow-up if needed

## Agreement Rules

Agreements must be specific enough to guide the designer.

Bad:
"Make it clean and modern."

Good:
"Preserve the problem → solution → proof → CTA narrative sequence, but allow the designer to explore alternative layout treatments for the proof section."

## Implementation Boundary Rules

The skill must define:
- approved interaction complexity
- responsive constraints
- reusable component expectations
- technical non-goals
- known implementation risks
- engineering follow-up items

## Accessibility And QA Rules

The skill should surface:
- keyboard navigation implications
- contrast considerations
- mobile readability
- motion sensitivity
- content overflow risks
- form validation concerns
- analytics instrumentation needs

when relevant.

## Readiness Rules

The skill must explicitly declare one of:
- ready_for_designer_handoff
- partially_ready_with_open_items
- blocked

The workflow should not proceed to designer handoff if:
- major strategic conflict remains unresolved
- implementation feasibility is unknown for critical sections
- CTA strategy is disputed
- responsive approach is disputed
- required proof assets are missing without fallback
- ownership for blockers is unclear

## Skill Rules

1. Do not perform another generic critique pass
2. Convert critique into decisions
3. Surface disagreement explicitly
4. Do not force false consensus
5. Document accepted risks
6. Assign owners to unresolved items
7. Separate agreements from preferences
8. Prepare stable input for designer handoff

## Success Criteria

A successful execution means:
- cross-functional concerns are consolidated
- conflicts are visible
- tradeoffs are resolved or escalated
- decisions are documented
- accepted risks are explicit
- implementation boundaries are clear
- designer handoff can proceed with fewer ambiguities
