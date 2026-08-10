# Clinical LiDAR Framework

[![Tests](https://github.com/manufaujdar/clinical-lidar-framework/actions/workflows/test.yml/badge.svg)](https://github.com/manufaujdar/clinical-lidar-framework/actions/workflows/test.yml)
[![License: Apache-2.0](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](LICENSE)

Clinical LiDAR Framework (CLF) is an open-source, vendor-neutral research
framework for calibrated wound-surface measurement and longitudinal comparison.
It provides deterministic geometry utilities, phantom-calibration helpers,
validation metrics, device-depth contracts, a local numeric store, and a small
paired-photo review webapp.

The name describes the research domain. This software is not a clinical device,
does not diagnose or score healing, and must not be used to make treatment,
triage, or patient-safety decisions.

## What is included

- Plane-relative depth and volume metrics from calibrated depth grids.
- Longitudinal geometry signals: decreasing, stable/mixed, increasing, or
  insufficient data/quality.
- Paired-photo planimetry with scale, frame, lighting, image-quality, and
  outline-review gates.
- Dependency-free phantom calibration and validation metrics.
- Explicit adapters for native depth, optional OpenCV calibration, optional
  Open3D registration, and optional SAM 2 segmentation integration.
- Local-first browser storage and an optional loopback SQLite summary service.
- Synthetic-only examples and tests; no patient images, model weights, or SDK
  binaries are included.

## Quick start

Requires Python 3.10+.

```bash
python3 -m unittest discover -s tests -v
python3 -m clinical_lidar examples/synthetic_progress_manifest.json
python3 -m clinical_lidar.research_cli calibrate \
  examples/synthetic_calibration_manifest.json
python3 -m clinical_lidar.research_cli validate \
  examples/synthetic_validation_manifest.json
```

Start the local webapp:

```bash
python3 -m http.server 8766 --directory webapp
```

Open <http://127.0.0.1:8766/>. The photo route keeps image pixels in browser
memory and stores numeric history locally; it does not turn an ordinary RGB
camera into a true depth sensor.

## Repository layout

```text
clinical_lidar/             importable Python package and device-neutral APIs
  surface_metrics.py        calibrated plane-relative depth metrics
  progress_tracker.py       longitudinal geometry comparison
  paired_comparison.py      paired-photo geometry and quality gates
  calibration.py            dependency-free phantom calibration
  validation.py             segmentation, measurement, repeatability metrics
  depth_provider.py          true-depth frame contract
  local_storage.py           numeric-only SQLite boundary
  local_service.py           loopback HTTP service
  ml/                        optional, provenance-first model adapters
webapp/                     dependency-free photo/depth browser interface
tools/frontend_agent/      deterministic supervised frontend review agent
examples/                   synthetic manifests only
tests/                      deterministic regression tests, including the review agent
docs in root                compliance, security, validation, and provenance
```

## Research boundary

Measurements describe geometry or image change only. They are not wound healing,
recovery, infection, tissue viability, prognosis, or treatment-response scores.
RGB segmentation is an operator-assistive heuristic. The depth pathway requires
calibration, device provenance, repeatability testing, and an appropriate
reference method before any clinical research claim is considered.

Before real clinical data or deployment, the project needs intended-use and
risk review, privacy/security controls, consent and retention rules, phantom and
reference-method validation, segmentation and registration validation,
demographic/setting robustness analysis, and any required institutional,
regulatory, IRB, BAA, or DPA approvals. See [COMPLIANCE.md](COMPLIANCE.md),
[SECURITY.md](SECURITY.md), and [VALIDATION_PROTOCOL.md](VALIDATION_PROTOCOL.md).

## Licensing and provenance

The source code is released under the Apache License 2.0, selected for its
permissive use terms, patent grant, and suitability for academic, community,
and commercial collaboration. See [LICENSE](LICENSE) and [NOTICE](NOTICE).

Datasets, clinical images, device SDKs, model weights, and third-party assets
are not covered automatically. Every future addition must carry its own license
and provenance record. See [REFERENCES.md](REFERENCES.md) and
[OPEN_SOURCE_EXTENSIONS.md](OPEN_SOURCE_EXTENSIONS.md).

## Contributing

Use synthetic fixtures or explicitly approved de-identified research data. Never
commit patient identifiers, clinical captures, screenshots containing sensitive
information, credentials, or proprietary SDK binaries. Run the full test suite
before opening a change and preserve the research-only language. See
[CONTRIBUTING.md](CONTRIBUTING.md).

Project conduct, decision-making, and release expectations are documented in
[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md), [GOVERNANCE.md](GOVERNANCE.md), and
[CHANGELOG.md](CHANGELOG.md). Future learned models and datasets must use the
[model/algorithm card](MODEL_CARD_TEMPLATE.md) and
[dataset card](DATASET_CARD_TEMPLATE.md) templates before review.

## Status

This is an early public research release. The next owners are clinical research,
privacy/security, device-calibration, and human-factors reviewers. Public source
availability does not imply clinical validation, regulatory clearance, or safe
use with protected health information.
