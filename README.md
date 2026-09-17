[README.md](https://github.com/user-attachments/files/32321893/README.md)
# BPSuplementsNG
# Supplement prescribing in bipolar disorder: a multi-site Nigerian cohort study

Analysis code for the manuscript *"Supplement prescribing co-occurs with
pharmacological complexity in bipolar disorder: a multi-site Nigerian cohort
study"*.

---

## Contents

| File | Description |
|---|---|
| `supplement_analysis.R` | Complete analysis script; reproduces all reported results |
| `output/` | Generated on run — tables (.docx), figures (.png), session info |

---

## Requirements

**R version 4.5.3** or later.

The script installs any missing packages automatically:

```
readxl, dplyr, tidyr, purrr, stringr, tibble, forcats,
FNN, ResourceSelection, car, gtsummary, flextable,
ggplot2, scales, ggrepel, patchwork, RColorBrewer
```

---

## Usage

1. Place `BDPharm.xlsx` in the working directory
2. Open `supplement_analysis.R` in R or RStudio
3. Run the script from top to bottom

All results print to the console. Tables and figures are written to `output/`.

The script stops with an informative error if the data file is not found.

---

## Data availability

The dataset contains identifiable clinical information from ten Nigerian
psychiatric facilities and is not publicly deposited. Requests for access
should be directed to the corresponding author and are subject to the
data-sharing agreement of the Multicentre Analysis of Pharmacological
Treatment Patterns (MAP-Study).

---

## Analysis overview

The script is organised by manuscript section:

| Section | Analysis |
|---|---|
| 2.2 | Participant flow and record completeness |
| 2.3 | Data import and variable derivation |
| 2.4 | Supplement identification and name standardisation |
| 2.5 | Anthropometrics, KNN imputation, Mifflin–St Jeor BMR |
| 2.6 | Pharmacotherapy variables and index episode |
| 3.1 | Table 1, supplement persistence, Supplementary Table 1 |
| 3.2 | Imputation sensitivity analysis, Supplementary Table 2 |
| 3.3 | Table 2, supplement frequency |
| 3.4 | Table 3, logistic regression, Supplementary Tables 3–4 |
| 3.5 | Estimated BMR by supplement status and persistence |
| 3.6 | Spearman correlations and moderated regression |

---

## Statistical notes

**Multiplicity correction** differs by analysis and is applied as follows:

| Analysis | Method |
|---|---|
| Spearman correlations (Section 3.6) | Bonferroni |
| Pairwise persistence comparisons (Section 3.5) | Benjamini–Hochberg |
| Supplement users vs non-users (Supplementary Table 1) | Benjamini–Hochberg |

**Missing data.** Height and weight were imputed using k-nearest neighbour
smoothing (k = 5) with age, sex, polarity type count and total episode burden
as predictors, weighted by inverse distance. Heights below 100 cm were treated
as data-entry errors and imputed. All BMR analyses are repeated in the
complete-case subgroup as a sensitivity analysis.

**Estimated BMR.** Basal metabolic rate was calculated from the sex-specific
Mifflin–St Jeor equation, not measured by indirect calorimetry, and is
reported throughout as *estimated* BMR.

**Symptom severity.** No validated rating instrument was administered. Episode
counts and psychotropic burden are used as indirect proxies for illness history
and treatment complexity, and are not equivalent to severity measurement.

---

## Citation

Ejiohuo O, Adiukwu FN, Salihu MO, Adegoke BO, Onyishi U,
Charles-Ugwuagbo IC, Uteh CO, Ibrahim AM, Abba FM, Kareem YA, Adesina IO.
*Supplement prescribing co-occurs with pharmacological complexity in bipolar
disorder: a multi-site Nigerian cohort study.* [PharmaNutrition, 2026].

---

## Contact

Ovinuchi Ejiohuo — ovinuchi.ejiohuo@up.poznan.pl
Frances Nkechi Adiukwu — frances.adiukwu@uniport.edu.ng
