# Fork Protection Policy

This repository is a MiamiCreme fork of World Monitor with an added public-safe GlobalIntel module plan.

The goal is to protect three things at the same time:

1. upstream license compliance,
2. MiamiCreme private business logic,
3. future EmpireOS and DealFlow integrations.

## Core Rule

This fork may be public.

Private EmpireOS and proprietary DealFlow logic must stay private.

Do not copy World Monitor source into private EmpireOS unless the use complies with AGPL-3.0-only or separate commercial terms are obtained.

## Protected Boundaries

### Public-Safe

The following can live in this public fork:

- GlobalIntel module docs,
- artifact contracts,
- public-safe adapter descriptions,
- generic brief shapes,
- generic risk categories,
- public examples without private data,
- attribution and license notes,
- non-proprietary SkillForge mapping.

### Private

The following must not be committed here:

- EmpireOS private workflows,
- personal dashboards,
- private daily priority logic,
- API keys and tokens,
- `.env` files,
- client data,
- buyer lists,
- CRM exports,
- DealFlow scoring formulas,
- underwriting assumptions,
- private outreach scripts,
- private memories or personal decision logs,
- proprietary automation logic.

## AGPL Compliance Reminder

World Monitor source is AGPL-3.0-only.

That means:

- Keep license notices intact.
- Keep upstream attribution intact.
- Treat this fork as public/source-available unless separate commercial terms exist.
- Do not build a private-source proprietary product directly from modified World Monitor source without legal review.
- Prefer APIs, exported artifacts, adapter contracts, and public-safe summaries for EmpireOS usage.

This file is not legal advice. It is an internal project-safety policy.

## Branch Protection Rules

Recommended GitHub settings for `main`:

- Require pull request before merging.
- Require at least one approval.
- Block force pushes.
- Block branch deletion.
- Require conversation resolution.
- Require status checks once CI is active.
- Restrict direct pushes to `main`.

Development should happen on:

```text
develop
```

Feature work should happen on branches like:

```text
feature/globalintel-artifacts
feature/skillforge-adapter
feature/empireos-boundary
feature/dealflow-boundary
```

## Pull Request Checklist

Before merging any PR, confirm:

- [ ] No secrets, keys, tokens, or `.env` files were added.
- [ ] No private EmpireOS logic was added.
- [ ] No proprietary DealFlow scoring or buyer data was added.
- [ ] Upstream license and attribution remain intact.
- [ ] GlobalIntel docs remain public-safe.
- [ ] Any new artifact shape includes evidence, risk, confidence, and next action fields.
- [ ] Any EmpireOS or DealFlow integration is described as a boundary/adapter, not implemented with private logic.
- [ ] The change does not imply official World Monitor branding ownership.

## Adapter Rule

Use adapters to cross boundaries.

```text
World Monitor / GlobalIntel artifact
  -> public-safe adapter contract
  -> private EmpireOS or DealFlow implementation
```

The public fork may define the adapter shape. Private systems own private interpretation, scoring, dashboards, and decisions.

## Incident Rule

If private data or secrets are accidentally committed:

1. Stop work immediately.
2. Revoke exposed credentials.
3. Remove the data from the repo history using proper secret-removal procedures.
4. Rotate any related keys.
5. Audit recent commits.
6. Document the incident privately.

## Golden Rule

If it would reveal how Kohron, EmpireOS, MiamiCreme, DealFlow, a buyer list, a client, or a private decision system actually operates, it does not belong in this public fork.
