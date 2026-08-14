# Privacy and data boundary

Status: local research software only. This file is a technical privacy
boundary, not a jurisdiction-specific privacy policy for clinical deployment.

## Current distribution

Examples and tests use synthetic manifests. The browser photo workflow keeps
image pixels in browser memory and stores numeric summaries locally; the
optional loopback service stores bounded numeric summaries and audit metadata.
The project does not include patient images, identifiers, model weights, or
vendor SDK binaries. Do not use the prototype with real patient or clinical
data without the approvals and controls described in `COMPLIANCE.md`.

Optional depth, segmentation, registration, sensor, and device integrations
may introduce their own data flows and licenses. Those integrations are not
licensed or approved merely because this repository is Apache-2.0.

## Deployment responsibility

Before any real-person or clinical use, the responsible organization must
define intended use, lawful basis or authorization, consent, data minimization,
identity/access, encryption, retention/deletion, audit, incident response,
device/model provenance, reference-method validation, contracts, and required
IRB, BAA, DPA, regulatory, or institutional approvals. A hosted or clinical
deployment must publish its own privacy notice and terms of service. This
repository does not provide those notices.

## Legal and safety boundary

The Apache-2.0 `LICENSE` governs the source code. It does not grant rights to
clinical images, datasets, device SDKs, models, vendor names, or third-party
assets, and it does not establish HIPAA/GDPR/DPDP compliance, regulatory
clearance, diagnosis, prognosis, or treatment suitability. See `NOTICE`,
`REFERENCES.md`, `COMPLIANCE.md`, `SECURITY.md`, and
`OPEN_SOURCE_EXTENSIONS.md`.

Reviewed: 2026-08-14.
