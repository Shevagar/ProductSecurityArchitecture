# Secure Firmware Update

A secure update design should explicitly address authenticity, integrity, version policy, failure recovery and signing-key lifecycle.

```
Build -> release approval -> artifact signing -> distribution
                                      |
Device: download -> verify signature -> version/policy check
       -> safe install -> boot verification -> health/recovery
```

## Threat-driven controls
- Reject unauthenticated or modified firmware.
- Define anti-rollback policy where downgrade creates security risk.
- Separate release authorization from artifact transport.
- Protect signing keys and define rotation/revocation procedures.
- Design power-loss/failure recovery to avoid unsafe partial updates.
- Retain auditable association between product version and released artifact.
