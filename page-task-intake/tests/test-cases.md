# Test Cases for Page Task Intake

## Test Case 1: Minimal usable request

Input:

```text
We need a landing page for our AI research assistant. The goal is to get researchers to sign up for the beta.
```

Expected behavior:

- Output Page Task Definition.
- Mark `page_type` as `landing_page`.
- Mark `target_user` as `researchers`.
- Mark `primary_business_goal` as beta signup.
- Mark missing user source and constraints.
- Status should be `partially_ready` or `ready` depending on strictness.

## Test Case 2: Blocked request

Input:

```text
I need a page for my project.
```

Expected behavior:

- Do not invent product, user, or goal.
- Status should be `blocked`.
- Ask no more than 5 intake questions.
- Do not generate strategy, copy, or wireframe.

## Test Case 3: Existing product page redesign

Input:

```text
We want to redesign our pricing page for a B2B SaaS analytics product. The users are startup founders and ops leads comparing plans. We want more visitors to start a free trial.
```

Expected behavior:

- Output Page Task Definition.
- Mark `page_type` as `pricing_page`.
- Mark `target_user` as startup founders and ops leads.
- Mark `funnel_stage` as evaluation or conversion.
- Mark `primary_business_goal` as free trial starts.
- Mark missing constraints, current page data, and success metrics.

## Test Case 4: Internal product page

Input:

```text
I need to design an onboarding step inside our app that asks users to connect their Gmail account. We want more users to complete setup.
```

Expected behavior:

- Output Page Task Definition.
- Mark `page_type` as `onboarding_page`.
- Mark `user_source` as product navigation or in-app onboarding.
- Mark `primary_business_goal` as onboarding completion or activation.
- Mark desired action as connecting Gmail.
- Include privacy/security concerns in missing information.

## Test Case 5: Over-requested downstream work

Input:

```text
Create a landing page strategy, copy, wireframe, and UI direction for a new AI agent product.
```

Expected behavior:

- Use this skill only for Step 1.
- Produce Page Task Definition first.
- State that strategy, copy, wireframe, and UI direction belong to later steps.
- Do not perform downstream work.
