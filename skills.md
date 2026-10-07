# Agentix Platform Skills

## Purpose

This file defines the most useful GitHub Copilot Enterprise capabilities for Genaixfi and maps them to an internal Agentix operating model. It is intentionally practical, repo-aware, and enterprise-safe.

## Operating principle

The platform must optimize for:

- code understanding across repositories
- repo-aware coding and refactoring
- secure pull request review
- quick diagnosis of failing builds and runtime issues
- governance-aligned delivery workflows
- measurable adoption by engineering teams

## Core capability map

### 1. Code generation

Use Copilot to accelerate implementation while preserving human review and architecture direction.

Best uses:
- scaffold new service and module boundaries
- generate boilerplate and tests
- create internal utilities and scripts
- speed up migrations and repetitive refactors

Governance:
- require peer review before merge
- keep prompts repo- and context-aware
- enforce review of generated code for correctness and security

### 2. Code understanding and navigation

Copilot is most effective when it understands repo intent, architecture, and runtime boundaries.

Best uses:
- explain login flow and auth validation logic
- trace a feature from UI to API to persistence
- identify where configuration, secrets, or routing are managed
- summarize service and domain boundaries

Key practice:
- ask for repository-scoped explanations, not generic responses
- use file- and symbol-aware prompt patterns

### 3. Pull request review

Copilot can act as a high-leverage review assistant for security, correctness, and maintainability.

Best uses:
- identify missing validation or unsafe defaults
- flag injection risks, unsafe deserialization, and edge-case logic
- compare changes against existing patterns
- summarize release impact and migration risks

Rules:
- human review remains mandatory
- use review output as a signal, not a final decision
- separate code quality from policy compliance review

### 4. Test generation and validation assistance

Copilot can help produce or extend tests for critical workflows.

Best uses:
- unit tests for edge cases
- API contract validation
- regression test generation for bug fixes
- CI failure triage with repo context

### 5. Incident and debug support

Copilot is valuable for triaging stack traces, logs, and root-cause analysis.

Best uses:
- narrow likely failure points from error traces
- propose minimal fixes and validation steps
- cross-reference service configuration and env variables
- summarize probable root cause before a human deep dive

### 6. Secure architecture and guardrail support

Use Copilot as an assistant for secure engineering without depending on it as the final security authority.

Best uses:
- review secrets handling and environment patterns
- identify unsafe file permission or process execution patterns
- suggest policy-compliant defaults for auth and API boundaries
- advise on least-privilege models

### 7. Repository-aware multi-agent orchestration

AgentK-inspired architecture suggests a multi-agent operating model, but it must stay governance-aligned.

Best uses:
- domain-specific specialist agents
- planner-orchestrator patterns
- research + implementation + validation hand-offs
- internal knowledge and tooling integration

Guardrails:
- no agent should operate without traceability
- no agent should mutate context without explicit ownership
- all autonomous execution should be constrained by repo, team, and policy layers

## Recommended skill taxonomy for Genaixfi

1. `system-architect`
   - identifies system boundaries and module ownership
2. `repo-analyst`
   - explains architecture, dependencies, and runtime flows
3. `security-reviewer`
   - checks for risky patterns and cloud/infra concerns
4. `test-engineer`
   - generates regression tests and validation plans
5. `incident-triage`
   - analyzes logs, stack traces, and build failures
6. `policy-guardrail`
   - checks for policy alignment before execution or merge
7. `onboarding-coordinator`
   - helps new team members understand code and workflows quickly

## Practical prompts for Genaixfi

Use prompts that ask for repo-aware, action-oriented outputs:

- "Find the login flow in this repo and explain how tokens are validated."
- "Review this PR and call out correctness and security issues."
- "What changed in the auth module last week?"
- "Debug this stack trace and identify the likely root cause."
- "Summarize the service boundaries and who owns this domain."
- "Create a secure implementation plan for this API change."

## Internal usage rules

- Prefer repo-scoped prompts over generic AI questions
- Require human review of all produced code changes
- Treat Copilot as a productivity accelerator, not a source of authority
- Keep agentic workflows traceable, auditable, and bounded
- Never bypass security or policy review using prompt rewriting or circumvention tactics

## Enterprise value

The highest-value Copilot usage for Genaixfi is not raw code generation. It is the combination of:

- code understanding
- security-aware review
- repo-aware debugging
- rapid onboarding
- structured governance

This creates a system where engineering velocity increases without losing control.
