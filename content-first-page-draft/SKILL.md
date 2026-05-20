
---
name: content-first-page-draft
description: Generate structured content-first page drafts from page strategy documents before wireframing or visual design begins.
---

# Content-First Page Draft

## Purpose

This skill converts page strategy into a structured content-first page draft.

The goal is to define:
- section structure
- messaging hierarchy
- conversion flow
- content sequencing
- CTA distribution
- visual content requirements

before any visual design work begins.

This skill exists to ensure:
- strategy survives design iteration
- page structure is content-driven
- sections have explicit purpose
- copy and UX remain aligned

This skill does NOT:
- generate high-fidelity UI
- generate design systems
- generate visual styles
- generate polished brand copy
- create final wireframes

---

## Workflow Position

page-task-intake
→ business-context-structuring
→ requirement-gap-analysis
→ requirement-discovery-qna
→ page-strategy-definition
→ content-first-page-draft
→ wireframe-specification

---

## Core Responsibilities

The skill must:

1. Translate strategy into page structure
2. Define section-by-section goals
3. Create messaging hierarchy
4. Draft strategic copy scaffolding
5. Define CTA placement
6. Identify required visual assets
7. Preserve narrative flow
8. Prepare inputs for wireframing

---

## Content-First Philosophy

This skill prioritizes:

- message clarity
- user cognition
- persuasion sequencing
- information architecture
- conversion support

before visual aesthetics.

Sections should exist because they solve communication problems.

Not because they are visually common.

---

## Required Inputs

Expected inputs:

1. Page Strategy Document

Optional:
- existing copy
- tone guidelines
- brand voice
- competitor references
- SEO requirements
- localization requirements

---

## Required Outputs

The skill MUST produce:

1. section structure
2. section purpose
3. user psychological state
4. core message
5. headline draft
6. supporting copy structure
7. CTA logic
8. visual asset requirements
9. content dependencies
10. transition logic
11. content risks
12. next-step readiness

Use templates in:
templates/

---

## Section Rules

Every section must define:

- why it exists
- what user state it addresses
- what action it supports
- what uncertainty it reduces
- what information it prioritizes

Avoid:
- filler sections
- generic SaaS structures
- repetitive messaging
- aesthetic-first organization

---

## Copy Drafting Rules

Copy should be:

- structurally useful
- strategically aligned
- concise
- scannable
- hierarchy-aware

This skill generates:
- content scaffolding
- strategic messaging structure

Not final marketing polish.

---

## CTA Rules

CTA placement must align with:

- user readiness
- trust level
- narrative progression
- friction level

The skill must avoid:
- premature high-friction CTAs
- repetitive CTA spam
- unclear action hierarchy

---

## Visual Asset Rules

The skill should identify required visual support:

Possible assets:
- product screenshots
- workflow diagrams
- UI demos
- metrics
- customer logos
- illustrations
- comparison tables
- process visualizations

The skill should explain WHY each asset matters.

---

## Transition Rules

The skill must preserve continuity between sections.

Each section transition should:
- reduce cognitive friction
- logically advance persuasion
- maintain narrative momentum

---

## Phase 1 Scope Pre-Check

Before drafting any section content, verify `phase_1_confirmed_scope` and `phase_2_out_of_scope`.

Never draft content that references Phase 2 features, even if they appeared in the original brief or were mentioned in strategy discussions. If a feature or capability is Phase 2, leave a placeholder note (e.g. "Phase 2 — omit from this draft") and continue.

**Why this matters:** Phase 2 features included in the content draft require removal at wireframe stage and cascade into the designer handoff brief.

## Service Type Completeness Check

For service businesses, before drafting service-related sections, verify the complete confirmed service list from the requirement state. Count the service types explicitly and draft a section for each confirmed service. Do not omit a service type because it was not prominent in the brief — all confirmed service types deserve a section.

## PDF Output Requirement

After completing the Content-First Page Draft in the conversation interface, generate a professionally formatted PDF and save it to the user's Downloads folder.

**File name:** `[project-slug]-content-draft.pdf`
Example: `liftwise-content-draft.pdf`

**PDF must include:**
- Cover page: "Content-First Page Draft", step number (Step 6 of 10), project/product name, date
- Section-by-section structure: section name, purpose, user state, core message, headline draft, copy scaffolding, CTA, visual asset requirements
- Content dependencies and risks
- Next-step readiness
- Page numbers, header, footer on every body page

**Formatting standard:**
- Orange accent (#E8570A) for cover bar, section dividers, key labels
- Dark (#1A1A1A) for headings and footer
- Section cards (dark header bar + structured content rows) for each page section
- Footer: `[project name]  ·  Content-First Page Draft  ·  Confidential`

**Implementation:** Use Python with reportlab. Reuse the BaseDocTemplate + PageTemplate pattern.

## Skill Rules

1. Never generate final UI
2. Never prioritize aesthetics over structure
3. Every section must have strategic purpose
4. Preserve information hierarchy
5. Maintain narrative consistency
6. Run Phase 1 scope pre-check before drafting any section
7. Run service type completeness check for service businesses
8. Keep copy editable
9. Preserve assumptions explicitly
10. Optimize for downstream wireframing

---

## Success Criteria

A successful execution means:

- section structure is coherent
- narrative flow is preserved
- messaging hierarchy is clear
- CTA sequencing is logical
- visual asset needs are identified
- wireframing can begin safely

Use:
- frameworks/
- templates/
- checklists/
- examples/
- tests/

before finalizing.
