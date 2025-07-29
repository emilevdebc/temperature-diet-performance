# Cricket Development Dataset

This repository contains raw and processed data from an experiment investigating the effects of chronic temperature and diet variation on developmental performance in two cricket species: *Acheta domesticus* and *Gryllodes sigillatus*.

## Overview

Crickets were reared under controlled conditions across a range of temperatures (26°C to 41°C) and dietary protein-to-carbohydrate (P:C) ratios (1:6.3 to 2.2:1). Development was tracked weekly, including instar progression, growth, survival, and final developmental time. This repository includes:

- Raw measurement data (`sig`, `dom`)
- Individual summary data (`CRICK`, `ACRICK`)
- Associated metadata
- Analysis scripts (see `.qmd` and R files)

## Data Dictionary

### Shared Columns

| Column Name  | Description |
|--------------|-------------|
| `cricket` | Unique numeric ID for each cricket |
| `sp` | Species ID (`"sig"` for *G. sigillatus*, `"dom"` for *A. domesticus*) |
| `temperature` | Rearing temperature (°C) |
| `diet` | Numeric code for diet treatment (see Table 1 in manuscript) |
| `dietperc` | Protein content in the different diet |
| `incubator` | ID of the incubator used |
| `sexfinal` | Final sex determination |
| `first`, `end` | Start and end dates of rearing. Dates before 42 days indicate an animals that died |
| `time` | Duration of experiment for each individual (days) |
| `death` | 0 = survived, 1 = died |
| `treatment` | Composite treatment code (temperature + diet) |
| `cricket_un` | Unique identifiers for tracking individuals |

### Growth Tracking Tables (`sig`, `dom`)

| Column Name | Description |
|-------------|-------------|
| `observation` | Row number of observation |
| `day`, `week` | Day and week of observation |
| `sex` | Observed sex at time of measurement |
| `instar` | Instar stage number |
| `container` | Weight of the empty container to weight the cricket |
| `cricket_container` | Weight of the container with the cricket inside for weight |

### Survival Summary Tables (`CRICK`, `ACRICK`)

Post-processed records for each individual summarizing survival, sex, and treatment group.

## Citation

If using this dataset, please cite the associated manuscript (in review).

## License

This repository uses the MIT License.

---

Please contact Émile Vadboncoeur (emilevadboncoeur@cmail.carleton.ca) for questions.
