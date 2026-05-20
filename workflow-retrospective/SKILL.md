
---
name: workflow-retrospective
description: Run structured retrospectives for product-led page design workflows, extracting reusable patterns, validating assumptions, and recommending SOP improvements after designer handoff or launch.
---

# Workflow Retrospective

## Purpose

This skill performs a structured retrospective after a page design workflow has produced a designer handoff brief, design output, stakeholder feedback, or launch data.

The goal is to convert a completed workflow into reusable organizational knowledge.

This skill identifies:

- what worked
- what failed
- reusable patterns
- recurring input gaps
- decision quality issues
- invalidated assumptions
- useful prompts or templates
- SOP improvements
- follow-up experiments

This skill exists to make the page design workflow compound over time instead of restarting from scratch for every page.

This skill does NOT:
- redesign the page
- rewrite the handoff brief
- generate a new page strategy
- run design critique as the primary task
- invent performance conclusions without evidence
- treat subjective opinions as validated learnings

---

## Workflow Position

page-task-intake
→ business-context-structuring
→ requirement-gap-analysis
→ requirement-discovery-qna
→ page-strategy-definition
→ content-first-page-draft
→ wireframe-specification
→ multi-role-review
→ designer-handoff-brief
→ workflow-retrospective

---

## When To Use

Use this skill when one or more of the following are available:

- completed designer handoff brief
- designer feedback
- stakeholder feedback
- design review notes
- implementation feedback
- launch metrics
- user feedback
- A/B test results
- post-launch learnings
- workflow execution notes

Do not use this skill before the workflow has produced enough artifacts to evaluate.

---

## Required Inputs

Expected inputs:

1. Designer Handoff Brief

Recommended inputs:

- Page Task Definition
- Business Context Document
- Requirement Gap Report
- Updated Requirement State
- Page Strategy Document
- Content-First Page Draft
- Wireframe Specification
- Multi-Role Review Report

Optional evidence:

- designer feedback
- stakeholder feedback
- engineering feedback
- user feedback
- analytics
- conversion metrics
- experiment results
- launch notes
- project timeline notes

---

## Required Outputs

The skill MUST produce:

1. retrospective summary
2. evidence inventory
3. what worked
4. what failed
5. reusable patterns
6. reusable assets
7. recurring input gaps
8. decision log review
9. assumption validation
10. SOP update recommendations
11. prompt/template update recommendations
12. future workflow improvements
13. follow-up experiments
14. next-step readiness

Use templates in:
templates/

---

## Retrospective Philosophy

The retrospective should distinguish between:

- evidence
- interpretation
- assumption
- opinion
- validated learning

A good retrospective does not simply summarize the project.

It extracts reusable operational knowledge.

---

## Evidence Hierarchy

When evaluating outcomes, prioritize evidence in this order:

1. launch metrics or experiment results
2. user feedback
3. designer / implementation feedback
4. stakeholder feedback
5. workflow artifacts
6. PM judgment
7. unverified assumptions

The skill must label confidence accordingly.

---

## Learning Categories

Classify learnings into:

- workflow learning
- product strategy learning
- user insight
- content learning
- UX learning
- design collaboration learning
- implementation learning
- analytics learning
- prompt / skill improvement

---

## Reusable Asset Rules

Reusable assets may include:

- section patterns
- question templates
- strategy patterns
- CTA patterns
- trust patterns
- wireframe patterns
- review checklists
- designer brief fragments
- prompt snippets
- anti-patterns

Every reusable asset must include:

- when to reuse it
- when not to reuse it
- required inputs
- known risks

---

## Assumption Validation Rules

For each assumption, determine:

- validated
- invalidated
- partially validated
- still unknown

Do not mark an assumption validated without evidence.

---

## SOP Update Rules

SOP recommendations must be:

- specific
- actionable
- linked to evidence
- scoped to a workflow step
- safe to reuse

Bad:
"Improve discovery."

Good:
"Add a required question in Step 3 for the user's strongest conversion objection because three recent projects lacked this input."

---

## PDF Output Requirement

After completing the Workflow Retrospective Report in the conversation interface, generate a professionally formatted PDF and save it to the user's Downloads folder.

**File name:** `[project-slug]-workflow-retrospective.pdf`
Example: `liftwise-workflow-retrospective.pdf`

**PDF must include:**
- Cover page: "Workflow Retrospective Report", step number (Step 9 of 10 or Step 10 of 10), project/product name, date
- All 14 required output sections
- Evidence inventory table
- What worked / what failed sections with evidence labels
- Reusable patterns in a scannable format
- Recurring input gaps table
- Decision log table
- Assumption validation table
- SOP update recommendations table (with priority and affected step)
- Follow-up experiments table
- Page numbers, header, footer on every body page

**Formatting standard:**
- Orange accent (#E8570A) for cover bar, section dividers, key labels
- Dark (#1A1A1A) for headings and footer
- Grid tables for structured multi-column sections
- Footer: `[project name]  ·  Workflow Retrospective  ·  Confidential`

**Implementation:** Use Python with reportlab. Reuse the BaseDocTemplate + PageTemplate pattern.

## Skill Rules

1. Do not invent outcomes
2. Separate evidence from opinion
3. Extract reusable patterns, not just project notes
4. Link recommendations to workflow steps
5. Preserve uncertainty explicitly
6. Identify both failures and successes
7. Create concrete SOP update suggestions
8. Optimize for cumulative workflow improvement

---

## Success Criteria

A successful execution means:

- reusable knowledge is extracted
- assumptions are reviewed
- recurring gaps are identified
- SOP updates are specific
- future workflows improve
- learnings are evidence-labeled
- no unsupported conclusions are made

Use:
- frameworks/
- templates/
- checklists/
- examples/
- tests/

before finalizing.
