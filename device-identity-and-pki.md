# Device Identity and PKI

## Lifecycle
```
Manufacturing / enrollment
        -> unique device identity
        -> protected private-key operation
        -> certificate issuance
        -> mutual authentication
        -> renewal / rotation
        -> revocation / decommissioning
```

Private keys should be generated/protected according to the platform threat model; designs may use TPMs, secure elements, TEEs or other hardware-backed facilities where appropriate. Certificate identity is distinct from application authorization: a valid device certificate should not automatically grant unrestricted product privileges.

## Architecture questions
- What establishes initial device trust?
- Can a credential be cloned or exported?
- How is ownership/enrollment authorized?
- How are certificates renewed before expiry?
- How is compromise/revocation propagated?
- What happens at factory reset, transfer and end of life?
