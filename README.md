# AI-Native Product Page Design Workflow

A modular Claude Skills system for running professional product-led website and landing page design workflows.

This repository turns page design from an ad-hoc conversation into a structured, reusable operational system.

The workflow models how experienced product managers, product designers, frontend engineers, architects, and growth teams collaborate to design high-quality product pages.

---

# Why This Exists

Most AI-assisted page design workflows fail because they:

* jump directly into UI generation
* skip strategic thinking
* mix discovery, critique, and implementation together
* lose assumptions between steps
* create endless feedback loops
* lack decision convergence
* produce unstable outputs

This system solves that problem by introducing:

* deterministic workflow sequencing
* explicit readiness gates
* structured artifacts
* cross-functional alignment
* assumption tracking
* revision loops
* reusable operational knowledge

The goal is not "fully automated design."

The goal is:

> operationalizing high-quality product thinking.

Final visual execution should still involve professional designers.

---

# System Architecture

```text
page-design-orchestrator
        ↓
11 Specialized Workflow Skills
```

The orchestrator manages workflow state, routing, readiness validation, rollback logic, and artifact continuity.

Each step is intentionally isolated into a dedicated Claude Skill with:

* stable inputs
* stable outputs
* explicit goals
* deterministic execution
* reusable artifacts
* independent testability

---

# Workflow

```text
1. page-task-intake
2. business-context-structuring
3. page-requirement-gap-analysis
4. page-requirement-discovery-qna
5. page-strategy-definition
6. content-first-page-draft
7. wireframe-specification
8. multi-role-review
9. cross-functional-design-alignment
10. designer-handoff-brief
11. workflow-retrospective
```

---

# Workflow Philosophy

This system follows several core principles:

## 1. Strategy Before UI

The workflow intentionally delays visual exploration until:

* business context is clear
* user context is clear
* narrative strategy exists
* CTA strategy exists
* trust strategy exists

---

## 2. Content Before Design

The workflow treats:

* information architecture
* messaging hierarchy
* narrative sequencing
* CTA logic

as upstream dependencies for design.

---

## 3. Critique ≠ Alignment

The system separates:

### Multi-Role Review

from

### Cross-Functional Alignment

Because identifying problems is fundamentally different from resolving tradeoffs.

---

## 4. Designers Need Constraints And Freedom

The workflow preserves:

* strategic intent
* implementation boundaries
* conversion goals

while still preserving:

* creative exploration
* layout experimentation
* visual authorship

---

## 5. Workflows Should Compound

The retrospective system turns:

* failures
* friction
* decisions
* assumptions
* experiments

into reusable operational knowledge.

---

# Included Skills

## Core Workflow Skills

| Step | Skill                               | Purpose                                             |
| ---- | ----------------------------------- | --------------------------------------------------- |
| 1    | `page-task-intake`                  | Normalize raw requests into structured design tasks |
| 2    | `business-context-structuring`      | Structure business and user context                 |
| 3    | `page-requirement-gap-analysis`     | Detect missing critical inputs                      |
| 4    | `page-requirement-discovery-qna`    | Resolve blocking requirement gaps                   |
| 5    | `page-strategy-definition`          | Define narrative and conversion strategy            |
| 6    | `content-first-page-draft`          | Create structured page content architecture         |
| 7    | `wireframe-specification`           | Produce lo-fi layout and interaction structure      |
| 8    | `multi-role-review`                 | Perform structured expert critique                  |
| 9    | `cross-functional-design-alignment` | Resolve tradeoffs and align execution               |
| 10   | `designer-handoff-brief`            | Create designer-ready execution brief               |
| 11   | `workflow-retrospective`            | Extract reusable operational learnings              |

---

## System-Level Skill

| Skill                      | Purpose                                                                                      |
| -------------------------- | -------------------------------------------------------------------------------------------- |
| `page-design-orchestrator` | Controls routing, state management, readiness gates, rollback logic, and workflow continuity |

---

# Repository Structure

Each skill follows Anthropic Claude Skills best practices.

```text
skill-name/
  SKILL.md
  principles.md
  frameworks/
  templates/
  checklists/
  examples/
  tests/
```

This keeps:

* execution logic
* reusable frameworks
* operational templates
* examples
* validation logic

modular and composable.

---

# Design Goals

This system is optimized for:

* SaaS landing pages
* product marketing pages
* onboarding flows
* feature pages
* AI product websites
* growth pages
* enterprise product pages

It is especially useful for teams that:

* move quickly
* collaborate cross-functionally
* use AI heavily in PM/design workflows
* want repeatable product thinking
* need higher signal design reviews

---

# What This System Is NOT

This is NOT:

* a one-shot website generator
* a Figma replacement
* a UI design system
* a no-code page builder
* an autonomous design agent

It is a:

> product design operating system.

---

# Key Operational Concepts

## Readiness Gates

Steps cannot advance unless:

* required artifacts exist
* blocking gaps are resolved
* assumptions are acknowledged
* tradeoffs are documented

---

## Revision Loops

The workflow supports controlled rollback when:

* strategy is weak
* UX risk is severe
* implementation becomes infeasible
* alignment fails

---

## Assumption Tracking

Assumptions persist across:

* reviews
* alignment
* handoffs
* retrospectives

They are treated as workflow objects.

---

## Artifact Continuity

The orchestrator preserves:

* decisions
* rationale
* accepted risks
* unresolved concerns
* ownership

throughout the workflow lifecycle.

---

# Recommended Usage

## 1. Install Skills

Place the skill folders into your Claude Skills environment.

---

## 2. Start With The Orchestrator

Use:

```text
page-design-orchestrator
```

as the top-level entry point.

The orchestrator determines:

* current workflow state
* missing artifacts
* next valid step
* rollback conditions
* alignment requirements

---

## 3. Execute Step-By-Step

Allow each specialized skill to:

* consume upstream artifacts
* produce stable outputs
* preserve workflow continuity

Do not skip steps unless intentionally customizing the workflow.

---

# Recommended Team Roles

This workflow works best when informed by:

* Product Managers
* Product Designers
* Frontend Engineers
* Architects / Tech Leads
* Growth / Marketing
* QA / Accessibility reviewers
* Stakeholders

The system intentionally models cross-functional product development dynamics.

---

# Inspirations

This project is heavily inspired by:

* Anthropic Claude Skills architecture
* real-world product design operations
* product-led growth workflows
* UX systems thinking
* cross-functional product development practices

---

# Future Directions

Potential extensions:

* visual design generation integration
* Figma synchronization
* analytics-aware retrospectives
* automated design QA
* implementation planning workflows
* component system integration
* experimentation frameworks

---

# License

MIT

---

# Contributing

Contributions are welcome, especially around:

* additional workflow skills
* better orchestration patterns
* improved review frameworks
* stronger testing structures
* integration patterns
* real-world case studies

---

# Final Note

The purpose of this repository is not to automate designers out of the process.

The purpose is to operationalize better product thinking so that:

* designers receive higher-quality inputs
* engineers receive clearer constraints
* PMs make more consistent decisions
* teams converge faster
* workflows become reusable systems instead of fragile conversations
