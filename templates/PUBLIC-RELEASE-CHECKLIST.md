# Public Research Release Checklist

A research repository should pass this gate before it is made public or assigned a stable citable release.

## Scientific validity

- [ ] Scientific purpose and scope are explicit.
- [ ] Methods and consequential parameters are documented.
- [ ] Released outputs have been checked against the authoritative analysis.
- [ ] Validation, uncertainty, and limitations are stated accurately.
- [ ] No preliminary result is presented as final without clear status labeling.

## Provenance and data governance

- [ ] Every important input has a documented source/provider.
- [ ] Dataset versions/acquisition periods are recorded where relevant.
- [ ] Raw, intermediate, derived, and publication outputs are distinguishable.
- [ ] Redistribution rights have been checked.
- [ ] Confidential, embargoed, personally identifiable, student-sensitive, or restricted material is absent.

## Reproducibility

- [ ] Environment/dependencies reflect the actual released workflow.
- [ ] Scientifically consequential versions are pinned or otherwise controlled.
- [ ] Configuration and execution order are documented.
- [ ] No undocumented absolute local paths are required.
- [ ] A clean-environment reproduction/verification has been attempted where feasible.
- [ ] Non-reproducible or restricted stages are explicitly identified.

## Geospatial / EO / InSAR quality

- [ ] CRS/datum, units, extent, and resolution are explicit.
- [ ] Temporal coverage is explicit.
- [ ] NoData, masking, resampling/interpolation, and classification conventions are documented where relevant.
- [ ] EO/InSAR acquisition and processing conventions required for interpretation are documented.
- [ ] LOS/sign/reference conventions are unambiguous where relevant.

## Documentation

- [ ] README is complete and matches the released repository state.
- [ ] Data access/provenance documentation is complete.
- [ ] Outputs are linked to their generating workflow where feasible.
- [ ] Known limitations and interpretation boundaries are visible.
- [ ] Contact/academic identity information is accurate.

## Citation and licensing

- [ ] `CITATION.cff` metadata are verified.
- [ ] ORCID/authorship information is accurate.
- [ ] Associated publication metadata and DOI are verified, if applicable.
- [ ] Code/content/data licenses have been selected only after rights review.
- [ ] Third-party material is not accidentally relicensed.
- [ ] DOI/archive metadata match the GitHub release if an archival release is created.

## Security and privacy

- [ ] No passwords, tokens, API keys, private SSH keys, credentials, or private endpoints are present.
- [ ] Commit history has been checked for accidentally committed secrets when warranted.
- [ ] Local usernames, private paths, emails not intended for release, and sensitive metadata have been reviewed.
- [ ] Automated dependency/security alerts have been reviewed where applicable.

## Repository quality

- [ ] File/directory naming is consistent.
- [ ] Temporary/cache/generated junk files are absent.
- [ ] Large files have a deliberate storage/publication strategy.
- [ ] Issues/TODOs do not conceal unresolved scientific validity problems.
- [ ] Release tag/version and changelog are consistent.
- [ ] Final repository state has undergone a scientific review and a technical/reproducibility review.

## Release decision

- **Decision:** `<Release | Hold>`
- **Reviewer:** `<name>`
- **Date:** `<YYYY-MM-DD>`
- **Release/tag:** `<...>`
- **Outstanding limitations:** `<...>`

> **Rule:** uncertainty about provenance, rights, confidentiality, scientific validity, or reproducibility results in **Hold**, not publication.
