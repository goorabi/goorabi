# Research Repository Template Library

This directory is the controlled template set for future public research repositories associated with this academic profile. Templates are starting points, not files to copy blindly.

## Template map

| Template | Purpose | Use |
| --- | --- | --- |
| `RESEARCH-README-TEMPLATE.md` | Master scientific README | Start substantive research repositories here; remove non-applicable sections. |
| `DATA-README-TEMPLATE.md` | Data provenance, access, lineage, restrictions | Use when research data are consumed, derived, or released. |
| `CITATION.cff.template` | Scholarly citation metadata | Convert to `CITATION.cff` only after title, version, rights, and publication metadata are verified. |
| `ENVIRONMENT-TEMPLATE.yml` | Reproducible Conda environment | Convert to `environment.yml`; include only dependencies actually used. |
| `SCIENTIFIC-GITIGNORE-TEMPLATE.txt` | Python/GIS/EO ignore rules | Convert to `.gitignore` and tailor to project data and release strategy. |
| `REPRODUCIBILITY-MANIFEST-TEMPLATE.md` | Reproducibility declaration and verification | Recommended for publication-associated or computationally consequential research. |
| `CHANGELOG-TEMPLATE.md` | Scientific/technical release history | Use where changes affect methods, results, or reproducibility. |
| `PUBLIC-RELEASE-CHECKLIST.md` | Final Release/Hold gate | Apply before public release or a stable citable version. |

## Minimal research repository

```text
README.md
CITATION.cff
.gitignore
environment.yml   # when a computational environment is required
data/README.md     # when research data are used
```

Add a changelog, reproducibility manifest, tests, CI, notebooks, or additional directories only when the project benefits from them.

## Publication-associated repository

```text
README.md
CITATION.cff
LICENSE            # only after rights review
.gitignore
environment.yml or equivalent
CHANGELOG.md
data/README.md
REPRODUCIBILITY.md
config/
src/ and/or scripts/
outputs/            # selected release products only
```

## Quality-control rules

1. **Do not template facts.** Dates, image counts, orbit/track identifiers, thresholds, CRS, software versions, DOI metadata, and licenses must come from authoritative project records.
2. **Do not over-engineer.** Empty directories and unused infrastructure reduce clarity.
3. **Do not publish raw data by default.** Check size, provenance, redistribution rights, confidentiality, and whether metadata/access instructions are preferable.
4. **Do not assign a license mechanically.** Code, data, figures, text, and third-party inputs may have different rights.
5. **Do not equate reproducibility with openness.** A workflow can be conditionally reproducible when identical inputs must be obtained under external terms.
6. **Do not manufacture contribution activity.** Commit history should represent meaningful scientific, documentation, or technical changes.
7. **Freeze citable states.** Stable releases need unambiguous version/tag metadata and, where appropriate, an archival DOI.

## Geospatial / InSAR extension

GIS, remote-sensing, and InSAR repositories must explicitly resolve conventions required to interpret results: CRS/datum, units/resolution, temporal coverage, masks/NoData, resampling/interpolation, sensor/acquisition geometry, reference strategy, sign convention, processing software/version, quality thresholds, and validation/uncertainty as applicable.

## Release sequence

**Scientific validity → provenance → rights/confidentiality → environment → reproducibility → documentation → citation → security → release review → publish/archive**

`PUBLIC-RELEASE-CHECKLIST.md` is the final operational gate.
