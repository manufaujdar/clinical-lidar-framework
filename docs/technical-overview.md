# Technical overview

Status: early public research release.

## Runtime and dependencies

- Python 3.10 or newer with Setuptools packaging.
- clinical-lidar and clinical-lidar-research entrypoints.
- Optional integrations are listed in requirements-optional.txt.
- Browser UI is plain HTML/CSS/JavaScript and can run from Python's static server.

## Code map

- Calibration/measurement: calibration.py, calibration_opencv.py, surface_metrics.py.
- Input/device contracts: depth_provider.py and synthetic manifests.
- Comparison/validation: paired_comparison.py, progress_tracker.py, validation.py.
- Persistence/service: local_storage.py and local_service.py.
- Research CLI: research_cli.py; module entrypoint: __main__.py.
- Optional ML adapters: clinical_lidar/ml/contracts.py, registration.py, segmentation.py.
- Browser application: webapp/.
- Tests cover analysis adapters, storage, paired comparison, progress tracking, and core logic.

## Local operations and validation

Run unittest discovery, the synthetic progress/calibration/validation examples,
and the local web server commands in README.md. Treat examples as protocol
fixtures, not clinical evidence. Keep model and dataset cards synchronized
with future weights or datasets.

## Human gates

Every future device path should preserve calibration metadata, device identity,
frame quality, reference geometry, repeatability, and provenance. Real data,
external SDKs, model weights, deployment, intended use, IRB/institutional
review, BAA/DPA, regulation, and clinical claims remain human-owned decisions.

