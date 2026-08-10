# Security and privacy

This is research software, not a clinical system. Do not commit patient data,
identifiers, screenshots, device captures, access tokens, or production
credentials. Use the synthetic manifest as the default test input.

If you find a security or privacy issue, do not publish sensitive details in a
public issue. Use GitHub's private [Security Advisories](https://github.com/manufaujdar/clinical-lidar-framework/security/advisories/new)
when available. Include a minimal reproduction without protected health
information, credentials, or raw captures.

The core analyzers have no network client or cloud dependency. The optional
webapp uses browser-local storage, and the optional local service uses loopback
SQLite with numeric-summary-only validation and an optional local token. A
future sensor adapter must define capture retention, access control, encryption,
audit, deletion, and consent requirements before handling clinical data.

Security reports are triaged by the repository maintainer. Public source
availability does not imply a security SLA, HIPAA compliance, or suitability for
protected health information.
