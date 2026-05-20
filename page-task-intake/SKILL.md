---
name: page-task-intake
description: Use this skill when a user provides an early, ambiguous, or incomplete website/page design request and you need to convert it into a stable Page Task Definition before any strategy, content, wireframe, or UI work. This is Step 1 of the Product-Led Page Design workflow.
---

# Page Task Intake

## Purpose

Convert a raw page design request into a stable, structured Page Task Definition.

This skill is the first step in a product-led website/page design workflow. It does not design the page, write final copy, generate a wireframe, or propose UI. It only clarifies what page is being requested, why it exists, who it serves, what action it should drive, and what is still unknown.

## When to use this skill

Use this skill when the user asks for help with any of the following:

- Designing a new website page
- Redesigning an existing page
- Creating a landing page, pricing page, feature page, onboarding page, signup page, checkout page, dashboard page, or similar
- Turning a vague page idea into a structured product/design brief
- Starting the first step of a page design SOP or workflow
- Preparing information for later page strategy, content drafting, wireframing, or designer handoff

Do not use this skill if the user is already asking for a later-stage deliverable, such as page strategy, content draft, wireframe, UI direction, or designer handoff brief, unless the request is missing basic task definition.

## Core rule

Do not proceed to page strategy, copywriting, wireframing, UI design, or designer handoff in this step.

Your only job is to produce a Page Task Definition and identify missing information.

## Required behavior

1. Read the user's raw request.
2. Extract all explicitly provided information.
3. Normalize it into the stable output schema.
4. Mark missing information as `unknown`.
5. Add assumptions only when they are necessary to make the output usable.
6. Clearly separate confirmed facts from assumptions.
7. End with `next_step_readiness`.
8. If the request is too ambiguous, ask focused intake questions instead of inventing the page task.

## Input fields to look for

The user may provide some, all, or none of these fields:

- `product_name`
- `product_description`
- `page_name`
- `page_type`
- `target_user`
- `user_source`
- `funnel_stage`
- `business_goal`
- `secondary_business_goal`
- `desired_user_action`
- `known_constraints`
- `timeline`
- `stakeholders`
- `existing_assets`
- `reference_pages`
- `language`
- `market`
- `device_priority`

If a field is not provided, set it to `unknown`.

### Additional required fields — learned from workflow execution

These fields must be captured at intake or explicitly flagged as high-priority unknowns. Leaving them unresolved has caused expensive mid-workflow corrections (full strategy rewrites, find-and-replace across all artifacts, scope removal at Step 6).

- `brand_name_exact_casing` — The exact rendering of the brand name as it must appear in every UI element, heading, footer, and copy reference. Example: `"liftwise"` (not `"LiftWise"`). Flag as `unknown` if not confirmed — a casing error here propagates through every subsequent artifact.

- `phase_1_confirmed_scope` — Which product features, capabilities, and page types are confirmed for this launch phase. Anything not listed is treated as out of scope. If the client has mentioned future or upcoming features, flag as a required clarification before Step 4 at the latest — including Phase 2 features in Phase 1 strategy requires expensive rewrites.

- `phase_2_out_of_scope` — Features or capabilities the client has explicitly deferred to a later phase. Capture alongside `phase_1_confirmed_scope`. If the client mentions forward-looking features (e.g. 3D configurators, smart integrations, AI features), mark each as `phase_1` or `phase_2` and confirm.

- `competitive_positioning_policy` — Whether the page may use comparative language implying superiority over named or implied competitors, or whether all differentiation must be purely factual and self-referential. If not provided, default to `factual_only` and flag for confirmation. Using comparative language without client clearance has required full strategy rewrites.

## Stable output format

Always output using this envelope:

```yaml
step_name: "Page Task Intake"
step_goal: "Convert a raw page design request into a stable Page Task Definition."
input_used:
  raw_user_request: ""
  extracted_fields: {}
output:
  page_task_definition:
    page_name: ""
    page_type: ""
    product_name: ""
    product_description: ""
    target_user: ""
    user_source: ""
    funnel_stage: ""
    primary_business_goal: ""
    secondary_business_goal: ""
    desired_user_action: ""
    success_metrics: []
    known_constraints: []
    existing_assets: []
    reference_pages: []
    language: ""
    market: ""
    device_priority: ""
    initial_page_mission: ""
    confirmed_facts: []
    unknowns: []
assumptions: []
missing_information: []
quality_check:
  page_type_clear: true
  target_user_clear: true
  business_goal_clear: true
  desired_action_clear: true
  unknowns_explicitly_marked: true
  no_downstream_work_performed: true
next_step_readiness:
  status: "ready | partially_ready | blocked"
  reason: ""
  required_action: ""
```

## Field guidance

### page_name

Use a concise descriptive name. If no name is given, derive one from the page type and product, then mark it as an assumption.

Example:

```yaml
page_name: "AI Workflow Tool Landing Page"
```

### page_type

Use a normalized page type where possible:

- landing_page
- pricing_page
- feature_page
- product_page
- signup_page
- onboarding_page
- waitlist_page
- checkout_page
- dashboard_page
- settings_page
- help_page
- comparison_page
- case_study_page
- unknown

### target_user

Describe the intended user as concretely as the input allows.

Weak:

```yaml
target_user: "users"
```

Better:

```yaml
target_user: "early-stage startup operators evaluating AI automation tools"
```

If unavailable:

```yaml
target_user: "unknown"
```

### user_source

Where the user is expected to come from.

Examples:

- paid search
- organic search
- Twitter/X ad
- LinkedIn post
- email campaign
- product navigation
- referral
- sales outreach
- unknown

### funnel_stage

Normalize into one of:

- awareness
- consideration
- evaluation
- activation
- conversion
- retention
- expansion
- unknown

### primary_business_goal

The main business outcome the page supports.

Examples:

- waitlist signup
- demo request
- account registration
- product activation
- paid conversion
- lead generation
- feature adoption
- user education
- unknown

### desired_user_action

The concrete user action the page should drive.

Examples:

- click "Join waitlist"
- submit demo request form
- start free trial
- create account
- complete onboarding step
- compare plans and upgrade
- unknown

### success_metrics

Use measurable indicators when possible. If the user has not provided metrics, propose likely candidate metrics but mark them as assumptions.

Examples:

```yaml
success_metrics:
  - "waitlist signup conversion rate"
  - "primary CTA click-through rate"
  - "hero section engagement"
```

### initial_page_mission

Write one concise sentence describing what the page must accomplish.

Formula:

```text
This page should help [target user] understand [core value] and take [desired action] in order to support [business goal].
```

If key fields are unknown, write a provisional mission and mark it as an assumption.

## Readiness logic

Use the following statuses:

### ready

Use when the minimum fields are clear enough to proceed to business context structuring:

- page_type
- target_user
- primary_business_goal
- desired_user_action

### partially_ready

Use when the page task is understandable but some important information is missing.

This is the most common status.

### blocked

Use when the request is too ambiguous to define the task.

For example:

```text
I need a page for my project.
```

In blocked cases, ask only the minimum intake questions needed to unblock the workflow.

## Minimum intake questions for blocked cases

Ask no more than 5 questions.

Prioritize:

1. What product or business is this page for?
2. What type of page do you want to create?
3. Who is the target user?
4. What should the user do after viewing the page?
5. What business outcome should the page support?

## Quality standards

A good Page Task Definition is:

- Specific enough for the next workflow step
- Honest about missing information
- Free of invented facts
- Focused on task definition, not solution design
- Structured enough to be machine-readable
- Clear enough for a PM, designer, or AI agent to use

## Failure modes to avoid

Do not:

- Generate page sections
- Write landing page copy
- Create a wireframe
- Recommend UI styles
- Over-ask unnecessary questions
- Treat assumptions as confirmed facts
- Ignore missing target user or business goal
- Proceed as if the page goal is clear when it is not

## PDF Output Requirement

After producing the Page Task Definition output in the conversation interface, generate a professionally formatted PDF and save it to the user's Downloads folder.

**File name:** `[project-slug]-page-task-definition.pdf`
Example: `liftwise-page-task-definition.pdf`

**PDF must include:**
- Cover page: "Page Task Definition", step number (Step 1 of 10), project/product name, date
- All Page Task Definition fields as a formatted document
- Assumptions and missing information listed clearly
- Quality check summary
- Next-step readiness declaration
- Page numbers, header, footer on every body page

**Formatting standard:**
- Orange accent (#E8570A) for cover bar, section dividers, key labels
- Dark (#1A1A1A) for headings and footer
- Key-value tables for structured field output
- Footer: `[project name]  ·  Page Task Definition  ·  Confidential`

**Implementation:** Use Python with reportlab. Reuse the BaseDocTemplate + PageTemplate pattern for consistent cover pages and body headers/footers across all workflow documents.

## References to bundled files

Use these files when needed:

- `principles.md` for product/design intake principles
- `templates/input-schema.yaml` for expected input shape
- `templates/output-schema.yaml` for stable output schema
- `templates/page-task-definition.md` for a human-readable document template
- `checklists/quality-check.md` for validation
- `examples/` for example inputs and outputs
- `tests/test-cases.md` for testing this skill
