# This repository and the AgenTrust Marketplace PR

This repository is the canonical standalone source:

https://github.com/MMM777-ai/OntoGuard-decision-authorization

It is not the AgenTrust monorepo overlay. Do not treat the tree as
`integrations/ontoguard-decision-authorization/` until you copy it into a
fork of `agentrust-io/integrations`.

## Standalone use

```bash
python -m pip install -e ".[test]"
pytest -q
```

## Marketplace PR

1. Fork `agentrust-io/integrations`.
2. Copy this repository's integration files into:
   `integrations/ontoguard-decision-authorization/`
3. Copy or adapt a monorepo-shaped workflow at the fork root that installs
   `pip install -e "integrations/ontoguard-decision-authorization[test]"`.
4. From the integrations repo root run:
   `python scripts/generate_marketplace_catalog.py`
5. Run the integration tests and TRACE Level-0 suite.
6. After a green run, set `tested_against` in `integration.yaml` to the
   exact `agentrust-trace` and `agentrust-trace-tests` versions used.
7. Open one integration PR.

Do not submit an internal OntoGuard converter. Do not claim TRACE
conformance until the published `trace-tests verify --level 0` job is green.

Counsel should review the final contribution and applicable OntoGuard
patent claims before the PR.

## PR title

`Add OntoGuard Decision Authorization TRACE adapter`
