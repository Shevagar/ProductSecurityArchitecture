# Trust Boundaries

| Boundary | Primary concern | Representative controls |
|---|---|---|
| Boot ROM/firmware | Code authenticity | Hardware root of trust, verified boot chain |
| Application/TEE or TPM | Key isolation | Protected key operations, authorization policy |
| Device/network | Device impersonation | Device identity, mutual authentication, certificate lifecycle |
| Edge/cloud | Service impersonation and privilege | mTLS, workload identity, least privilege |
| API/service | Broken authorization | Central identity, scoped authorization, validation |
| Cloud/AI | Data and action misuse | Data policy, model gateway, tool authorization, audit |
| Build/product | Supply-chain compromise | Controlled build, provenance, signing, dependency/SBOM management |
