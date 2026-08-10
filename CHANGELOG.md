# Changelog

All notable changes to Clinical LiDAR Framework are recorded here.

The project follows a lightweight release convention: versioned source changes,
validation evidence, provenance notes, and known limitations are recorded
together. This is not a statement of clinical performance.

## [Unreleased]

- Added a deterministic, repo-local frontend review agent and CI audit command.
- Hardened local history persistence and report downloads in the browser app.
- Clarified that the current longest-axis metric is axis-aligned rather than a true rotated maximum.
- Improved workflow order, button hierarchy, empty-history states, and advanced-settings placement.
- Added a single photo-first `Analyze pair` action with automatic first-pass setup and collapsed settings.

## [0.1.0] - 2026-08-10

### Added

- Standalone `clinical_lidar` Python package.
- Calibrated depth-grid geometry and longitudinal comparison utilities.
- Paired-photo webapp with local setup suggestions and human review gates.
- Phantom calibration, validation metrics, and device-depth contracts.
- Local numeric-only storage boundary and loopback service.
- Synthetic fixtures, focused regression tests, CI, Apache-2.0 licensing,
  security/compliance guidance, citation metadata, and provenance notes.

### Limitations

- No validated wound-specific segmentation model.
- No clinical dataset, clinical accuracy claim, or regulatory clearance.
- Native ARCore/ARKit adapters and professional device exports remain external
  integration work.
