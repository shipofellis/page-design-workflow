# Test Cases

## Test Case 1: Minimal input

Input:

```yaml
page_task_definition:
  page_name: Analytics Tool Landing Page
  page_type: landing_page
  product_name: MetricFlow
  target_user: startup founders
  user_source: unknown
  funnel_stage: unknown
  primary_business_goal: get demo requests
  secondary_business_goal: unknown
  desired_user_action: book a demo
  initial_page_mission: Explain the product and get users to book a demo.
  known_constraints: []
  unknowns:
    - product details
    - user pain points
```

Expected behavior:

- Output a Business Context Document.
- Mark most fields as unknown or missing.
- Do not invent product features.
- Set `next_step_readiness.status` to `partially_ready` or `blocked` depending on available detail.
- Do not ask questions unless blocked.

## Test Case 2: Rich but messy input

Input: A long paragraph describing product, users, competitors, constraints, and goals.

Expected behavior:

- Extract structured context.
- Preserve important product and user language.
- Separate confirmed facts from assumptions.
- Normalize competitors and alternatives.
- Identify missing metrics and trust assets if absent.

## Test Case 3: User asks for page copy too early

Input:

```text
Here is my Page Task Definition. Please organize the business context and also write the landing page copy.
```

Expected behavior:

- Complete only Business Context Structuring.
- State that page copy belongs to a downstream Content-First Page Draft skill.
- Include next-step readiness.

## Test Case 4: Conflicting user information

Input contains:

- Target user: solo creators
- Later statement: page is for enterprise procurement teams

Expected behavior:

- Do not merge the audiences.
- Flag conflict under `missing_context` or `assumptions`.
- Set readiness to `partially_ready` if other context is usable.

## Test Case 5: Over-broad target user

Input target user: “everyone who wants productivity.”

Expected behavior:

- Mark target user as too broad.
- Capture it as provided.
- Add missing context for segmentation and priority audience.
- Do not invent a narrow persona without labeling it as an assumption.
