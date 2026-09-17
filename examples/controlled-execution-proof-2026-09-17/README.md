# Historical controlled-execution proof (2026-09-17)

This is a captured historical controlled-execution proof from live OntoGuard
ALLOW `2fcdc71e-dc28-4d94-9150-fae4517103f3`.

Its authorization intentionally expires on 2026-09-24.
Signature, digest, handoff, action-binding, and historical execution
evidence remain independently inspectable after expiry, but current
authorization replay is expected to fail once the authorization expires.

Do not weaken expiry validation to keep this static demo green.
Live GitHub Actions generates fresh TRACE material on each run.

This pack does not contain OntoGuard core source. Execution is a controlled
local state change (PENDING → RELEASED), not a bank transfer and not L5.

```bash
python verify_proof.py
python replay_adapter.py
```
