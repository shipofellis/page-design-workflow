
# Routing Rules

## Initial Intake

Condition:
No structured artifacts exist.

Route:
page-task-intake

## Missing Business Context

Condition:
Task definition exists but business context incomplete.

Route:
business-context-structuring

## Missing Critical Inputs

Condition:
Context exists but critical gaps unresolved.

Route:
page-requirement-gap-analysis

## Gap Resolution Needed

Condition:
Blocking gaps exist.

Route:
page-requirement-discovery-qna

## Strategy Missing

Condition:
Requirements stable but strategy absent.

Route:
page-strategy-definition

## Content Structure Missing

Condition:
Strategy exists but no structured content draft.

Route:
content-first-page-draft

## Layout Definition Missing

Condition:
Content draft exists but no wireframe spec.

Route:
wireframe-specification

## Expert Review Required

Condition:
Wireframe exists but risks not reviewed.

Route:
multi-role-review

## Cross-Functional Alignment Required

Condition:
Multi-role review exists and any of the following are true:

- major tradeoffs remain unresolved
- implementation feasibility is disputed
- CTA strategy is disputed
- responsive behavior is disputed
- architecture concerns exist
- designer decision space is unclear
- accepted risks are not documented
- ownership for open concerns is missing

Route:
cross-functional-design-alignment

## Design Handoff Needed

Condition:
Alignment passed or no material alignment issues remain.

Route:
designer-handoff-brief

## Retrospective Eligible

Condition:
Designer brief exists and feedback or outcomes exist.

Route:
workflow-retrospective
