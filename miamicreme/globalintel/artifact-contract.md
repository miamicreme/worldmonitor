# GlobalIntel Artifact Contract

This contract defines the public-safe output shape for GlobalIntel artifacts.

The goal is to let SkillForge, EmpireOS, DealFlow, reports, and proposals consume global intelligence without coupling themselves to the full World Monitor app runtime.

## Artifact Shape

```json
{
  "artifact_id": "string",
  "artifact_contract_version": "0.1.0",
  "artifact_type": "global_intel_brief | country_risk_brief | market_risk_brief | infrastructure_risk_brief | energy_risk_brief | aviation_risk_brief | deal_context_brief | empireos_alert",
  "source_module": "globalintel",
  "title": "string",
  "summary": "string",
  "decision_supported": "string",
  "region_scope": "global | country | region | city | market | route | asset | client | deal",
  "topic_scope": ["geopolitical", "market", "energy", "infrastructure", "aviation", "climate", "cyber", "military", "finance", "supply_chain", "public_health", "other"],
  "risk_level": "low | medium | high | critical",
  "confidence": "low | medium | high",
  "time_horizon": "immediate | 24h | 7d | 30d | 90d | long_term",
  "evidence": [
    {
      "source_type": "feed | api | map_layer | country_index | finance_signal | user_context | assumption | manual_note",
      "source": "string",
      "claim": "string",
      "confidence": "low | medium | high",
      "timestamp": "optional string",
      "location": "optional string"
    }
  ],
  "risks": ["string"],
  "opportunities": ["string"],
  "watch_items": ["string"],
  "next_actions": ["string"],
  "quality_gate": {
    "status": "pass | warn | fail",
    "notes": "string"
  },
  "render_targets": ["markdown", "html", "skillforge", "empireos", "dealflow", "proposal", "report"]
}
```

## Required Fields

- `artifact_id`
- `artifact_contract_version`
- `artifact_type`
- `source_module`
- `title`
- `summary`
- `decision_supported`
- `region_scope`
- `topic_scope`
- `risk_level`
- `confidence`
- `time_horizon`
- `evidence`
- `risks`
- `next_actions`
- `quality_gate`

## Quality Gate Rules

Use `pass` when:

- the decision is clear,
- evidence is present,
- risk level is justified,
- confidence is stated,
- next actions are specific.

Use `warn` when:

- evidence is thin,
- source freshness is unknown,
- confidence is low,
- assumptions materially affect the recommendation.

Use `fail` when:

- no evidence is available,
- the decision supported is unclear,
- risk level cannot be justified,
- the artifact cannot produce a useful next action.
