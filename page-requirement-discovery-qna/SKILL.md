
---
name: page-requirement-discovery-qna
description: Conduct structured requirement discovery interviews for page design workflows. Use after requirement-gap-analysis and before page-strategy-definition.
---

# Page Requirement Discovery Q&A

## Purpose

This skill conducts structured requirement discovery interviews to resolve critical gaps before page strategy work begins.

The skill transforms incomplete or uncertain business context into validated, structured requirements.

This skill should:
- ask high-leverage clarification questions
- prioritize questions by downstream impact
- reduce ambiguity
- preserve assumptions explicitly
- update requirement state after answers
- improve strategy readiness

This skill does NOT:
- generate page strategy
- generate wireframes
- invent answers
- ask unstructured brainstorming questions
- overwhelm users with unnecessary questions

---

## Workflow Position

page-task-intake
→ business-context-structuring
→ requirement-gap-analysis
→ requirement-discovery-qna
→ page-strategy-definition

---

## Core Responsibilities

The skill must:

1. Read requirement gaps
2. Prioritize clarification needs
3. Ask structured questions
4. Explain why each question matters
5. Capture answers consistently
6. Update requirement state
7. Track unresolved gaps
8. Evaluate readiness for strategy work

---

## Question Prioritization Rules

Questions should prioritize:

1. business-critical unknowns
2. conversion-impacting uncertainty
3. positioning ambiguity
4. user psychology gaps
5. CTA ambiguity
6. trust and proof gaps
7. implementation constraints

Avoid:
- low-impact cosmetic questions
- duplicate questions
- open-ended brainstorming
- vague prompts

---

## Interview Style

Questions must be:

- specific
- actionable
- contextual
- decision-oriented
- low cognitive load

Bad:
"Tell me more about your product."

Good:
"What is the single biggest reason users hesitate before signing up?"

---

## Mandatory Standard Questions

The following questions must always be asked if not already resolved from upstream steps. These are not optional — each was added because missing the answer caused expensive mid-workflow corrections in prior runs. Include them in the first round if unresolved.

1. **Brand name exact casing** (if `brand_name_exact_casing` is `unknown`): "What is the exact rendering of the brand name as it must appear in every heading, nav item, footer, and copy reference — including casing?" This must be confirmed before strategy work generates any artifacts.

2. **Phase 1 scope** (if `phase_1_confirmed_scope` is `unknown` or incomplete): "Which product features and capabilities are confirmed for Phase 1 launch? Which are planned for a later phase?" Do not proceed to strategy if the client has mentioned features that may be Phase 2.

3. **Competitive positioning policy** (if `competitive_positioning_policy` is `unknown`): "Should this page ever imply your company is better than a named or unnamed competitor — or must all differentiation be purely factual and self-referential?" Default assumption is factual-only; confirm before generating strategy.

4. **Complete service type list** (for service businesses, if service types have not been explicitly confirmed): "What are all the service types you offer, listed in full? Please confirm the complete list." A single missing service type discovered at content draft stage requires revision across all downstream artifacts.

5. **Hero / primary photography** (for pages requiring a full-bleed hero image): "Is a high-quality lifestyle photo for the hero section confirmed and available? If not, who is responsible for sourcing it and by what date?" This is the most common unresolved design execution dependency at designer handoff.

These five questions take priority over other discovery questions. If the round limit forces a choice, ask these first.

## Question Limits

The skill should:

- ask the minimum viable number of questions
- batch related questions
- avoid interrogation fatigue
- prioritize unresolved blockers first

Default maximum:
5 questions per round

If the five mandatory standard questions above are all already resolved, the round limit applies normally to remaining gaps.

---

## Required Inputs

Expected inputs:

1. Requirement Gap Report
2. Business Context Document
3. Page Task Definition

Optional:
- stakeholder notes
- analytics
- research
- previous answers

---

## Output Requirements

The skill MUST output:

1. prioritized questions
2. why each question matters
3. expected answer format
4. updated requirement state
5. unresolved risks
6. readiness assessment

Use schemas in:
templates/

---

## State Management

The skill must track:

- resolved gaps
- unresolved gaps
- assumptions
- contradictions
- new risks
- updated confidence

Never lose prior context.

---

## Readiness Rules

The skill must explicitly declare:

- ready
- partially_ready
- blocked

and explain why.

---

## PDF Output Requirement

After completing the Discovery Q&A output and updated requirement state in the conversation interface, generate a professionally formatted PDF and save it to the user's Downloads folder.

**File name:** `[project-slug]-discovery-qa.pdf`
Example: `liftwise-discovery-qa.pdf`

**PDF must include:**
- Cover page: "Requirement Discovery Q&A", step number (Step 4 of 10), project/product name, date
- Questions asked with rationale for each
- Client answers as captured
- Updated requirement state — resolved vs. unresolved gaps
- Readiness assessment
- Page numbers, header, footer on every body page

**Formatting standard:**
- Orange accent (#E8570A) for cover bar, section dividers, key labels
- Dark (#1A1A1A) for headings and footer
- Key-value or Q&A block format for questions and answers
- Footer: `[project name]  ·  Discovery Q&A  ·  Confidential`

**Implementation:** Use Python with reportlab. Reuse the BaseDocTemplate + PageTemplate pattern.

## Skill Rules

1. Never hallucinate answers
2. Never ask unnecessary questions
3. Never continue without critical clarification
4. Always ask the five mandatory standard questions first if unresolved
5. Preserve ambiguity explicitly
6. Prefer structured answers
7. Optimize for downstream strategy quality
8. Questions must improve decisions
9. Keep interviews efficient

---

## Success Criteria

A successful execution means:

- critical gaps are resolved
- ambiguity is reduced
- requirements become strategy-ready
- downstream risks are lowered
- the workflow can safely continue

Use:
- checklists/discovery-checklist.md
- templates/
- examples/
- tests/

before finalizing.
