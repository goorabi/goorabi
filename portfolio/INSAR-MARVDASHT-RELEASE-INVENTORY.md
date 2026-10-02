# Marvdasht InSAR — Release & Privacy Inventory

**Planned repository:** `insar-land-subsidence-marvdasht`  
**Status:** Pre-repository release planning  
**Default rule:** when rights, authorship, publication status, confidentiality, or provenance are uncertain, classify conservatively and do not publish.

## Classification scheme

| Class | Meaning |
| --- | --- |
| **Public now** | May be released after routine QC because it is original/releasable, non-sensitive, and sufficiently documented. |
| **Public after review/publication** | Scientifically suitable for release, but only after manuscript/thesis, authorship, embargo, or co-author/student review is resolved. |
| **Metadata-only** | Describe provenance, identifiers, acquisition/access instructions, and processing role; do not redistribute the underlying data. |
| **Private** | Keep outside the public repository because of confidentiality, unpublished/student-sensitive content, licensing, or unresolved rights. |
| **Exclude** | Do not place in the research repository because it is unnecessary, unsafe, redundant, generated junk, or inappropriate for version control. |

## Authoritative project facts to preserve

The repository documentation must not silently merge distinct InSAR processing tracks.

### PS-InSAR / SARPROZ

- Sentinel-1, ascending and descending geometries.
- Ascending acquisition period begins **13 November 2016** and extends to **2020**.
- Descending acquisition period begins **21 March 2017** and extends to **2020**.
- Reported image counts: **99 ascending** and **81 descending**.
- Primary role: precise subsidence-rate/pattern characterization and deformation time-series analysis.

### LiCSBAS

- Sentinel-1, ascending and descending geometries.
- Reported image counts: **240 ascending** and **206 descending**.
- Ascending processing record extends to **12 March 2024**.
- Descending processing record extends to **31 May 2024**.
- Primary role: longer deformation time series and spatial hazard/exposure analysis.

**Integrity rule:** there is no basis in the authoritative project record for presenting PS-InSAR as beginning in 2014 or LiCSBAS processing as extending into 2025. Any future repository metadata must preserve the verified periods rather than older preliminary descriptions.

## Candidate-material inventory

| Material | Default classification | Release rationale / condition |
| --- | --- | --- |
| Repository README and methodological overview | **Public after review/publication** | Public release is appropriate once wording does not prematurely disclose thesis/manuscript-sensitive interpretation. |
| Verified acquisition dates and image counts | **Public after review/publication** | Suitable metadata, but synchronize with the authoritative thesis/article record before public release. |
| Sentinel-1 raw SLC/GRD archives | **Metadata-only** | Do not duplicate large authoritative mission archives; document product/access provenance instead. |
| Sentinel-1 product identifiers / acquisition lists | **Public after review/publication** | Highly useful for reproducibility if verified and not restricted by the publication workflow. |
| SARPROZ software binaries/installers/license material | **Exclude** | Third-party software and licensing material do not belong in the repository. |
| SARPROZ parameter documentation created by the research team | **Public after review/publication** | Release only after parameters are verified against the actual final processing. |
| SARPROZ project/cache/intermediate working directories | **Exclude** | Machine/project-state files are generally unsuitable for Git and may contain large/redundant material. |
| PS-InSAR analytical scripts authored for post-processing | **Public after review/publication** | Release after code audit, path cleanup, provenance check, and manuscript/thesis review. |
| PS velocity/time-series derived tables | **Public after review/publication** | Candidate derived products if authorship, publication status, and source-data terms permit. |
| PS point datasets / geospatial outputs | **Public after review/publication** | Release selectively; document CRS, LOS convention, reference strategy, units, QC, and derivation. |
| LiCSBAS software/source copied from upstream | **Exclude** | Do not vendor/copy upstream software unnecessarily; cite/link the authoritative project/version instead. |
| LiCSBAS configuration/parameter records used in the study | **Public after review/publication** | Valuable for reproducibility after verification against final execution records. |
| LiCSBAS raw/downloaded processing inputs | **Metadata-only** | Prefer provenance/access instructions; assess each upstream product's redistribution terms. |
| LiCSBAS velocity/time-series derived outputs | **Public after review/publication** | Candidate release products after publication/rights and scientific QC. |
| Small representative/synthetic test dataset | **Public now** | Prefer synthetic or clearly releasable samples for demonstrating code without exposing restricted study material. |
| Generic Python code for time-series cleaning/plotting/statistics | **Public now** | May be released independently once generalized, documented, tested, and stripped of study-sensitive values. |
| Study-specific Python analysis scripts | **Public after review/publication** | Keep private until scientific outputs and embedded parameters/paths have been audited. |
| Final publication-quality maps generated by the project | **Public after review/publication** | Release only if figure rights, basemap/data licenses, publication policy, and authorship permit. |
| Draft maps, exploratory plots, rejected figures | **Private** | Preserve locally/project-private if scientifically useful; do not clutter the public scholarly record. |
| GIS study boundary created/owned by the project | **Public after review/publication** | Release if provenance and redistribution rights are clear; include CRS and boundary definition. |
| Third-party administrative/geological/soil/land-use layers | **Metadata-only** by default | Do not redistribute until the license/source terms for each layer are individually verified. |
| Groundwater, well, infrastructure, population, or institutional datasets | **Private / Metadata-only** | Classification depends on provider rights, sensitivity, aggregation, and publication permissions. |
| Exposure/sensitivity input layers used in risk modelling | **Private / Metadata-only** initially | Audit all 19 exposure layers and sensitivity inputs individually before any release. |
| Co-location element-at-risk layers | **Private / Metadata-only** initially | Audit all 11 categories per orbit for provenance, sensitivity, and redistribution rights. |
| Derived aggregate statistics that cannot reconstruct restricted inputs | **Public after review/publication** | Candidate for release after disclosure-risk and scientific review. |
| Thesis Word/PDF working files | **Private** | A research-code repository is not a thesis-document backup. Deposit the final thesis only through an appropriate institutional/archive channel if desired and permitted. |
| Student drafts, comments, supervision correspondence | **Private** | Confidential/student-sensitive material must not enter the public repository. |
| Manuscript drafts, reviewer correspondence, submission files | **Private** | Keep outside public Git unless a deliberate later open-review/publication decision permits release. |
| Published article citation/DOI metadata | **Public now** once bibliographically verified | Metadata can be linked without reproducing publisher-controlled article files. |
| Publisher PDF | **Exclude** unless explicit rights allow | Prefer DOI/publisher/authorized repository link; do not assume redistribution rights. |
| Author-accepted manuscript | **Private until rights/embargo checked** | Release only under the journal's permitted self-archiving conditions. |
| `environment.yml` / dependency specification | **Public after verification** | Should reflect the environment actually used or a tested reproducible reconstruction, not guessed versions. |
| `CITATION.cff` | **Public at repository release** | Populate only with verified authorship, title, release version/date, license, and related DOI metadata. |
| Reproducibility manifest | **Public at repository release** | State honestly whether reproduction is Full, Conditional, or Partial. |
| Credentials, API tokens, SSH/private keys, account cookies | **Exclude** | Never commit. If ever exposed, revoke/rotate rather than merely deleting from the latest revision. |
| Absolute local paths, usernames, temporary caches, logs | **Exclude** | Replace paths with configuration/relative paths and remove machine-specific artifacts. |

## GIS layer audit required before release

Because the study includes composite hazard–exposure–sensitivity assessment and co-location analysis, each input layer must receive an individual rights/provenance record before publication. At minimum record:

```text
Layer name
Scientific role
Provider / owner
Original URL or institutional source
Date/version
Spatial resolution / scale
CRS
License / terms of use
Redistribution allowed? Yes / No / Unclear
Contains sensitive information? Yes / No / Unclear
Derived/transformed? How?
Planned public status
Required citation / acknowledgement
```

No blanket assumption should be made that all 19 exposure layers or all 11 element-at-risk categories can be redistributed merely because they were used analytically.

## Code audit before public release

Every script proposed for release must be checked for:

- hard-coded Windows/local paths;
- usernames and machine identifiers;
- credentials or tokens;
- unpublished study-specific constants that should instead be configuration;
- undocumented CRS/units/sign conventions;
- dependencies not declared in the environment;
- copied third-party code without attribution/license compatibility;
- outputs that depend on unavailable private files;
- non-deterministic steps and undocumented manual edits;
- dead/debug code and temporary export logic.

## Recommended first public package

The safest first release does **not** need to contain the complete Marvdasht dataset. A high-quality initial public package can consist of:

```text
README.md
CITATION.cff
LICENSE                  # after rights review
environment.yml
config/example.yml
data/README.md            # provenance and access, not restricted raw data
src/ or scripts/          # audited original code
examples/                 # synthetic or openly releasable small data
outputs/example/          # reproducible demonstration outputs
docs/methodology.md
REPRODUCIBILITY.md
```

This structure can demonstrate scientific reproducibility without redistributing restricted or publication-sensitive research assets.

## Pre-creation decision gate

Before creating `insar-land-subsidence-marvdasht`, resolve these items:

- [ ] Confirm repository authorship/contributor roles, including student/co-author contributions.
- [ ] Confirm current publication/thesis disclosure constraints.
- [ ] Audit rights for each candidate GIS/data layer.
- [ ] Identify which code is original and releaseable.
- [ ] Remove credentials, private paths, and machine-specific configuration.
- [ ] Verify final PS-InSAR and LiCSBAS parameters against authoritative processing records.
- [ ] Decide whether study-specific derived datasets will be released, archived elsewhere, or described metadata-only.
- [ ] Select licenses separately for code and non-code material after rights review.
- [ ] Define the initial reproducibility level: Full, Conditional, or Partial.
- [ ] Perform final scientific and privacy review before changing repository visibility to Public.

## Current recommendation

**Do not create the public repository yet.** First collect and audit the actual candidate code/data/documentation against this inventory. Repository creation should follow the evidence, not precede it.
