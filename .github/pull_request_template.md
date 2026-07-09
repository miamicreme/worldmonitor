## Summary

<!-- Brief description of what this PR does -->

## Type of change

- [ ] Bug fix
- [ ] New feature
- [ ] New data source / feed
- [ ] New map layer
- [ ] Refactor / code cleanup
- [ ] Documentation
- [ ] CI / Build / Infrastructure
- [ ] GlobalIntel module / adapter docs

## Affected areas

- [ ] Map / Globe
- [ ] News panels / RSS feeds
- [ ] AI Insights / World Brief
- [ ] Market Radar / Crypto
- [ ] Desktop app (Tauri)
- [ ] API endpoints (`/api/*`)
- [ ] Config / Settings
- [ ] MiamiCreme GlobalIntel module
- [ ] SkillForge adapter boundary
- [ ] EmpireOS boundary
- [ ] DealFlow boundary
- [ ] Other: <!-- specify -->

## Protection Checklist

- [ ] No API keys, secrets, tokens, or `.env` files were committed.
- [ ] No private EmpireOS logic, personal dashboards, private memory, or private decision logs were added.
- [ ] No proprietary DealFlow scoring formulas, buyer lists, CRM records, underwriting assumptions, or private outreach scripts were added.
- [ ] Upstream World Monitor attribution and AGPL-3.0-only license notices remain intact.
- [ ] Any GlobalIntel addition is public-safe and does not imply ownership of official World Monitor branding.
- [ ] Any EmpireOS or DealFlow integration is documented as a boundary/adapter unless it is intentionally public-safe.
- [ ] The change follows `PROTECTION.md`.

## Artifact Quality Checklist

For GlobalIntel artifacts or docs:

- [ ] Decision supported is clear.
- [ ] Region/topic scope is clear.
- [ ] Risk level is stated.
- [ ] Confidence level is stated.
- [ ] Evidence or source description is included.
- [ ] Assumptions/gaps are visible.
- [ ] Next best action is specific.

## Original World Monitor Checklist

- [ ] Tested on [worldmonitor.app](https://worldmonitor.app) variant
- [ ] Tested on [tech.worldmonitor.app](https://tech.worldmonitor.app) variant (if applicable)
- [ ] New RSS feed domains added to `api/rss-proxy.js` allowlist (if adding feeds)
- [ ] TypeScript compiles without errors (`npm run typecheck`)

## Documentation Alignment Checklist

<!-- Required for documentation-alignment PRs that touch methodology, API/MCP contracts, generated docs, examples, Redis keys, CII, CRI, news, digest, or briefing. Mark N/A only when this PR does not publish or change documentation claims. -->

- [ ] Claim ledger attached or linked
- [ ] All required Audit Council role signoffs attached
- [ ] Generated docs regenerated from proto where applicable
- [ ] Fixture-backed examples recomputed
- [ ] Redis writers/readers enumerated for every documented key

## License / Safety Notes

Mention any license, attribution, privacy, or data-boundary concerns reviewers should know.

## Screenshots

<!-- If applicable, add screenshots or screen recordings -->
