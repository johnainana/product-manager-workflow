---
name: product-manager-workflow
description: End-to-end product manager workflow for turning ideas, problems, requests, or opportunities into validated PM deliverables. Use when the user asks to clarify a product idea, define a problem, write or review a PRD, create user stories and acceptance criteria, design metrics, plan a roadmap, structure A/B tests or validation, plan delivery, run product reviews, analyze competitors, or prepare launch retrospectives.
---

# Product Manager Workflow

Use this skill to run a complete product manager workflow from discovery interview to structured deliverables. Default to an interview-first process: ask one question at a time, do not invent missing facts, check information completeness, then produce only the deliverables that are sufficiently supported by confirmed information.

## Core Rules

- Follow the user's language. If the user writes in Chinese, respond in Chinese; if English, respond in English. Keep common product and technical terms in their usual form when helpful.
- Ask one question at a time during discovery.
- Show the current interview stage and progress when asking. In Chinese, use a format such as `当前阶段：1/9 背景与触发原因`.
- Do not repeat back every user answer by default. Only restate for confirmation when the answer is ambiguous, contradictory, or important enough to affect later work.
- When an answer is too broad, provide 2-4 concrete options to help the user choose, without deciding for them.
- Do not make assumptions or fill gaps with industry guesses. If information is missing, ask for it or mark the item as not ready.
- Require evidence sources for user needs or problem claims. If no evidence exists, mark the need as unverified.
- Before final deliverables, run an information completeness check and ask the user whether to continue discovery or generate the supported outputs.
- Preserve `待确认` and `未验证` markers in formal outputs. Do not hide missing or unsupported information.
- Do not browse the web unless the user explicitly asks. For external facts such as competitor state, pricing, regulations, platform policies, or API capabilities, mark facts as unverified when not checked.
- Use the minimum process needed for the request, but keep the workflow auditable: every output should trace to confirmed user input, cited evidence, or an explicit user decision.
- Include non-goals only when the request is complex, cross-functional, high-risk, likely to expand in scope, or the user asks for them.
- Do not suggest or launch subagents by default. Use the multi-role review checklist instead.
- Default to standard detail: complete enough for collaboration, but not exhaustive unless the user asks for a detailed version.

## Discovery Interview

Ask through these stages in order. Ask only one question per message, and stay in the current stage until the answer is clear enough to continue.

1. Background and trigger
2. Goal and business outcome
3. Users and use scenarios
4. Current problem and evidence
5. Success metrics
6. Scope boundaries and non-goals when needed
7. Constraints, dependencies, and risks
8. Priority and milestones
9. Launch validation and retrospective approach

Prefer concrete questions over generic prompts. Examples:

- "What triggered this request now?"
- "Which user segment is most affected?"
- "What evidence shows this problem exists?"
- "What outcome would make this work successful?"
- "What constraint is least flexible: time, scope, quality, compliance, or resources?"

## Completeness Check

Before creating formal deliverables, summarize:

- Confirmed information
- Missing information
- Unverified claims or evidence gaps
- Whether there is enough information for each requested deliverable
- Recommended next step: continue interviewing, narrow scope, or generate supported outputs

Ask for user confirmation before proceeding from the completeness check to final deliverables.

Use this output shape:

- Confirmed information
- Missing information, why it matters, and the suggested follow-up question
- Unverified information, current claim, and needed evidence
- Which deliverables can be generated, and why
- Recommended next step: continue interviewing, narrow scope, or generate supported outputs

## Deliverable Priority

When the user asks for full-process output, produce deliverables in this default order:

1. Requirement clarification summary
2. Full engineering-collaboration PRD
3. User stories and acceptance criteria
4. Metrics system and success criteria
5. Roadmap and milestones
6. A/B test or validation plan
7. Project delivery plan
8. Review checklist
9. Launch retrospective template

Generate only deliverables with enough confirmed information. If a deliverable is not ready, explain why in the completeness check instead of forcing a partial document. When generating multiple deliverables, start with an output table of contents, then write each deliverable in order.

Add competitor analysis when the user asks for competitor research, competitive review, market comparison, positioning, or benchmark analysis.

Load `references/templates.md` when writing these deliverables or when the user asks for a template.

## PRD Standard

Default to a full engineering-collaboration PRD. Cover the material needed by product, design, engineering, QA, data, and operations:

- Context and problem
- Goals and business outcomes
- Target users and scenarios
- Evidence and source quality
- Scope, functional requirements, and non-functional requirements
- User stories and acceptance criteria
- States, edge cases, permissions, errors, and boundary conditions
- Page and interaction notes, prototype links, and flow diagram locations
- Metrics, event tracking, and validation plan
- Dependencies, risks, rollout, and rollback
- Milestones and owners

## Product Principles

Use these principles during interviews, reviews, and output checks:

- Define the problem before proposing solutions.
- Identify specific users and scenarios.
- Require success metrics.
- State non-goals when complexity or scope risk requires it.
- Cover boundary conditions and exception paths.
- Include tracking and validation plans.
- Identify dependencies, risks, and launch strategy.

## Method Defaults

- Metrics: use North Star metric, input metrics, and guardrail metrics.
- Prioritization: choose the method by context, such as RICE, MoSCoW, value-cost matrix, Kano, or impact-effort. Explain why the method fits.
- Requirement priority labels: follow the user's team convention. If no convention is provided, use `P0 / P1 / P2`.
- Competitor analysis: default to structured analysis covering target users, core flows, feature matrix, pricing or business model, strengths, weaknesses, and opportunity points.
- Delivery plan: define deliverables, owners, milestones, dependencies, completion criteria, and risks.
- Launch retrospective: cover goal review, actual results versus expectation, metric performance, user feedback, issues or incidents, decision review, lessons learned, and follow-up actions.

## Review Checklist

Use this checklist for PM review or before handoff:

- Problem is clear and evidence-backed.
- Target user and scenario are specific.
- Outcome and success metrics are measurable.
- Scope is clear enough for design and engineering.
- Non-goals are present when needed.
- Requirements include edge cases, errors, states, and permissions.
- Acceptance criteria are testable.
- Metrics and event tracking support validation.
- Dependencies and risks have owners or mitigation.
- Rollout, rollback, and post-launch review are defined.
