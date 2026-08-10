# Governance

Clinical LiDAR Framework is an early-stage open-source research project.

## Maintainer

The repository maintainer is Manu Faujdar. The maintainer is responsible for
reviewing pull requests, releases, dependency/provenance changes, and safety
language. A maintainer may reject a change that increases clinical risk,
privacy risk, licensing uncertainty, or measurement overclaiming.

## Contributions

Contributions are welcome when they include tests, documentation, provenance,
and a clear statement of what remains unvalidated. See
[CONTRIBUTING.md](CONTRIBUTING.md). Changes involving patient data, clinical
claims, regulated intended use, or device SDK redistribution require explicit
review before merge.

## Clinical and research decisions

This repository does not provide clinical governance. Any study or deployment
must have its own responsible clinical investigator, privacy/security owner,
calibration/validation plan, institutional approvals, and intended-use review.
Open-source maintainership is not clinical sign-off.

## Releases

Releases should update [CHANGELOG.md](CHANGELOG.md), run the full CI workflow,
confirm license/provenance boundaries, and state unresolved limitations. A
version tag does not imply clinical validation or regulatory clearance.
