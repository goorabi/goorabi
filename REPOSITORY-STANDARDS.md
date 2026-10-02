# Academic Repository Standards

This document defines the default technical and scholarly standards for future public research repositories associated with this profile. Individual projects may deviate when the scientific workflow requires it, but deviations should be documented.

## 1. Repository naming

Use short, descriptive, lowercase names separated by hyphens.

Preferred pattern:

```text
<method-or-theme>-<scientific-subject>[-<study-area>]
```

Examples:

```text
insar-land-subsidence
geomorphometric-analysis
morphotectonic-gis-analysis
sentinel1-deformation-timeseries
```

Avoid vague names (`project1`, `analysis-final`), dates as the primary identifier, personal names, and unexplained abbreviations.

## 2. Repository scope

A repository should represent one coherent scientific product: a reproducible analysis, reusable method, documented dataset derivative, software utility, or publication-associated workflow. Do not combine unrelated projects merely to reduce repository count.

## 3. Core files

Stable public research repositories should normally include:

- `README.md` — scientific scope, methods, execution, outputs, limitations, and citation guidance;
- `CITATION.cff` — machine-readable citation metadata;
- `LICENSE` — selected only after confirming ownership and redistribution rights;
- `.gitignore` — tailored to the software stack and generated data;
- `environment.yml`, `requirements.txt`, or another appropriate environment specification;
- `CHANGELOG.md` when releases or substantive versioned changes warrant it.

Do not add files merely to satisfy a template when they have no scientific or technical function.

## 4. Recommended directory model

```text
repository/
├── README.md
├── CITATION.cff
├── LICENSE
├── .gitignore
├── environment.yml          # or another reproducible dependency specification
├── config/
├── data/
│   └── README.md
├── docs/
├── src/                     # reusable code
├── scripts/                 # ordered analytical scripts when appropriate
├── notebooks/               # exploratory/presentational notebooks only when useful
├── outputs/                 # selected reproducible outputs suitable for version control
└── tests/                   # for reusable or consequential computational code
```

Raw satellite scenes, large rasters, proprietary datasets, confidential records, and redistributable-restricted material should normally remain outside Git unless there is a justified data-publication strategy.

## 5. README scientific schema

Each research README should address, in an order appropriate to the project:

1. title and concise scientific purpose;
2. research context and scope;
3. study area and/or dataset coverage;
4. data sources and provenance;
5. software and environment;
6. methodology/workflow;
7. key parameters and assumptions;
8. execution/reproduction instructions;
9. outputs and expected products;
10. validation and quality control;
11. limitations and uncertainty;
12. data-access and licensing constraints;
13. citation;
14. authors/contributors and academic profile links.

For geospatial projects, explicitly state CRS/datum, units, spatial resolution, temporal coverage, NoData/masking conventions, and relevant resampling/interpolation rules.

For InSAR projects, document sensor/mode/orbit/track where relevant, acquisition period, processing software, reference strategy, masking/quality thresholds, time-series conventions, LOS/vertical assumptions, and validation information sufficient to interpret the released result.

## 6. Code and workflow conventions

- Prefer deterministic, parameterized scripts over undocumented manual operations.
- Separate configuration from analytical logic where practical.
- Avoid hard-coded local absolute paths.
- Use relative paths or documented configuration variables.
- Record software/package versions that can materially affect results.
- Use fixed random seeds when stochastic behavior affects reproducibility.
- Keep exploratory notebooks distinct from authoritative production workflows.
- Ensure figures/tables can be traced to the workflow that generated them whenever feasible.

## 7. Data governance

Every repository containing or referencing research data must distinguish:

- **source/raw data** — original observations or externally acquired products;
- **intermediate data** — processing-stage products;
- **derived data** — analytical outputs created by the research workflow;
- **publication outputs** — final figures, tables, maps, or release products.

Document provenance, access date/version where relevant, provider, license/terms, and redistribution constraints. Never publish credentials, private metadata, personally identifiable information, confidential student/research material, or data whose redistribution rights are uncertain.

## 8. Licensing

Do not apply a license automatically to all repositories.

- Code licensing and data/content licensing may require different terms.
- Confirm ownership and third-party restrictions before selecting a license.
- A repository without a license is not automatically open for reuse.
- Publication-associated repositories should state clearly which files are covered by which license when mixed content exists.

License selection should be made project-by-project before public release.

## 9. Citation and scholarly identity

Stable research repositories should include `CITATION.cff` using the verified scholarly identity of the author(s). Include ORCID identifiers where appropriate. When a repository corresponds to a publication, cite the publication and clearly state the relationship between repository release and article/version.

For archival releases, consider DOI registration through a suitable research archive such as Zenodo when scientifically appropriate. Git tags/releases and archived DOI versions should correspond unambiguously.

## 10. Versioning and releases

Use meaningful Git history and avoid artificial commits intended only to increase contribution counts.

For stable scientific products:

- use tagged releases when a citable state is reached;
- use semantic versioning when the repository behaves as software;
- for analysis repositories, use documented release versions that correspond to scientific milestones;
- preserve reproducibility of previously cited releases when practical.

## 11. GitHub collaboration model

For substantive research repositories:

- use `main` as the stable default branch;
- use short-lived branches for significant changes when collaboration or review warrants it;
- use pull requests for changes that benefit from review;
- use Issues for traceable tasks, methodological questions, bugs, and reproducibility problems rather than informal undocumented notes;
- protect stable/citable branches when the collaboration model justifies it.

## 12. Security

- Never commit passwords, API keys, tokens, private SSH keys, or service credentials.
- Keep GitHub secret scanning/push protection enabled where available.
- Use repository/environment secrets for CI credentials when needed.
- Pin or otherwise control critical computational dependencies when reproducibility/security requires it.
- Review automated dependency updates before merging them into scientific workflows.

## 13. Automation and CI

GitHub Actions should be added only when they improve scientific or software quality. Appropriate uses include:

- syntax/lint checks;
- automated tests;
- environment/build verification;
- reproducibility smoke tests using small public test data;
- documentation builds;
- validation of `CITATION.cff` or other metadata.

Do not run expensive Earth-observation processing in CI unless cost, data access, licensing, and runtime are explicitly appropriate.

## 14. Public-release gate

Before a repository becomes public, verify all of the following:

**Scientific validity → provenance → licensing → confidentiality → reproducibility → documentation → citation → security → final review.**

If any of these is unresolved, the repository should remain private or unpublished until resolved.
