# GlobalIntel to SkillForge Adapter

This adapter maps GlobalIntel outputs into SkillForge artifacts, recipes, packs, and quality gates.

## Purpose

SkillForge should consume GlobalIntel as an intelligence source, not as a runtime dependency.

GlobalIntel provides global risk and opportunity context. SkillForge turns that context into:

- briefs,
- proposals,
- business ops assessments,
- DealFlow context,
- EmpireOS alerts,
- implementation plans,
- client-ready reports.

## Mapping

| GlobalIntel Artifact | SkillForge Artifact |
|---|---|
| `global_intel_brief` | `global_intel_brief` |
| `country_risk_brief` | `global_intel_brief` or `deal_brief` |
| `market_risk_brief` | `proposal`, `business_ops_assessment`, or `deal_brief` |
| `infrastructure_risk_brief` | `business_ops_assessment` or `deal_brief` |
| `energy_risk_brief` | `business_ops_assessment`, `deal_brief`, or `proposal` |
| `aviation_risk_brief` | `global_intel_brief` or `business_ops_assessment` |
| `deal_context_brief` | `deal_brief` |
| `empireos_alert` | private EmpireOS mission/priority object |

## Recommended SkillForge Recipes

Future SkillForge recipes that can consume GlobalIntel:

- `globalintel-to-brief.md`
- `globalintel-to-deal-risk.md`
- `globalintel-to-business-ops.md`
- `globalintel-to-proposal.md`
- `globalintel-to-empireos-alert.md`

## Input Requirements

The adapter should receive:

- GlobalIntel artifact,
- decision supported,
- target customer/client/deal/project if any,
- time horizon,
- risk tolerance,
- desired output format.

## Output Requirements

The adapter should output:

- SkillForge-compatible artifact,
- evidence array,
- risk list,
- assumptions/gaps,
- next actions,
- quality gate.

## Example Flow

```text
World Monitor data / brief
  -> GlobalIntel artifact
  -> SkillForge adapter
  -> global_intel_brief or deal_brief
  -> SkillForge recipe
  -> proposal, client risk note, EmpireOS mission, or DealFlow context
```

## Boundary Rule

SkillForge should not import World Monitor app internals directly. It should consume exported briefs, API responses, CLI output, MCP output, or manually prepared artifacts.
