# GlobalIntel / EmpireOS Boundary

EmpireOS is private. This public fork should not contain private EmpireOS logic, private memory, personal dashboards, or client-specific workflows.

## Purpose

GlobalIntel can produce public-safe intelligence artifacts that EmpireOS may consume privately.

EmpireOS should decide:

- whether the signal matters to Kohron,
- whether it affects today's priorities,
- which AI team member should act,
- whether a client, deal, project, or personal plan needs attention.

## Allowed Public Interface

This repo may define public-safe structures like:

```json
{
  "empireos_alert": {
    "linked_artifact_id": "string",
    "priority": "low | medium | high | urgent",
    "mission_type": "research | decide | follow_up | sell | build | avoid | monitor",
    "risk_level": "low | medium | high | critical",
    "next_best_action": "string",
    "time_horizon": "immediate | 24h | 7d | 30d | 90d | long_term"
  }
}
```

## Private Implementation Stays Out

Do not include:

- personal priorities,
- private daily schedule logic,
- financial data,
- client CRM details,
- deal pipeline data,
- private memories,
- credentials,
- private automations,
- personal decision logs.

## EmpireOS Consumption Pattern

```text
GlobalIntel artifact
  -> public-safe empireos_alert summary
  -> private EmpireOS adapter
  -> mission card / daily priority / AI team task / watch item
```

## Quality Gate

An EmpireOS-facing GlobalIntel alert is usable only when it includes:

- clear reason it matters,
- risk level,
- time horizon,
- next best action,
- linked source artifact,
- confidence level.
