# Example: Complete Output

```yaml
step_name: "Page Task Intake"
step_goal: "Convert a raw page design request into a stable Page Task Definition."
input_used:
  raw_user_request: "I want to make a landing page for an AI tool so people can join the waitlist."
  extracted_fields:
    product_name: "unknown"
    product_description: "AI tool"
    page_name: "unknown"
    page_type: "landing_page"
    target_user: "unknown"
    user_source: "unknown"
    funnel_stage: "awareness"
    business_goal: "waitlist signup"
    secondary_business_goal: "unknown"
    desired_user_action: "join the waitlist"
    known_constraints: []
    existing_assets: []
    reference_pages: []
    language: "unknown"
    market: "unknown"
    device_priority: "unknown"
output:
  page_task_definition:
    page_name: "AI Tool Waitlist Landing Page"
    page_type: "landing_page"
    product_name: "unknown"
    product_description: "AI tool"
    target_user: "unknown"
    user_source: "unknown"
    funnel_stage: "awareness"
    primary_business_goal: "waitlist signup"
    secondary_business_goal: "unknown"
    desired_user_action: "join the waitlist"
    success_metrics:
      - "waitlist signup conversion rate"
      - "primary CTA click-through rate"
      - "hero section engagement"
    known_constraints: []
    existing_assets: []
    reference_pages: []
    language: "unknown"
    market: "unknown"
    device_priority: "unknown"
    initial_page_mission: "This page should help the target user understand the AI tool's core value and join the waitlist in order to support waitlist signup growth."
    confirmed_facts:
      - "The requested page is a landing page."
      - "The product is an AI tool."
      - "The desired user action is joining the waitlist."
      - "The primary business goal is waitlist signup."
    unknowns:
      - "Product name"
      - "Specific product description"
      - "Target user"
      - "User source"
      - "Market"
      - "Device priority"
      - "Brand or technical constraints"
assumptions:
  - assumption: "The page is intended for awareness-stage users."
    reason: "Landing pages for waitlist collection commonly target users who need to understand the product before signing up."
    risk: "medium"
  - assumption: "Waitlist signup conversion rate is a relevant success metric."
    reason: "The user explicitly said people should join the waitlist."
    risk: "low"
missing_information:
  - field: "target_user"
    why_it_matters: "The target user determines messaging, pain points, proof, and page structure."
    priority: "high"
  - field: "product_value_proposition"
    why_it_matters: "The page cannot communicate value clearly without knowing what the AI tool does."
    priority: "high"
  - field: "user_source"
    why_it_matters: "Traffic source affects user intent and the amount of education needed."
    priority: "medium"
  - field: "brand_constraints"
    why_it_matters: "Brand constraints affect later design direction and handoff."
    priority: "medium"
quality_check:
  page_type_clear: true
  target_user_clear: false
  business_goal_clear: true
  desired_action_clear: true
  unknowns_explicitly_marked: true
  no_downstream_work_performed: true
next_step_readiness:
  status: "partially_ready"
  reason: "The basic page type, business goal, and desired action are clear, but target user and product value proposition are missing."
  required_action: "Proceed to Business Context Structuring while preserving the missing information, or ask the user to clarify target user and product value proposition first."
```
