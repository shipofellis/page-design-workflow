
---
name: wireframe-specification
description: Convert content-first page drafts into structured low-fidelity wireframe specifications before visual UI design begins.
---

# Wireframe Specification

## Purpose

This skill transforms content-first page drafts into structured low-fidelity wireframe specifications.

The goal is to define:
- layout logic
- content placement
- information hierarchy
- interaction structure
- responsive behavior
- CTA positioning
- visual hierarchy intent

before high-fidelity UI design begins.

This skill exists to ensure:
- strategy survives visual exploration
- content structure becomes spatially coherent
- UX risks are identified early
- layout decisions support cognition and conversion

This skill does NOT:
- generate high-fidelity UI
- define branding systems
- produce visual styling
- define animations in detail
- create polished visual comps

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

---

## Core Responsibilities

The skill must:

1. Translate content structure into layout structure
2. Define section-by-section layout behavior
3. Preserve information hierarchy spatially
4. Define CTA placement logic
5. Specify responsive behavior
6. Identify UX and layout risks
7. Define content density expectations
8. Prepare inputs for UI exploration

---

## Wireframe Philosophy

Wireframes are:
- structural tools
- UX communication tools
- hierarchy validation tools

They are NOT:
- visual design deliverables
- branding exercises
- aesthetic explorations

This skill prioritizes:
- comprehension
- conversion flow
- scannability
- responsiveness
- interaction clarity

before visual polish.

---

## Required Inputs

Expected inputs:

1. Content-First Page Draft

Optional:
- responsive requirements
- component constraints
- technical limitations
- accessibility requirements
- platform constraints

---

## Required Outputs

The skill MUST produce:

1. page layout summary
2. desktop wireframe specification
3. mobile wireframe specification
4. section layouts
5. hierarchy logic
6. CTA placement logic
7. responsive behavior
8. interaction notes
9. content density notes
10. UX risk analysis
11. implementation complexity notes
12. **unresolved asset dependencies** — every key asset that is not yet confirmed (hero photos, product photos, icons, illustrations), with owner and priority. This section makes the designer handoff brief substantive without requiring it to rediscover asset gaps from scratch.
13. next-step readiness

Use templates in:
templates/

---

## Layout Rules

Every section layout must define:

- content positioning
- visual emphasis
- reading order
- CTA location
- hierarchy logic
- desktop behavior
- mobile behavior

Avoid:
- arbitrary symmetry
- aesthetic-first layouts
- unclear reading flow
- dense content walls

---

## Responsive Rules

The skill must explicitly define:

- desktop behavior
- tablet behavior
- mobile behavior
- stacking rules
- CTA adaptation
- hierarchy preservation

Mobile should not be treated as:
"desktop shrunk smaller."

---

## Hierarchy Rules

The wireframe must preserve:

- strategic priorities
- narrative flow
- visual scanning patterns
- conversion emphasis
- trust visibility

Hierarchy should remain understandable without visual styling.

---

## CTA Placement Rules

CTA placement must align with:

- user readiness
- narrative progression
- trust accumulation
- friction level

The skill must explain:
WHY a CTA appears where it does.

---

## Interaction Rules

The skill may define:

- expandable sections
- tab systems
- comparison interactions
- onboarding flows
- demo triggers

Only when interaction meaningfully improves comprehension.

Avoid:
interaction complexity without strategic purpose.

---

## UX Risk Rules

The skill must identify:

- cognitive overload risks
- weak hierarchy
- unclear navigation
- mobile readability issues
- excessive density
- weak CTA visibility
- trust placement problems

---

## PDF Output Requirement

After completing the Wireframe Specification in the conversation interface, generate a professionally formatted PDF and save it to the user's Downloads folder.

**File name:** `[project-slug]-wireframe-specification.pdf`
Example: `liftwise-wireframe-specification.pdf`

**PDF must include:**
- Cover page: "Wireframe Specification", step number (Step 7 of 10), project/product name, date
- Executive summary
- Section-by-section wireframe specs with ASCII layout diagrams in monospace font
- Responsive behaviour summary table (desktop / tablet / mobile per section)
- UX risk analysis table
- Implementation complexity table
- Unresolved asset dependencies section
- Next-step readiness
- Page numbers, header, footer on every body page

**Formatting standard:**
- Orange accent (#E8570A) for cover bar, section dividers, key labels
- Dark (#1A1A1A) for headings and footer
- Monospace (Courier) font for all ASCII diagrams — preserve spacing exactly
- Grid tables for responsive summary, UX risk, and implementation complexity
- Footer: `[project name]  ·  Wireframe Specification  ·  Confidential`

**Implementation:** Use Python with reportlab. Reuse the BaseDocTemplate + PageTemplate pattern.

## Skill Rules

1. Never generate high-fidelity UI
2. Never prioritize aesthetics over structure
3. Every layout decision needs rationale
4. Preserve narrative continuity
5. Preserve hierarchy across breakpoints
6. Explicitly define responsive behavior
7. Always produce the Unresolved Asset Dependencies section
8. Preserve assumptions explicitly
9. Optimize for downstream UI design

---

## Success Criteria

A successful execution means:

- layout logic is coherent
- hierarchy is spatially clear
- responsive behavior is defined
- CTA placement supports conversion
- UX risks are identified early
- UI design can begin safely

Use:
- frameworks/
- templates/
- checklists/
- examples/
- tests/

before finalizing.
