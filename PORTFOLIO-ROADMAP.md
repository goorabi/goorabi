# Academic Research Portfolio Roadmap

This document defines the organizational framework for future public repositories associated with this academic profile. It is intentionally limited to public, publication-ready, ethically shareable research materials.

## Repository principles

Future research repositories should be:

1. **Scientifically scoped** — one coherent research problem, method, dataset family, or reproducible workflow per repository.
2. **Reproducible** — processing steps, software dependencies, parameters, coordinate reference systems, and analytical assumptions should be documented sufficiently for independent interpretation or reproduction where licensing permits.
3. **Traceable** — distinguish source data, intermediate products, derived outputs, figures, tables, and code.
4. **Citation-ready** — include bibliographic metadata, software/data citations, authorship information, and a recommended citation when a repository reaches a stable public release.
5. **Ethically shareable** — exclude confidential, restricted, student-sensitive, personally identifiable, or third-party material that cannot legally or ethically be redistributed.
6. **Versioned** — substantive analytical changes should be traceable through meaningful commits and, for stable research outputs, releases/tags where appropriate.

## Planned portfolio domains

### InSAR & land subsidence
Reproducible workflows and selected derived products for Sentinel-1 deformation analysis, including time-series interpretation and spatial characterization of land subsidence.

### Geomorphology & morphotectonics
Workflows supporting quantitative geomorphology, morphometric analysis, active-tectonic interpretation, and landscape-evolution research.

### GIS-based hazard and risk analysis
Spatial workflows for hazard, exposure, sensitivity, and risk assessment, with explicit documentation of normalization, weighting, overlay, classification, and uncertainty assumptions.

### DEM-based geomorphometry
Reusable terrain-analysis workflows, including DEM preprocessing, derivative generation, morphometric indices, and quality-control procedures.

### Reproducible geoscience computing
Python-based utilities and documented analytical workflows intended to improve transparency, repeatability, and scientific visualization in geoscience research.

## Recommended structure for future research repositories

```text
repository/
├── README.md
├── LICENSE
├── CITATION.cff
├── environment.yml or requirements.txt
├── docs/
├── src/ or scripts/
├── notebooks/              # only when notebooks are scientifically useful
├── config/                 # parameters and reproducible settings
├── data/
│   └── README.md            # provenance/access instructions; avoid restricted raw data
├── outputs/                 # selected reproducible derived outputs
└── tests/                   # where reusable code warrants automated testing
```

The exact structure should follow the scientific workflow rather than forcing unnecessary directories.

## Minimum README standard

Each public research repository should document:

- scientific objective and scope;
- study area or dataset scope, where applicable;
- data sources, provenance, licensing, and access constraints;
- software environment and dependencies;
- methodological workflow and key parameters;
- coordinate reference system and spatial units for geospatial work;
- instructions required to reproduce released outputs;
- interpretation limits and known uncertainties;
- authorship, citation, license, and contact/profile links.

## Publication policy

A repository should not be made public merely to increase profile activity. Public release is appropriate when the material has a clear scientific purpose, adequate documentation, verified provenance, and no confidentiality or licensing conflict.

---

This roadmap is an organizational document for the GitHub academic portfolio and does not itself represent a research dataset or publication.
