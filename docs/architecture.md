# System architecture

Clinical LiDAR Framework is a local-first research toolkit with deterministic
geometry and validation at its center. Measurement contracts remain separate
from optional device, computer-vision, and browser layers.

## Component flow

Depth frame or paired-photo manifest -> calibration and quality gates ->
surface/planimetry metrics -> longitudinal comparison or paired review ->
numeric local storage/service -> synthetic report or operator review.

## Components

- calibration.py and calibration_opencv.py: dependency-free and optional calibration paths.
- depth_provider.py: device-neutral true-depth frame contract.
- surface_metrics.py and paired_comparison.py: geometry and photo comparison.
- validation.py: segmentation, repeatability, and validity metrics.
- progress_tracker.py: longitudinal change with insufficient-quality handling.
- local_storage.py and local_service.py: numeric-only local persistence/service.
- ml/: optional provenance-first registration and segmentation adapters.
- webapp/: dependency-free browser interface; pixels remain in browser memory.
- examples/ and tests/: synthetic manifests and deterministic regression coverage.

## Boundaries and non-goals

The default path is synthetic/local. No patient images, model weights, SDK
binaries, or external provider calls are required. The system does not
diagnose, score healing, infer infection, predict prognosis, or recommend
treatment. Real clinical use requires intended-use, privacy, calibration,
reference-method, validation, and institutional review gates.

