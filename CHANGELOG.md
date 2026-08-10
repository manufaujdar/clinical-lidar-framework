# Changelog

All notable changes to Clinical LiDAR Framework are recorded here.

The project follows a lightweight release convention: versioned source changes,
validation evidence, provenance notes, and known limitations are recorded
together. This is not a statement of clinical performance.

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
