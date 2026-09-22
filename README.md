# Secure Connected Product Reference Architecture

A reference security architecture for connected embedded products spanning device, edge, cloud and AI-enabled services.

## Reference architecture

```
+---------------- Embedded Device ----------------+
| Secure/Measured Boot | TPM/TEE | Device Identity|
| Secure Storage       | Signed Update            |
+-----------------------+--------------------------+
                        |
                 mTLS / device PKI
                        |
+------------------- Edge / Gateway ---------------+
| Protocol termination | policy | local isolation |
+-----------------------+--------------------------+
                        |
                 authenticated API
                        |
+--------------------- Cloud -----------------------+
| API Gateway | IAM | Workload Identity | KMS/HSM  |
| Services    | Data | Monitoring        | Updates  |
+-----------------------+--------------------------+
                        |
+------------------ AI Services --------------------+
| Model gateway | RAG | agent/tool policy | audit  |
+--------------------------------------------------+
```

## Core security principles
- Establish device identity from provisioning onward.
- Protect boot and update trust chains.
- Prefer short-lived/scoped workload identities over shared secrets.
- Separate authentication, authorization and cryptographic key lifecycle concerns.
- Treat cloud and AI services as extensions of the product threat model.
- Maintain vulnerability, dependency and cryptographic inventories across lifecycle.
- Design for key/certificate rotation and future cryptographic migration.

## Design documentation
See [trust-boundaries.md](trust-boundaries.md), [device-identity-and-pki.md](device-identity-and-pki.md), and [secure-update.md](secure-update.md).

All scenarios are fictional reference designs and contain no employer/customer architecture.
