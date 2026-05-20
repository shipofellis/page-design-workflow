
---
name: page-requirement-gap-analysis
description: Analyze missing information, structural weaknesses, and requirement risks before page strategy definition. Use after business-context-structuring and before requirement-discovery-qna.
---

# Page Requirement Gap Analysis

## Purpose

This skill identifies missing, weak, contradictory, or risky information in a page design workflow before page strategy work begins.

The skill should:

- Audit requirement completeness
- Detect missing decision-critical information
- Evaluate risk severity
- Prevent premature page design
- Generate structured gap reports
- Prioritize clarification questions
- Preserve uncertainty explicitly

This skill does NOT:
- invent missing information
- generate page strategy
- generate wireframes
- generate UI directions
- assume business goals without evidence

---

## When To Use

Use this skill when:

- Business context has already been structured
- Product information exists but may be incomplete
- The team is preparing for page strategy work
- The PM wants to know what information is still missing
- The workflow risks moving into design too early

Do NOT use this skill:

- before page-task-intake
- before business-context-structuring
- after page strategy definition
- for visual critique
- for copywriting

---

## Required Inputs

The skill expects:

1. Page Task Definition
2. Business Context Document

Optional:
- competitor references
- analytics
- existing copy
- stakeholder notes
- research summaries

---

## Core Responsibilities

The skill must:

1. Identify requirement gaps
2. Categorize each gap
3. Explain why each gap matters
4. Estimate downstream impact
5. Assess severity
6. Recommend clarification questions
7. Distinguish blocking vs non-blocking gaps
8. Preserve assumptions explicitly

---

## Gap Categories

Possible categories:

- user
- business
- product
- conversion
- trust
- messaging
- content
- analytics
- brand
- technical
- legal
- design
- market
- positioning

## Critical Gap Flags — Always Check

The following gaps must always be checked and flagged as `critical` if unresolved, because they have caused expensive mid-workflow corrections in prior runs:

- **Brand name exact casing** (`brand_name_exact_casing`): If not confirmed in the Page Task Definition, flag as critical. An error here propagates through every artifact and requires a find-and-replace pass across the entire workflow.

- **Phase 1 / Phase 2 scope split**: If the client has mentioned any future or upcoming features (e.g. configurators, smart integrations, AI features, IoT), and Phase 1 scope has not been explicitly confirmed, flag as critical. Including Phase 2 features in Phase 1 strategy requires a full strategy rewrite.

- **Competitive positioning policy**: If it is unknown whether the page may use comparative language, flag as high. Using comparative language without client clearance has required a full Page Strategy Document rewrite.

- **Service type completeness**: For any service business, if the complete list of confirmed service types has not been explicitly provided, flag as high. Incomplete lists cause content drafts to omit service types.

- **Primary photography / hero asset status**: For any page requiring a full-bleed hero or photography-heavy layout, if the hero photo is not confirmed and available, flag as high. This is the most common design execution blocker and must be assigned an owner before the designer handoff step.

---

## Severity Levels

- critical
- high
- medium
- low

Critical gaps block strategy work.

---

## Output Requirements

The final output MUST include:

- executive summary
- readiness assessment
- structured gap report
- blocking issues
- assumptions
- recommended next actions

Use the canonical schema in:

templates/requirement-gap-report-template.md

---

## PDF Output Requirement

After completing the Gap Report output in the conversation interface, generate a professionally formatted PDF and save it to the user's Downloads folder.

**File name:** `[project-slug]-requirement-gap-report.pdf`
Example: `liftwise-requirement-gap-report.pdf`

**PDF must include:**
- Cover page: "Requirement Gap Report", step number (Step 3 of 10), project/product name, date
- Executive summary with readiness status
- Structured gap table: gap, category, severity, downstream impact
- Blocking issues clearly marked
- Recommended next actions
- Page numbers, header, footer on every body page

**Formatting standard:**
- Orange accent (#E8570A) for cover bar, section dividers, key labels
- Dark (#1A1A1A) for headings and footer
- Grid tables for gap listings (severity colour-coded in notes where possible)
- Footer: `[project name]  ·  Requirement Gap Report  ·  Confidential`

**Implementation:** Use Python with reportlab. Reuse the BaseDocTemplate + PageTemplate pattern.

## Skill Rules

1. Never hallucinate missing information
2. Missing data must remain explicit
3. Every gap must explain downstream impact
4. Prioritize strategic gaps over cosmetic gaps
5. Avoid generic questions
6. Focus on decision-making impact
7. Distinguish uncertainty from contradiction
8. Preserve reusable structure
9. Always check the five Critical Gap Flags before declaring readiness

---

## Workflow Position

This skill belongs to:

page-task-intake
→ business-context-structuring
→ requirement-gap-analysis
→ requirement-discovery-qna
→ page-strategy-definition

---

## Success Criteria

A successful execution means:

- critical unknowns are surfaced
- information risks are explicit
- downstream strategy risks are identified
- next questions are prioritized
- the workflow can safely continue

Use:
- checklists/gap-analysis-checklist.md
- examples/
- tests/

before finalizing output.
