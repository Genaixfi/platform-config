# Governance Model

## Purpose

This document defines the enterprise governance model for Genaixfi's GitHub Copilot adoption.

## Core principles

- secure by default
- repo-aware by design
- team-scoped access and ownership
- auditable activity
- human approval remains mandatory for production changes

## Governance layers

### 1. Repository access and ownership

- Each repository must have an explicit owner or owning team
- Access should be granted by team, not by ad hoc permissions
- Shared repos should have a clear default branch and protection rules

### 2. Copilot access policy

- Copilot Enterprise should be assigned by engineering team and role
- Pilot teams should be allowed first, then broad expansion
- Policy controls should be reviewed periodically as adoption grows

### 3. Feature control

Use GitHub policy controls to manage:
- feature access
- model availability
- agent-related capabilities
- org-level rollout phases

### 4. Code review policy

- All production code changes require code review
- Security-sensitive changes require additional review from a designated owner
- PR comments and review outcomes should be captured in the normal GitHub flow

### 5. Auditability and telemetry

- Review GitHub audit logs and access changes regularly
- Maintain repository ownership records and team membership
- Validate that access is aligned to work responsibilities

## Recommended Genaixfi org structure

- `owners` — organization owners and platform stewards
- `engineering` — core software development teams
- `platform` — CI/CD, infra, and developer tooling
- `security` — governance and compliance review
- `product` — business and product-facing engineering coordination

## Decision ownership

- Org owner: `ricardotgomes11`
- Platform stewards: define repo and policy defaults
- Team leads: approve team access and onboarding
- Security review: validate high-risk changes and policy exceptions

## Governance cadence

- weekly: access and usage review
- monthly: policy tuning and adoption review
- quarterly: roadmap, metrics, and capability evaluation
