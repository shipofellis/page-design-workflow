
---
name: page-strategy-definition
description: Define strategic page architecture, narrative logic, information hierarchy, and conversion structure before content drafting or wireframing.
---

# Page Strategy Definition

## Purpose

This skill converts validated business requirements into a strategic page plan.

The skill defines:
- page mission
- user psychological flow
- narrative structure
- information hierarchy
- CTA strategy
- trust strategy
- objection handling strategy
- section architecture

This skill exists to ensure that page structure is driven by product strategy and user psychology — not aesthetics.

This skill does NOT:
- generate high-fidelity UI
- create visual design systems
- produce polished marketing copy
- generate final wireframes
- invent business goals

---

## Workflow Position

page-task-intake
→ business-context-structuring
→ requirement-gap-analysis
→ requirement-discovery-qna
→ page-strategy-definition
→ content-first-page-draft

---

## Core Responsibilities

The skill must:

1. Define page mission
2. Define target user state
3. Design narrative progression
4. Define information hierarchy
5. Create section architecture
6. Design CTA strategy
7. Define trust strategy
8. Handle objections strategically
9. Identify strategic risks
10. Prepare stable inputs for content drafting

---

## Strategic Scope

This skill focuses on:

- persuasion structure
- cognitive sequencing
- conversion logic
- narrative flow
- information prioritization
- user psychology
- trust construction
- friction reduction

This is NOT a visual design phase.

---

## Required Inputs

Expected inputs:

1. Page Task Definition
2. Business Context Document
3. Updated Requirement State

Optional:
- analytics
- competitor references
- existing copy
- positioning docs
- brand strategy
- user research

---

## Required Outputs

The skill MUST produce:

1. page mission
2. user intent analysis
3. user psychological state
4. narrative strategy
5. information hierarchy
6. section architecture
7. CTA strategy
8. trust strategy
9. objection handling strategy
10. strategic assumptions
11. risk analysis
12. next-step readiness

Use templates in:
templates/

---

## Narrative Design Rules

Narrative progression should:

- reduce cognitive friction
- match user awareness level
- support conversion intent
- progressively build confidence
- answer objections at the right time
- avoid information overload

Possible narrative models:

- Problem → Solution → Proof → CTA
- Outcome → Mechanism → Trust → CTA
- Pain → Differentiation → Validation → Action
- Awareness → Education → Conviction → Conversion

Use the framework that best fits the user state.

---

## Information Hierarchy Rules

The skill must:

- prioritize high-impact information
- separate primary vs secondary messaging
- define scannability priorities
- optimize above-the-fold clarity
- reduce unnecessary complexity

Do not flatten all information equally.

---

## CTA Strategy Rules

The skill must define:

- primary CTA
- secondary CTA
- CTA placement logic
- CTA escalation strategy
- friction level
- commitment level
- CTA sequencing

CTA decisions must align with user readiness.

---

## Trust Strategy Rules

The skill must define:

- trust signals
- timing of trust elements
- proof hierarchy
- risk reduction mechanisms
- credibility reinforcement

Possible trust assets:
- testimonials
- metrics
- logos
- case studies
- demos
- guarantees
- compliance indicators

---

## Objection Handling Rules

The skill must identify:

- key user hesitations
- where objections emerge
- how the page addresses them
- whether objections block conversion

Objections should be handled proactively.

---

## Positioning Tonality Pre-Check

Before generating any strategy output, check the `competitive_positioning_policy` from the upstream requirement state.

- If `factual_only` (or equivalent): All differentiation must be expressed through the company's own facts — years of experience, product type, service coverage, geographic focus. Never use language that implies superiority over a named or implied competitor.

- If `comparative_allowed`: Comparative language is permitted. Confirm specific claims are defensible before including them.

- If `unknown`: Default to `factual_only`, flag the assumption explicitly, and recommend confirming before content drafting.

**Why this matters:** Using comparative positioning language without client clearance has required a full Page Strategy Document rewrite in prior workflow runs. Running this check before generating strategy prevents that.

## Phase 1 Scope Pre-Check

Before generating section architecture or feature references, verify `phase_1_confirmed_scope` and `phase_2_out_of_scope`.

- Never include Phase 2 features in strategy output, even if they were mentioned in the original brief.
- If a feature appears in the brief but is not confirmed as Phase 1, flag it as out of scope and note it as a future enhancement.

**Why this matters:** Phase 2 features included in Phase 1 strategy propagate into content draft and wireframe, requiring removals across multiple artifacts.

## PDF Output Requirement

After completing the Page Strategy Document output in the conversation interface, generate a professionally formatted PDF and save it to the user's Downloads folder.

**File name:** `[project-slug]-page-strategy.pdf`
Example: `liftwise-page-strategy.pdf`

**PDF must include:**
- Cover page: "Page Strategy Document", step number (Step 5 of 10), project/product name, date
- Page mission statement
- User intent analysis (all user tracks)
- Narrative strategy per track
- Information hierarchy
- Section architecture with rationale
- CTA strategy
- Trust strategy
- Objection handling strategy
- Strategic assumptions and risks
- Next-step readiness
- Page numbers, header, footer on every body page

**Formatting standard:**
- Orange accent (#E8570A) for cover bar, section dividers, key labels
- Dark (#1A1A1A) for headings and footer
- Key-value tables for structured fields; grid tables for multi-column strategy content
- Footer: `[project name]  ·  Page Strategy Document  ·  Confidential`

**Implementation:** Use Python with reportlab. Reuse the BaseDocTemplate + PageTemplate pattern.

## Skill Rules

1. Never jump directly into UI
2. Never generate visual systems
3. Never flatten strategy into generic sections
4. Every section must have strategic purpose
5. Narrative flow must match user psychology
6. Run positioning tonality pre-check before generating any differentiation language
7. Run Phase 1 scope pre-check before referencing any product features
8. Preserve assumptions explicitly
9. Distinguish trust from persuasion
10. Optimize for downstream content drafting

---

## Success Criteria

A successful execution means:

- the page has a clear strategic mission
- the user journey is coherent
- section ordering has rationale
- conversion logic is explicit
- trust and objections are addressed
- the workflow is ready for content drafting

Use:
- frameworks/
- templates/
- checklists/
- examples/
- tests/

before finalizing.
