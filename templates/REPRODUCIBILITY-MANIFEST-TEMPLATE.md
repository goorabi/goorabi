# Reproducibility Manifest

## Research product

- **Repository:** `<owner/repository>`
- **Release / commit:** `<tag or commit SHA>`
- **Scientific product:** `<analysis / software / dataset derivative / publication workflow>`
- **Associated publication:** `<citation or N/A>`
- **Manifest date:** `<YYYY-MM-DD>`

## Reproducibility level

Select and justify one:

- **Full** — released inputs (or openly obtainable identical inputs), environment, parameters, code, and instructions can regenerate the released analytical outputs.
- **Conditional** — workflow is reproducible after obtaining externally licensed/restricted inputs according to documented access instructions.
- **Partial** — only selected stages or outputs are reproducible; limitations are explicitly documented below.

**Declared level:** `<Full | Conditional | Partial>`

**Justification:** `<explain>`

## Computational environment

- Operating system: `<...>`
- Python / R / other runtime: `<...>`
- GIS / EO / InSAR software and versions: `<...>`
- Environment specification: `<environment.yml / requirements.txt / other>`
- Hardware-sensitive requirements: `<RAM/GPU/storage or N/A>`

## Input inventory

| Input | Version / date | Provenance | Access | Checksum / identifier | Included? |
| --- | --- | --- | --- | --- | --- |
| `<input>` | `<...>` | `<provider>` | `<URL/terms>` | `<SHA256/DOI/product ID>` | `<Yes/No>` |

## Configuration and parameters

Identify the authoritative configuration files and all scientifically consequential parameters not encoded directly in them.

| Parameter / configuration | Value / file | Scientific relevance |
| --- | --- | --- |
| `<...>` | `<...>` | `<...>` |

## Execution order

```text
1. <environment setup>
2. <data acquisition/preparation>
3. <preprocessing>
4. <primary analysis>
5. <quality control / validation>
6. <figure/table/map generation>
```

## Expected outputs

| Output | Generating workflow | Verification criterion |
| --- | --- | --- |
| `<file/product>` | `<script/step>` | `<checksum/range/visual/statistical criterion>` |

## Geospatial conventions

- CRS / datum: `<...>`
- Horizontal / vertical units: `<...>`
- Spatial resolution: `<...>`
- NoData / masking: `<...>`
- Resampling / interpolation: `<...>`

## Earth-observation / InSAR conventions (if applicable)

- Mission / sensor: `<...>`
- Orbit / track / geometry: `<...>`
- Acquisition period: `<...>`
- Reference point / reference area: `<...>`
- Quality thresholds: `<...>`
- LOS sign convention: `<...>`
- LOS-to-vertical assumption, if used: `<...>`
- Validation / uncertainty metric: `<...>`

## Known non-determinism

Document stochastic algorithms, multithreading/GPU variation, external services, mutable upstream datasets, manual interpretation, or software behavior that may prevent bit-for-bit reproduction.

## Restricted or unavailable components

List inputs or steps that cannot be distributed and state precisely how this affects reproducibility.

## Verification record

- [ ] Fresh environment created from the released specification
- [ ] Input provenance checked
- [ ] Configuration checked
- [ ] Workflow executed in documented order
- [ ] Expected outputs generated
- [ ] Validation/QC criteria satisfied
- [ ] Restrictions and deviations recorded

## Deviations

`<Record any difference between the documented release and the verification run.>`
