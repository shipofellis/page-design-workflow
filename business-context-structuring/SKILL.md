---
name: business-context-structuring
description: Structure product, user, market, business, trust, brand, and constraint context for a website page design workflow. Use after a Page Task Definition exists, or when the user asks to organize background information before page strategy, copy, wireframe, or designer handoff work.
---

# Business Context Structuring

## Purpose

Use this skill to convert fragmented page-design background information into a stable **Business Context Document** that downstream page-design skills can consume.

This skill is Step 2 in the Product-Led Page Design SOP workflow. It does **not** create page strategy, page copy, wireframes, UI concepts, or designer briefs. Its only job is to organize the business context needed before those steps.

## When to use

Use this skill when:

- A Page Task Definition has already been created.
- The user has provided product, user, market, competitor, business, trust, brand, or constraint information.
- The next workflow step needs a clean, structured context document.
- The user says they want to prepare the inputs for page strategy, landing page planning, product page design, or designer handoff.

Do not use this skill when the user only wants final UI copy, visual design, code, or a finished design brief. In those cases, use the relevant downstream skill.

## Required upstream input

The preferred upstream input is a `Page Task Definition` from Step 1.

Expected upstream fields:

```yaml
page_name:
page_type:
product_name:
target_user:
user_source:
funnel_stage:
primary_business_goal:
secondary_business_goal:
desired_user_action:
initial_page_mission:
known_constraints:
unknowns:
```

If the upstream Page Task Definition is missing, create a minimal `input_status` section and mark missing information explicitly. Do not silently infer foundational facts.

## Optional additional input

The user may also provide:

```yaml
product_description:
core_features:
target_segments:
user_pain_points:
use_cases:
competitors:
differentiators:
pricing_info:
trust_assets:
brand_constraints:
technical_constraints:
analytics_context:
existing_research:
reference_pages:
stakeholder_notes:
```

## Core operating rules

1. **Structure, do not invent.** If information is missing, place it under `missing_context` or `assumptions`, depending on whether the workflow can proceed without it.
2. **Preserve source fidelity.** Do not over-polish ambiguous input into false certainty.
3. **Separate facts from assumptions.** Anything not explicitly provided must be labeled as an assumption.
4. **Do not design the page yet.** Do not produce page narrative, section architecture, copy, wireframe, UI direction, or designer handoff.
5. **Make downstream use easy.** Output stable field names and concise, decision-relevant content.
6. **Prioritize relevance to page design.** Include only context that could affect page strategy, content, trust, conversion, visual direction, implementation, or measurement.

## Process

Follow this sequence:

1. Inspect the upstream Page Task Definition.
2. Extract all provided product, user, market, business, trust, brand, technical, and measurement context.
3. **For service businesses:** Explicitly enumerate all service types and mark each as `confirmed` or `assumed`. Do not proceed with a partial or assumed service list — an incomplete enumeration at this step has caused content drafts to omit service types entirely, requiring correction at Step 6.
4. Carry forward `brand_name_exact_casing`, `phase_1_confirmed_scope`, `phase_2_out_of_scope`, and `competitive_positioning_policy` from the Page Task Definition into the constraints section. If any are `unknown`, flag them as high-priority missing context.
5. Normalize the information into the Business Context Document schema.
6. Identify missing context that could affect downstream page strategy.
7. Separate confirmed facts, assumptions, and open questions.
8. Run the quality checklist.
9. Declare next-step readiness.

For detailed field definitions, read `reference/field-definitions.md`.
For output format, use `templates/business-context-document.md`.
For validation, use `checklists/business-context-quality-checklist.md`.

## Output requirements

Always output using this envelope:

```yaml
step_name: Business Context Structuring
step_goal: Convert page-design background information into a structured Business Context Document.
input_used:
  page_task_definition:
  additional_context:
output:
  business_context_document:
assumptions:
missing_information:
quality_check:
next_step_readiness:
  status: ready | partially_ready | blocked
  reason:
  required_action:
```

The `business_context_document` must include these fields:

```yaml
product_overview:
target_users:
user_pain_points:
user_use_cases:
core_value_proposition:
key_features:
competitive_context:
differentiation:
user_objections:
trust_assets:
business_objectives:
success_metrics:
constraints:
assumptions:
missing_context:
```

## Readiness decision rules

Use `ready` when the context is sufficient for Requirement Gap Analysis.

Use `partially_ready` when some context is missing but the next step can still identify gaps and generate useful questions.

Use `blocked` only when the available input is too thin to identify the product, page type, target user, or business goal.

## Common failure modes

Avoid these failures:

- Generating page sections or copy too early.
- Treating vague marketing claims as confirmed product truth.
- Collapsing different user segments into one generic audience.
- Ignoring user objections, trust signals, constraints, or success metrics.
- Overfilling the document with generic SaaS assumptions.
- Producing a long essay instead of a structured context document.
- Assuming a service list is complete without explicit confirmation from the client.
- Failing to carry `brand_name_exact_casing` and `competitive_positioning_policy` into constraints.

## PDF Output Requirement

After completing the Business Context Document output in the conversation interface, generate a professionally formatted PDF and save it to the user's Downloads folder.

**File name:** `[project-slug]-business-context.pdf`
Example: `liftwise-business-context.pdf`

**PDF must include:**
- Cover page: "Business Context Document", step number (Step 2 of 10), project/product name, date
- All Business Context Document fields as a structured, readable document
- Assumptions and missing context clearly listed
- Quality check summary
- Next-step readiness declaration
- Page numbers, header, footer on every body page

**Formatting standard:**
- Orange accent (#E8570A) for cover bar, section dividers, key labels
- Dark (#1A1A1A) for headings and footer
- Key-value tables for structured fields
- Grid tables for multi-column content (pain points, use cases, competitors)
- Footer: `[project name]  ·  Business Context Document  ·  Confidential`

**Implementation:** Use Python with reportlab. Reuse the BaseDocTemplate + PageTemplate pattern for consistent cover pages and body headers/footers across all workflow documents.

## Minimal user-facing behavior

When responding to the user, provide the completed structured output. If critical input is missing, do not ask questions immediately unless the step is blocked. Instead, list missing context and mark next-step readiness.
