# References and provenance

Reviewed 2026-08-10. These sources informed the architecture and validation
questions; no source code, patient data, model weights, or proprietary material
was copied into this tool.

## Open-source implementation references

| Source | What was useful | Boundary |
|---|---|---|
| [uwm-bigdata/wound-segmentation](https://github.com/uwm-bigdata/wound-segmentation) | Clear separation of training and prediction, dataset provenance, and explicit credits. | 2D image segmentation; not reused as code or model. |
| [theomthakur/woundscope](https://github.com/theomthakur/woundscope) | Staged ingestion/extraction/routing, provenance, confidence, and review-oriented outputs. | Billing/EHR hackathon project; not a LiDAR algorithm and not reused as code. |
| [opengeos/lidar](https://github.com/opengeos/lidar) | Geometric treatment of surface depressions and depth/volume-style metrics. | Terrain analysis; not medical and not reused as code. |

## Clinical and technical evidence to guide future validation

- [Smartphone-Based LiDAR Application for Easy and Accurate Wound Size Measurement](https://pubmed.ncbi.nlm.nih.gov/37762982/) — clinical comparison of a LiDAR wound-size workflow against ruler and image analysis.
- [Automatic segmentation and measurement of pressure injuries using deep learning models and a LiDAR camera](https://pmc.ncbi.nlm.nih.gov/articles/PMC9839689/) — reports a LiDAR plus segmentation workflow and highlights the need for external validation.
- [Evaluation of a Novel Three-Dimensional Wound Measurement Device for Assessment of Diabetic Foot Ulcers](https://pmc.ncbi.nlm.nih.gov/articles/PMC7580588/) — emphasizes reliability, practicality, and comparison against established measurements.
- [Quantitative Monitoring Wound Healing Status Through Three-dimensional Imaging on Mobile Platforms](https://pmc.ncbi.nlm.nih.gov/articles/PMC6161627/) — relevant background for serial 3D measurement and repeatability.
- [NSW Agency for Clinical Innovation wound assessment toolkit](https://aci.health.nsw.gov.au/networks/spinal-cord-injury/pi-toolkit/assessment/wound-assessment/validated-tool) — distinguishes validated assessment tools such as PUSH and BWAT from ad-hoc scores.
- [Digital planimetry results in more accurate wound measurements](https://pmc.ncbi.nlm.nih.gov/articles/PMC2909508/) — supports calibrated planimetry over length × width estimation.
- [Non-contact digital planimetry using a photo scale reference](https://pubmed.ncbi.nlm.nih.gov/36001845/) — reports reproducibility of a marker-based photo workflow.
- [Automatic colorimetric calibration of human wounds](https://pmc.ncbi.nlm.nih.gov/articles/PMC2850874/) — supports color-chart/white-balance controls before interpreting color changes.
- [Standardized photography protocol for injury documentation](https://pubmed.ncbi.nlm.nih.gov/26932497/) — supports consistent distance, scale, orientation, and capture protocol.
- [PUSH derivation and validation](https://pubmed.ncbi.nlm.nih.gov/11723157/) — supports the limited pressure-ulcer structure of length × width, exudate amount, and tissue type.
- [Bates-Jensen wound assessment reliability](https://pmc.ncbi.nlm.nih.gov/articles/PMC6693585/) — supports recording wound size, visible depth, edges, undermining/tunneling, tissue, exudate, and periwound characteristics as structured observations.
- [Percentage area reduction and diabetic foot-ulcer outcomes](https://pubmed.ncbi.nlm.nih.gov/16799391/) — supports cautious longitudinal use of area change in a defined diabetic-foot-ulcer study population, not a general recovery threshold.
- [Standardized wound photography algorithm](https://pubmed.ncbi.nlm.nih.gov/35993857/) — supports recording standardized capture conditions and repeatable photography practices.
- [Computerized planimetry accuracy and reliability](https://pubmed.ncbi.nlm.nih.gov/19521289/) — supports separating image-derived planimetry from subjective clinical observations and documenting image-margin quality.
- [The influence of wound geometry on healing-rate measurement](https://doi.org/10.1016/S0741-5214(96)80021-8) — motivates reporting linear edge change alongside percentage area reduction.
- [Structural similarity image quality assessment](https://pubmed.ncbi.nlm.nih.gov/15376593/) — source for the SSIM-style image comparison signal.

These papers are evidence for what must be tested, not evidence that this
prototype is clinically accurate. No clinical performance claim is made here.

Optional integration candidates and their license/provenance boundaries are
listed in [OPEN_SOURCE_EXTENSIONS.md](OPEN_SOURCE_EXTENSIONS.md).

## License references

- [Apache License 2.0, Apache Software Foundation](https://www.apache.org/licenses/LICENSE-2.0.txt)
- [OSI approved licenses](https://opensource.org/licenses)
- [Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/) — possible future choice for separately authored explanatory materials or datasets, not automatically applied to this code.

## Security and privacy guidance

- [HHS Security Rule](https://www.hhs.gov/hipaa/for-professionals/security/index.html) — administrative, physical, and technical safeguard context; this project is not HIPAA-certified.
- [HHS Minimum Necessary Requirement](https://www.hhs.gov/hipaa/for-professionals/privacy/guidance/minimum-necessary-requirement/index.html) — data-minimization context for any future PHI workflow.
- [OWASP Application Security Verification Standard](https://owasp.org/www-project-application-security-verification-standard/) — application-security verification topics for a future reviewed deployment.
