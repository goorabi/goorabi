# Changelog

All scientifically or technically meaningful changes to stable releases should be documented here.

The format is inspired by Keep a Changelog, but entries should emphasize changes that affect interpretation, reproducibility, data lineage, methodology, or released outputs.

## [Unreleased]

### Added
- <new analysis, dataset, workflow, documentation, validation, or output>

### Changed
- <methodological, parameter, dependency, data, or documentation change>

### Fixed
- <error correction and its scientific/technical consequence>

### Data / provenance
- <source dataset version, acquisition, access, or lineage change>

### Reproducibility
- <environment, configuration, execution, or verification change>

## [x.y.z] - YYYY-MM-DD

### Added
- <...>

### Changed
- <...>

### Fixed
- <...>

### Scientific impact
- <state whether results, figures, statistics, interpretation, or conclusions changed>

### Reproducibility impact
- <state whether prior instructions/environment remain valid>

---

## Versioning guidance

For software-like repositories, semantic versioning may be appropriate:

- **MAJOR** — incompatible methodological/API/workflow change or a change that invalidates reproduction under the previous interface;
- **MINOR** — backward-compatible new capability, analysis, or output;
- **PATCH** — backward-compatible correction that does not change the intended scientific interpretation.

For publication-associated analytical repositories, release tags may instead correspond to manuscript/revision/publication milestones. Whichever scheme is used, document it in the repository README and never imply that a corrected scientific result is merely cosmetic.
