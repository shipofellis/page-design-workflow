
---
name: designer-handoff-brief
description: Create a designer-ready handoff brief from page strategy, content-first draft, wireframe specification, and multi-role review outputs.
---

# Designer Handoff Brief

## Purpose

This skill converts validated product, UX, content, and wireframe work into a designer-ready handoff brief.

The goal is to give a professional product designer enough context to begin high-quality visual and interaction design without needing to rediscover:

- business goals
- target users
- page mission
- narrative strategy
- section structure
- CTA logic
- trust requirements
- wireframe rationale
- open risks
- design constraints

This skill exists to improve PM-to-designer collaboration, reduce ambiguity, and preserve strategic intent through the design phase.

This skill does NOT:
- generate final UI
- prescribe every visual decision
- replace the designer's judgment
- create high-fidelity mockups
- turn wireframes into visual design
- over-constrain creative direction

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

## Core Responsibilities

The skill must:

1. Consolidate upstream outputs
2. Preserve strategic intent
3. Separate fixed requirements from design exploration space
4. Translate PM language into designer-usable context
5. Clarify page goals and success criteria
6. Summarize page structure and rationale
7. Surface open questions and risks
8. Define expected design deliverables
9. Prepare the next design review

---

## Required Inputs

Expected inputs:

1. Page Strategy Document
2. Content-First Page Draft
3. Wireframe Specification
4. Multi-Role Review Report

Optional:
- brand guidelines
- design system references
- competitor references
- preferred visual references
- asset inventory
- timeline
- delivery format
- stakeholder requirements
- technical constraints

---

## Required Outputs

The skill MUST produce:

1. project background
2. page objective
3. target user context
4. page mission
5. success metrics
6. strategy summary
7. final section structure
8. core content and CTA requirements
9. wireframe summary
10. visual direction guidance
11. fixed requirements
12. designer decision space
13. constraints and risks
14. asset requirements
15. delivery requirements
16. review checklist
17. open questions
18. **post-launch test plan** — for each significant conversion assumption in the strategy, specify what to test or measure, which metric to track, the test method, and the minimum evidence threshold. This closes the strategy-to-measurement loop and ensures conversion assumptions are validated after launch rather than treated as permanent facts.
19. next-step readiness

Use templates in:
templates/

---

## Handoff Philosophy

A good design brief should:

- provide strong strategic context
- clarify what must not change
- clarify where designers should explore
- explain rationale, not just instructions
- avoid micromanaging visual choices
- preserve product intent while enabling design craft

The brief should function as a collaboration artifact, not a command document.

---

## Fixed vs Flexible Boundary

The skill must clearly distinguish:

### Fixed Requirements

Things the designer should preserve unless explicitly renegotiated:
- page mission
- primary CTA
- target user
- conversion goal
- core narrative flow
- required sections
- required proof points
- critical constraints

### Designer Decision Space

Things the designer may explore:
- visual hierarchy expression
- layout refinements
- typography treatment
- spacing and rhythm
- visual metaphors
- interaction details
- illustration direction
- motion direction
- component treatment

---

## Visual Direction Guidance

The skill may provide visual direction guidance, but must not over-specify visual design.

Good guidance:
"Explore a modern B2B SaaS direction that feels precise, trustworthy, and operationally robust."

Bad guidance:
"Use exactly blue gradients, 16px border radius, Inter font, and a three-card layout."

Unless those constraints are supplied by brand guidelines.

---

## Asset Rules

The skill must identify:

- required assets
- optional assets
- missing assets
- fallback options
- ownership or source if known

Examples:
- product screenshots
- workflow diagrams
- customer logos
- testimonials
- metrics
- security badges
- demo videos
- comparison visuals

---

## Review Preparation Rules

The skill must define how the first design review should be evaluated.

Review criteria should include:
- strategy preservation
- user comprehension
- CTA clarity
- visual hierarchy
- trust expression
- mobile feasibility
- implementation feasibility

---

## PDF Output Requirement

After completing the Designer Handoff Brief in the conversation interface, generate a professionally formatted PDF and save it to the user's Downloads folder.

**File name:** `[project-slug]-designer-handoff-brief.pdf`
Example: `liftwise-designer-handoff-brief.pdf`

**PDF must include:**
- Cover page: "Designer Handoff Brief", step number (Step 8 of 10), project/product name, date
- All 19 required output sections
- Section cards (dark header bar + structured content rows) for the section structure
- Asset tables (available, required missing, fallbacks)
- Risk table
- Open questions table
- First design review checklist (as checkboxes)
- Post-launch test plan
- Page numbers, header, footer on every body page

**Formatting standard:**
- Orange accent (#E8570A) for cover bar, section dividers, key labels
- Dark (#1A1A1A) for headings and footer
- Key-value tables for metadata and structured fields
- Grid tables for multi-column content (assets, risks, open questions, test plan)
- Footer: `[project name]  ·  Designer Handoff Brief  ·  Confidential`

**Implementation:** Use Python with reportlab. Reuse the BaseDocTemplate + PageTemplate pattern.

## Skill Rules

1. Do not generate final UI
2. Do not over-constrain the designer
3. Preserve strategic rationale
4. Separate fixed requirements from flexible decisions
5. Include open questions explicitly
6. Include asset requirements explicitly
7. Include design review criteria
8. Always include the post-launch test plan
9. Optimize for designer execution clarity

---

## Success Criteria

A successful execution means:

- designer can start work without redoing discovery
- strategic intent is clear
- page structure is stable
- content and CTA requirements are explicit
- creative freedom is protected
- risks and open questions are visible
- design review can be conducted objectively

Use:
- frameworks/
- templates/
- checklists/
- examples/
- tests/

before finalizing.
