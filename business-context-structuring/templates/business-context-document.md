# Business Context Document Template

```yaml
step_name: Business Context Structuring
step_goal: Convert page-design background information into a structured Business Context Document.

input_used:
  page_task_definition:
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
  additional_context:
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

output:
  business_context_document:
    product_overview:
      summary:
      category:
      core_job_to_be_done:
      product_maturity:
      notes:

    target_users:
      primary:
        segment:
        role:
        context:
        awareness_level:
        decision_role:
      secondary:
        - segment:
          role:
          context:
          awareness_level:
          decision_role:

    user_pain_points:
      - pain_point:
        evidence_or_source:
        severity:
        page_relevance:

    user_use_cases:
      - use_case:
        trigger:
        user_action:
        desired_outcome:
        page_relevance:

    core_value_proposition:
      primary_value:
      supporting_values:
        - value:
      value_proposition_notes:

    key_features:
      - feature:
        user_benefit:
        supports_value:
        should_appear_on_page: yes | no | unknown

    competitive_context:
      direct_competitors:
        - name:
          known_positioning:
          relevance:
      indirect_alternatives:
        - alternative:
          relevance:
      existing_workarounds:
        - workaround:
          downside:

    differentiation:
      - differentiator:
        user_relevance:
        credibility_level: confirmed | assumed | unknown
        evidence:

    user_objections:
      - objection:
        category:
        likely_severity:
        implication_for_page:

    trust_assets:
      - asset:
        type:
        available: yes | no | unknown
        page_usage_potential:

    business_objectives:
      primary:
      secondary:
      downstream_user_path:

    success_metrics:
      primary_metric:
      secondary_metrics:
        - metric:
      measurement_notes:

    constraints:
      brand:
        - constraint:
      technical:
        - constraint:
      legal_or_compliance:
        - constraint:
      timeline:
        - constraint:
      content_or_asset:
        - constraint:
      accessibility_or_localization:
        - constraint:

    assumptions:
      - assumption:
        reason:
        risk:
        validation_needed:

    missing_context:
      - missing_item:
        category:
        why_it_matters:
        downstream_impact:
        priority: high | medium | low

assumptions:
  - assumption:
    reason:
    risk:
    validation_needed:

missing_information:
  - item:
    impact:
    priority: high | medium | low

quality_check:
  product_is_understandable: pass | fail
  target_user_is_identified: pass | fail
  pain_points_are_specific: pass | fail
  value_proposition_is_clear: pass | fail
  business_goal_is_clear: pass | fail
  success_metrics_are_defined: pass | fail
  constraints_are_captured: pass | fail
  uncertainty_is_explicit: pass | fail
  no_page_design_generated: pass | fail

next_step_readiness:
  status: ready | partially_ready | blocked
  reason:
  required_action:
```
