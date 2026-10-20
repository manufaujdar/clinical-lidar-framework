# Documentation index

Clinical LiDAR Framework is an Apache-2.0, vendor-neutral research framework
for calibrated depth and wound-surface measurement. It is not a clinical
device, diagnostic system, treatment tool, or validated healing score.

## Choose a task

| Task | Read first | Continue with |
| --- | --- | --- |
| Run a synthetic example | [Quick start](../README.md#quick-start) | [Technical overview](technical-overview.md) |
| Change a measurement component | [Architecture](architecture.md) | [Comparison method](../WOUND_COMPARISON_METHOD.md), [validation protocol](../VALIDATION_PROTOCOL.md) |
| Use the browser or local service | [Webapp guide](../webapp/README.md) | [Security boundary](../SECURITY.md), [UI decisions](../UI_UX_REVIEW.md) |
| Add a device or model adapter | [Extension policy](../OPEN_SOURCE_EXTENSIONS.md) | [ML contracts](../clinical_lidar/ml/README.md), [model card](../MODEL_CARD_TEMPLATE.md), [dataset card](../DATASET_CARD_TEMPLATE.md) |
| Contribute or publish | [Contribution guide](../CONTRIBUTING.md) | [Quality gates](../QUALITY.md), [governance](../GOVERNANCE.md), [changelog](../CHANGELOG.md) |
| Assess a research claim | [Validation protocol](../VALIDATION_PROTOCOL.md) | [References](../REFERENCES.md), [compliance](../COMPLIANCE.md) |

## File and folder ownership

| Location | Purpose |
| --- | --- |
| `clinical_lidar/` | Geometry, calibration, comparison, validation and numeric storage APIs |
| `clinical_lidar/ml/` | Optional registration and segmentation adapters with explicit provenance |
| `webapp/` | Browser interface and its operating instructions |
| `examples/`, `tests/` | Synthetic input manifests and deterministic regression evidence |
| `tools/`, `.quality/` | Supervised local review and repository quality tooling |
| `docs/` | This task index, architecture and technical overview |
| Root Markdown files | Shared methodology, safety, governance, contribution and provenance contracts |

Keep implementation-specific instructions beside their package or webapp. Link
shared methodology and governance from this index rather than duplicating their
requirements. New examples must remain synthetic and clearly labelled.

## Evidence and release limits

Geometry or image change is not a healing score. Device calibration,
reference-method validation, intended use and approved data handling remain
separate research gates. Optional OpenCV, Open3D and segmentation integrations
do not turn RGB images into native depth measurements or establish clinical
fitness. Source and third-party terms are in [LICENSE](../LICENSE),
[NOTICE](../NOTICE) and the [reference register](../REFERENCES.md).
