# GlobalIntel / DealFlow Boundary

DealFlow can use GlobalIntel to add external risk and opportunity context to deals, but proprietary deal scoring and buyer-matching logic should stay outside this public fork.

## Purpose

GlobalIntel can inform:

- country risk,
- market risk,
- energy risk,
- infrastructure risk,
- supply-chain risk,
- aviation/logistics risk,
- geopolitical exposure,
- local instability,
- financing or commodity pressure.

DealFlow should use that context to improve deal judgment, not to replace underwriting.

## Public-Safe Deal Context Shape

```json
{
  "deal_context_brief": {
    "deal_name": "string",
    "deal_type": "real_estate | business | asset | partnership | unknown",
    "region_scope": "string",
    "global_risk_summary": "string",
    "risk_level": "low | medium | high | critical",
    "buyer_angle": "string",
    "watch_items": ["string"],
    "next_best_action": "string",
    "linked_artifact_id": "string"
  }
}
```

## Private Logic Stays Out

Do not include:

- proprietary scoring formulas,
- buyer lists,
- CRM records,
- seller/buyer private information,
- underwriting assumptions,
- private financing strategy,
- private outreach scripts tied to real people.

## Example Flow

```text
GlobalIntel market/region risk
  -> deal_context_brief
  -> private DealFlow adapter
  -> buyer fit, risk score, outreach, or hold/pass recommendation
```

## Quality Gate

A DealFlow-facing GlobalIntel artifact is useful only when it provides:

- specific deal or region context,
- risk level,
- evidence or source description,
- buyer/operator angle,
- watch items,
- next best action.
