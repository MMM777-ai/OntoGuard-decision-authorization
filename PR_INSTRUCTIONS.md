# Marketplace PR

This tree is the integration directory to copy into a fork of
`agentrust-io/integrations`:

```
integrations/ontoguard-decision-authorization/
```

Do not submit OntoGuard core. Do not claim L5 or production non-bypassability.

## Before opening the PR

1. `pytest -q` from this directory (or from the integrations repo after copy).
2. `python examples/controlled-execution-proof-2026-09-17/verify_proof.py`
3. Let GitHub Actions install current `agentrust-trace` / `agentrust-trace-tests`.
   Only then set `tested_against` to the exact versions from that green run.
4. From the integrations repo root: `python scripts/generate_marketplace_catalog.py`

## PR title

`Add OntoGuard Decision Authorization TRACE adapter`
