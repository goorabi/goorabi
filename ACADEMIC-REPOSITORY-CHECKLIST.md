# Academic Repository Quality Checklist

Use this checklist before making a research repository public or assigning it a stable release.

## Scientific integrity

- [ ] The repository has a clearly defined scientific purpose.
- [ ] Claims are supported by the released methods, code, data references, or derived outputs.
- [ ] Experimental/analytical parameters are documented rather than implied.
- [ ] Units, coordinate reference systems, conventions, and temporal coverage are explicit.
- [ ] Known uncertainty, limitations, and validation procedures are stated.

## Data governance

- [ ] Data provenance and original source are documented.
- [ ] Redistribution rights have been checked.
- [ ] Restricted, confidential, student-sensitive, or personally identifiable material is absent.
- [ ] Large or non-redistributable datasets are referenced through access instructions rather than copied into the repository.
- [ ] Derived products are clearly distinguished from source data.

## Reproducibility

- [ ] Software versions and dependencies are specified.
- [ ] Required configuration and parameters are version-controlled.
- [ ] The execution order or workflow is documented.
- [ ] Paths and scripts do not depend on an undocumented local machine configuration.
- [ ] Random processes use documented seeds where scientifically relevant.
- [ ] Outputs can be traced to the scripts/workflows that generated them.

## Geospatial and Earth-observation quality

- [ ] CRS/datum information is explicit.
- [ ] Spatial resolution and extent are documented.
- [ ] Temporal coverage and acquisition conventions are explicit.
- [ ] No-data, masking, resampling, interpolation, and classification rules are documented where relevant.
- [ ] Remote-sensing/InSAR processing parameters required for interpretation are reported.
- [ ] Validation and quality-control metrics are included where available.

## Documentation and citation

- [ ] README provides scope, method, setup, execution, outputs, limitations, and citation information.
- [ ] External datasets and software are properly cited.
- [ ] Authorship and contributor roles are accurate.
- [ ] A suitable LICENSE is included only after confirming rights to distribute the repository contents.
- [ ] CITATION.cff is included for stable research repositories.
- [ ] Persistent identifiers (for example, DOI/Zenodo) are added when a stable release warrants archival citation.

## Release quality

- [ ] Temporary files, credentials, tokens, machine-specific paths, and private metadata are absent.
- [ ] Filenames and directory names are consistent and interpretable.
- [ ] Figures and tables have meaningful names and are linked to their generating workflow where feasible.
- [ ] Commit history reflects substantive work rather than artificial activity.
- [ ] The repository has undergone a final scientific and reproducibility review.

---

**Release rule:** if provenance, licensing, confidentiality, or scientific validity is uncertain, keep the material private or unpublished until the issue is resolved.
