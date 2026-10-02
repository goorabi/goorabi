# Research Portfolio Architecture

This document defines the planned architecture of the public GitHub research portfolio associated with this academic profile. It is a planning document: repository creation should occur only when the underlying scientific material is sufficiently mature, rights-cleared, and documented.

## Portfolio objective

The portfolio should demonstrate a coherent academic identity in **geomorphology, morphotectonics, active tectonics, remote sensing, GIS, InSAR, land subsidence, geohazards, and reproducible geoscience**. Repositories should represent genuine scientific work rather than profile-filling activity.

## Selection criteria

A candidate repository should satisfy most of the following:

1. Clear scientific purpose and relationship to the research profile.
2. Reusable or independently interpretable analytical value.
3. Sufficient methodological documentation for reproducibility or conditional reproducibility.
4. Verified provenance and redistribution rights.
5. No confidential, embargoed, student-sensitive, or restricted content.
6. A defensible distinction between source data, derived products, code, and publication outputs.
7. A maintenance burden proportional to its scientific value.

## Planned repository families

### Priority 1 — InSAR land-subsidence reproducibility

**Working repository name:** `insar-land-subsidence-marvdasht`

**Scientific role:** flagship portfolio repository demonstrating reproducible land-subsidence analysis for the Marvdasht Plain using Sentinel-1 time-series products and documented geospatial workflows.

**Candidate public content:**
- documented analytical code and parameter/configuration files;
- selected derived tables and small reproducible outputs where rights permit;
- time-series analysis and visualization workflows;
- spatial post-processing methods;
- data provenance/access instructions rather than restricted or very large raw SAR data;
- methodological documentation sufficient to distinguish PS-InSAR/SARPROZ and LiCSBAS-derived analytical stages where both are represented.

**Release constraint:** thesis/article-sensitive material, student work, restricted data, unpublished interpretation, and third-party data without redistribution rights must remain private until legitimately releasable.

**Initial visibility:** `Private` during preparation; `Public` only after scientific/publication and rights review.

**Portfolio priority:** Highest.

---

### Priority 2 — GIS subsidence hazard, exposure, and sensitivity analysis

**Working repository name:** `subsidence-risk-gis-workflow`

**Scientific role:** reusable GIS workflow for spatial assessment of subsidence hazard, exposure, substrate sensitivity, and co-location with elements at risk.

**Candidate public content:**
- normalization/standardization procedures;
- weighting and aggregation logic;
- spatial overlay and co-location routines;
- classification and sensitivity-analysis code;
- synthetic or legally redistributable test data where real layers cannot be released;
- reproducible generation of selected figures/tables.

**Initial visibility:** `Private` until methodology and input rights are fully audited.

**Portfolio priority:** High.

---

### Priority 3 — Sentinel-1 deformation time-series analysis utilities

**Working repository name:** `sentinel1-deformation-timeseries`

**Scientific role:** reusable Python-oriented utilities for reading, quality-controlling, summarizing, comparing, and visualizing deformation time series derived from established InSAR processing systems.

**Candidate public content:**
- generic time-series ingestion/cleaning functions;
- trend/statistical summaries;
- orbit-aware plotting and comparison;
- uncertainty/QC utilities;
- small synthetic/example datasets;
- automated tests for reusable functions.

**Initial visibility:** may become `Public` earlier than study-specific repositories if fully generic and free of restricted material.

**Portfolio priority:** High.

---

### Priority 4 — DEM and geomorphometric analysis

**Working repository name:** `geomorphometry-dem-workflows`

**Scientific role:** reusable terrain-analysis workflows supporting quantitative geomorphology and landscape analysis.

**Candidate public content:**
- DEM preprocessing conventions;
- terrain derivatives and morphometric indices;
- drainage/topographic analysis where scientifically validated;
- CRS/resampling/NoData documentation;
- small openly licensed test data or download instructions.

**Initial visibility:** `Public` once scientifically validated and documented.

**Portfolio priority:** Medium-high.

---

### Priority 5 — Morphotectonic and active-tectonic spatial analysis

**Working repository name:** `morphotectonic-spatial-analysis`

**Scientific role:** documented GIS/computational methods for morphotectonic indices, active-tectonic interpretation, and landscape-response analysis.

**Candidate public content:** reusable calculations, spatial methods, uncertainty/interpretation guidance, and reproducible examples based on releasable data.

**Initial visibility:** project-dependent; `Private` while tied to unpublished/student research, otherwise `Public` after review.

**Portfolio priority:** Medium-high.

---

### Priority 6 — Reproducible geoscience utilities

**Working repository name:** `geoscience-python-tools`

**Scientific role:** only for genuinely reusable utilities that emerge from multiple research projects and do not belong more naturally in a domain-specific repository.

**Release rule:** do not create this repository merely as a miscellaneous script collection. Create it only after a coherent reusable package/toolset exists.

**Initial visibility:** `Public` when mature.

**Portfolio priority:** Conditional.

## What should not become a public repository

- complete thesis working directories;
- raw student submissions or unpublished student research;
- manuscripts under review when release conflicts with journal/co-author policy;
- raw Sentinel-1 archives merely duplicated from authoritative providers;
- licensed/proprietary GIS layers without redistribution permission;
- local-machine backups, software installers, or processing caches;
- miscellaneous scripts without documentation or a coherent scientific purpose;
- credentials, tokens, private endpoints, personal data, or confidential records;
- artificial repositories created only to increase contribution counts.

## Recommended creation order

```text
1. insar-land-subsidence-marvdasht        [prepare privately]
2. sentinel1-deformation-timeseries       [extract generic reusable methods]
3. subsidence-risk-gis-workflow           [prepare privately]
4. geomorphometry-dem-workflows           [general reusable methods]
5. morphotectonic-spatial-analysis        [when a mature releasable workflow exists]
6. geoscience-python-tools                [only if a coherent toolset emerges]
```

The creation order is not the same as the public-release order. A generic reusable repository may be ready for public release before a study-specific repository that remains constrained by publication, student, or data-rights considerations.

## Future pinned-repository strategy

Once mature repositories exist, the GitHub profile should pin only a small set representing complementary strengths rather than six near-duplicates. A target portfolio could include:

1. flagship InSAR/land-subsidence study;
2. reusable Sentinel-1 time-series methods;
3. GIS hazard/risk workflow;
4. DEM/geomorphometry workflow;
5. morphotectonic/active-tectonic analysis.

Selection should be based on scientific quality, documentation, reproducibility, and relevance—not contribution volume.

## Repository readiness gate

Before creating or publishing a planned repository, answer:

- Is the scientific scope stable?
- Are authorship and student/co-author roles resolved?
- Are publication/embargo constraints resolved?
- Are source-data rights and redistribution terms known?
- Is there code or methodology worth preserving independently?
- Can the repository meet the documentation and reproducibility standards defined in this profile?

If the answer to a critical item is **No**, preparation may continue privately, but public release should wait.

## Next implementation milestone

The first implementation milestone is to inventory the candidate material for **`insar-land-subsidence-marvdasht`** and classify every prospective component as:

**Public now / Public after publication or review / Metadata-only / Private / Exclude**.

Only after that inventory should the first research repository be created.
