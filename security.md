# Security and Compliance Guardrails

## Purpose

The use of AI and agentic tooling inside Genaixfi must be aligned to security, legal, and engineering standards.

## Baseline guardrails

- treat all AI-generated code as draft output requiring human review
- never commit secrets or tokens to repositories
- use least-privilege team access and repository permissions
- require branch protection for primary branches
- prefer signed or reviewed commits for sensitive repos

## Repo-level controls

- restrict admin access to platform and security stewards
- enable protection rules on default branches
- require PR checks and status validations
- review external integrations before enabling them

## Data handling guidelines

- do not paste production secrets, credentials, or private customer data into AI prompts
- keep repo and environment context limited to what is necessary
- review third-party integrations and automation hooks carefully
- verify that AI usage is consistent with internal governance and compliance expectations

## Security-sensitive workflows

These should receive extra review:

- authentication and authorization logic
- token validation or session management
- file-system and process execution logic
- deployment automation and CI/CD changes
- infrastructure and secret management updates

## Governance checkpoints

- review org access weekly
- review repo permissions monthly
- audit AI- or agent-enabled workflows before rollout to production
- capture exceptions in a written policy or risk register

## Recommended operational stance

AI should reduce friction and accelerate engineering delivery without replacing judgment, accountability, or control.
