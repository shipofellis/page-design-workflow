
# Test Cases

## Test 1 — Premature Handoff

Input:
Multi-role review contains unresolved engineering and design concerns, user requests designer brief.

Expected:
- block direct handoff
- route to cross-functional-design-alignment
- explain unresolved tradeoffs

## Test 2 — No Material Alignment Needed

Input:
Multi-role review passes with low risks and no disputed tradeoffs.

Expected:
- allow routing to designer-handoff-brief
- note alignment not required

## Test 3 — Alignment Failed

Input:
Alignment report marks blocked due to architecture concern.

Expected:
- block handoff
- route back to wireframe-specification or page-strategy-definition depending on issue

## Test 4 — Full Workflow

Input:
All artifacts plus launch feedback.

Expected:
- route to workflow-retrospective
- preserve assumption and decision history
- maintain artifact continuity
