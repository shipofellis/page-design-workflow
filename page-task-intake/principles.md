# Page Task Intake Principles

## 1. Define the job before designing the solution

The first step of page design is not layout, copy, or UI. It is defining the job the page must perform.

The task definition should answer:

- What page is being created?
- Who is it for?
- Why does it exist?
- What user action should it drive?
- What business outcome does that action support?

## 2. Treat missing information as a first-class output

Missing information should not be hidden or filled in casually. It should be explicitly captured as:

- `unknowns`
- `missing_information`
- `assumptions`
- `required_action`

This keeps later workflow steps grounded.

## 3. Separate facts from assumptions

A confirmed fact is directly provided by the user.

An assumption is a reasonable inference made to keep the workflow moving.

Assumptions must always be labeled.

## 4. Optimize for downstream stability

The output of this step will be consumed by later workflow steps. Therefore, the output must be stable, structured, and predictable.

Avoid prose-only output. Use consistent fields.

## 5. Do not solve too early

This step must not generate:

- Page strategy
- Section architecture
- Marketing copy
- Wireframes
- UI concepts
- Designer handoff brief

Premature solutioning reduces the quality of the workflow.

## 6. Ask only blocking questions

If enough information exists to produce a partial Page Task Definition, do that first.

Only ask questions when the task is too ambiguous to structure.

## 7. Prefer normalized labels

Use normalized values for page type, funnel stage, and business goal when possible. This improves reusability and testability across workflows.

## 8. The minimum viable task definition

At minimum, a usable Page Task Definition needs:

- `page_type`
- `target_user`
- `primary_business_goal`
- `desired_user_action`

If these are all unknown, the workflow is blocked.
