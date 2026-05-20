# Example Output

```yaml
step_name: Business Context Structuring
step_goal: Convert page-design background information into a structured Business Context Document.

input_used:
  page_task_definition:
    page_name: AI Operations Agent Landing Page
    page_type: landing_page
    product_name: OpsPilot
    target_user: Operations managers at small and mid-sized SaaS companies
    user_source: LinkedIn ads and founder social posts
    funnel_stage: top_of_funnel
    primary_business_goal: collect waitlist signups
    secondary_business_goal: validate positioning for AI workflow automation
    desired_user_action: join waitlist
    initial_page_mission: Help first-time visitors quickly understand OpsPilot and join the waitlist.
    known_constraints:
      - No public pricing yet
      - Product is in private beta
    unknowns:
      - exact success metric
      - available proof assets
  additional_context:
    product_description: OpsPilot helps operations teams automate repetitive cross-tool workflows using AI agents without needing engineering support.
    core_features:
      - workflow builder
      - AI task execution
      - integrations with Slack, HubSpot, and Google Sheets
      - approval checkpoints
    target_segments:
      - SaaS operations managers
      - RevOps leads
    user_pain_points:
      - manual handoffs across tools
      - repeated reporting tasks
      - dependence on engineers for internal automation
    use_cases:
      - automate lead enrichment and routing
      - weekly KPI reporting
      - customer onboarding task coordination
    competitors:
      - Zapier
      - Make
      - internal scripts
    differentiators:
      - AI agents can reason across messy operational tasks
      - approval checkpoints reduce automation risk
    trust_assets:
      - private beta screenshots
      - 3 pilot customer quotes, not yet approved for public use
    brand_constraints:
      - should feel modern, credible, and calm
    technical_constraints:
      - must be implemented in Webflow initially

output:
  business_context_document:
    product_overview:
      summary: OpsPilot is an AI workflow automation product for operations teams that need to automate repetitive cross-tool tasks without relying on engineering support.
      category: AI workflow automation / operations automation
      core_job_to_be_done: Help operations teams coordinate and automate recurring workflows across business tools.
      product_maturity: private beta
      notes: The product should not be positioned as fully mature or generally available unless confirmed later.

    target_users:
      primary:
        segment: Small and mid-sized SaaS companies
        role: Operations manager
        context: Responsible for recurring internal workflows, reporting, routing, and coordination across tools.
        awareness_level: likely problem-aware, possibly solution-aware
        decision_role: likely evaluator or recommender; buyer role not confirmed
      secondary:
        - segment: SaaS companies
          role: RevOps lead
          context: Owns revenue operations workflows such as lead enrichment, routing, and reporting.
          awareness_level: likely solution-aware
          decision_role: unknown

    user_pain_points:
      - pain_point: Manual handoffs across disconnected tools create operational drag.
        evidence_or_source: user-provided
        severity: medium_to_high
        page_relevance: high
      - pain_point: Repeated reporting tasks consume team time.
        evidence_or_source: user-provided
        severity: medium
        page_relevance: high
      - pain_point: Teams depend on engineers for internal automation work.
        evidence_or_source: user-provided
        severity: high
        page_relevance: high

    user_use_cases:
      - use_case: Lead enrichment and routing
        trigger: New leads enter the revenue system and need to be enriched, qualified, and routed.
        user_action: Configure or monitor an automated workflow.
        desired_outcome: Faster and more reliable lead operations.
        page_relevance: high
      - use_case: Weekly KPI reporting
        trigger: Recurring reporting cycle.
        user_action: Automate data collection and report preparation.
        desired_outcome: Less manual reporting effort.
        page_relevance: medium
      - use_case: Customer onboarding task coordination
        trigger: New customer onboarding begins.
        user_action: Coordinate tasks across tools and teams.
        desired_outcome: More consistent onboarding execution.
        page_relevance: medium

    core_value_proposition:
      primary_value: Automate recurring operations workflows with AI agents without adding engineering overhead.
      supporting_values:
        - value: Reduce repetitive manual coordination.
        - value: Connect workflows across common business tools.
        - value: Use approval checkpoints to reduce automation risk.
      value_proposition_notes: The page should likely emphasize practical operational outcomes rather than abstract AI novelty.

    key_features:
      - feature: Workflow builder
        user_benefit: Allows operations teams to define automations without engineering support.
        supports_value: no-code or low-code workflow creation
        should_appear_on_page: yes
      - feature: AI task execution
        user_benefit: Handles less structured operational tasks that simple rule-based automation may not cover.
        supports_value: AI-powered automation
        should_appear_on_page: yes
      - feature: Slack, HubSpot, and Google Sheets integrations
        user_benefit: Connects to tools already used by target teams.
        supports_value: cross-tool workflow automation
        should_appear_on_page: yes
      - feature: Approval checkpoints
        user_benefit: Gives teams control before high-risk automated actions are completed.
        supports_value: safer automation
        should_appear_on_page: yes

    competitive_context:
      direct_competitors:
        - name: Zapier
          known_positioning: workflow automation platform
          relevance: high
        - name: Make
          known_positioning: visual automation platform
          relevance: high
      indirect_alternatives:
        - alternative: internal scripts
          relevance: high
      existing_workarounds:
        - workaround: manual coordination across tools
          downside: slow, repetitive, error-prone, and dependent on individual operators

    differentiation:
      - differentiator: AI agents can reason across messy operational tasks.
        user_relevance: high
        credibility_level: assumed
        evidence: user-provided claim; no supporting proof yet
      - differentiator: Approval checkpoints reduce automation risk.
        user_relevance: high
        credibility_level: confirmed_from_input
        evidence: listed as a core feature

    user_objections:
      - objection: AI automation may be unreliable for operational workflows.
        category: trust
        likely_severity: high
        implication_for_page: The page may need to explain approval checkpoints, control, and safety mechanisms.
      - objection: Product may be too early-stage because it is in private beta.
        category: product_maturity
        likely_severity: medium
        implication_for_page: The page may need to position waitlist/private beta status clearly.
      - objection: Users may compare against Zapier or Make and question why another automation tool is needed.
        category: differentiation
        likely_severity: high
        implication_for_page: The page will need clear differentiation from rule-based automation.

    trust_assets:
      - asset: private beta screenshots
        type: product_visual
        available: yes
        page_usage_potential: high
      - asset: 3 pilot customer quotes not yet approved for public use
        type: testimonial
        available: restricted
        page_usage_potential: medium_if_approved

    business_objectives:
      primary: Collect waitlist signups.
      secondary: Validate positioning for AI workflow automation.
      downstream_user_path: Waitlist signup flow; post-signup experience not provided.

    success_metrics:
      primary_metric: waitlist signup conversion rate
      secondary_metrics:
        - metric: primary CTA click-through rate
        - metric: signup form completion rate
        - metric: traffic-to-signup conversion by source
      measurement_notes: Exact success target is not provided.

    constraints:
      brand:
        - constraint: Should feel modern, credible, and calm.
      technical:
        - constraint: Must be implemented in Webflow initially.
      legal_or_compliance: []
      timeline: []
      content_or_asset:
        - constraint: Pilot quotes are not yet approved for public use.
        - constraint: No public pricing yet.
      accessibility_or_localization: []

    assumptions:
      - assumption: Primary visitors are problem-aware but may not understand how AI agents differ from traditional automation tools.
        reason: Traffic comes from LinkedIn ads and founder social posts, and competitors include Zapier/Make.
        risk: Page strategy may over-educate or under-educate if awareness level is wrong.
        validation_needed: Confirm visitor awareness and ad messaging.

    missing_context:
      - missing_item: Specific success target for waitlist conversion.
        category: analytics
        why_it_matters: Defines whether the page is optimized primarily for conversion volume, lead quality, or positioning validation.
        downstream_impact: Page strategy and CTA design.
        priority: high
      - missing_item: Whether pilot customer quotes can be used publicly.
        category: trust
        why_it_matters: Affects trust strategy and social proof options.
        downstream_impact: Content draft and designer brief.
        priority: medium
      - missing_item: Post-signup user journey.
        category: conversion
        why_it_matters: Affects CTA expectation-setting and confirmation messaging.
        downstream_impact: Page strategy and funnel continuity.
        priority: medium

assumptions:
  - assumption: Primary visitors are problem-aware but may not understand AI-agent automation differentiation.
    reason: Inferred from channel and competitive context.
    risk: Messaging depth may be miscalibrated.
    validation_needed: Confirm acquisition message and user awareness level.

missing_information:
  - item: Specific success target for waitlist conversion.
    impact: Measurement and optimization criteria remain incomplete.
    priority: high
  - item: Public availability of testimonials.
    impact: Trust strategy may need fallback proof assets.
    priority: medium

quality_check:
  product_is_understandable: pass
  target_user_is_identified: pass
  pain_points_are_specific: pass
  value_proposition_is_clear: pass
  business_goal_is_clear: pass
  success_metrics_are_defined: partially_pass
  constraints_are_captured: pass
  uncertainty_is_explicit: pass
  no_page_design_generated: pass

next_step_readiness:
  status: ready
  reason: The context is sufficient for Requirement Gap Analysis, with key missing items already identified for prioritization.
  required_action: Proceed to Step 3 and convert missing_context into a prioritized Requirement Gap Report.
```
