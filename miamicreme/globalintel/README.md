# GlobalIntel Module

GlobalIntel is the MiamiCreme module layer for converting World Monitor intelligence into reusable briefs, risks, decisions, and next actions.

This module should keep the upstream World Monitor app intact while defining a clean adapter surface for SkillForge, EmpireOS, and DealFlow.

## Purpose

World Monitor is a real-time global intelligence dashboard. GlobalIntel turns that intelligence into decision-ready artifacts.

Use GlobalIntel to answer:

- What changed globally that matters?
- What risks should we monitor?
- What could affect a client, deal, market, project, or personal plan?
- What should SkillForge turn into a brief, proposal, risk note, or task?
- What should private EmpireOS surface as a priority or mission?

## Position in the MiamiCreme Stack

```text
SignalBrief  = what people are saying
FrameBrief   = what videos show
GlobalIntel  = what is happening globally
SkillForge   = turns intelligence into plans, artifacts, and delivery gates
EmpireOS     = privately decides what Kohron should do next
DealFlow     = applies risk and opportunity signals to deals
```

## Non-Goals

GlobalIntel should not:

- rebrand the upstream app as a MiamiCreme product without clear attribution,
- copy upstream AGPL source into private EmpireOS,
- expose private EmpireOS workflows in this public repo,
- replace SignalBrief or FrameBrief,
- become the DealFlow scoring engine,
- hide evidence or assumptions.

## AGPL Boundary

The upstream World Monitor source is AGPL-3.0-only. Treat this fork as a public, source-available experiment unless separate commercial terms are obtained.

For private EmpireOS usage, prefer:

1. consuming public APIs or exported artifacts,
2. using adapter contracts,
3. keeping private EmpireOS logic outside this repo,
4. preserving attribution and license notices.

## First Deliverables

- `artifact-contract.md` — GlobalIntel output shape.
- `skillforge-adapter.md` — how GlobalIntel maps into SkillForge artifacts.
- `empireos-boundary.md` — what can and cannot flow into private EmpireOS.
- `dealflow-boundary.md` — how global risk can inform deal analysis without leaking proprietary logic.

## Recommended Artifact Types

- `global_intel_brief`
- `country_risk_brief`
- `market_risk_brief`
- `infrastructure_risk_brief`
- `energy_risk_brief`
- `aviation_risk_brief`
- `deal_context_brief`
- `empireos_alert`

## Quality Gate

A GlobalIntel artifact is not useful unless it includes:

- the decision it supports,
- the affected region, market, asset, client, or deal,
- evidence or source description,
- risk level,
- confidence level,
- assumptions/gaps,
- next best action.
