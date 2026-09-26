# TNF-α -308 G>A polymorphism and dengue severity

This repository contains the R/Quarto code used for the statistical analyses of the manuscript:

**Molecular Detection of the -308 G/A Polymorphism in the Tumor Necrosis Factor Alpha (TNFα) Gene Promoter and its Relationship with the Development of Severe Dengue in Patients from Urabá Subregion, Antioquia-Colombia**
## Study overview

This study evaluated the association between the **TNF-α -308 G>A promoter polymorphism** and dengue severity among 92 patients with laboratory-confirmed dengue from the Urabá subregion of Antioquia, Colombia.

Patients were classified into three clinical groups:

- Dengue without warning signs (DWOS), n = 30
- Dengue with warning signs (DWWS), n = 43
- Severe dengue (SD), n = 19

The statistical analyses were conducted in R and are provided here to improve transparency and reproducibility.

## Repository contents

- `Script_R.qmd`: Quarto document containing the R code used for data preparation and statistical analyses.

## Analyses included

The Quarto script includes:

- Data import and variable verification
- Recoding of dengue severity groups
- Descriptive analysis of demographic variables
- Analysis of demographic characteristics by dengue severity group
- Analysis of clinical characteristics by dengue severity group
- Identification of TNF-α -308 A-allele carriers
- Crude Firth penalized logistic regression
- Age-adjusted Firth penalized logistic regression
- Firth penalized logistic regression adjusted for age and primary/secondary infection status
- Pairwise adjusted comparisons:
  - SD vs DWOS
  - SD vs DWWS
  - DWWS vs DWOS
- Comparison of crude and adjusted effect estimates
- Sensitivity analysis comparing severe and non-severe dengue

## Statistical approach

Because of the low frequency of TNF-α -308 A-allele carriers and the presence of sparse cells, **Firth penalized logistic regression** was used to reduce small-sample and sparse-data bias.

The adjusted models included age and primary/secondary infection status as prespecified clinically relevant covariates. Age was modeled per 10-year increase.

Results are reported as odds ratios (ORs) or adjusted odds ratios (aORs) with 95% confidence intervals.

## Software and R packages

The analyses were performed in R using the following packages:

- `readxl`
- `dplyr`
- `gtsummary`
- `logistf`

The analysis was developed as a Quarto (`.qmd`) document.

## Data availability

The individual-level clinical dataset is not included in this public repository because it contains participant-level clinical information and is subject to the confidentiality and ethical requirements described in the manuscript.

Researchers interested in data access should contact the corresponding author, subject to applicable ethical and institutional approvals.

## Reproducing the analysis

The analysis script is provided in `Script_R.qmd`.

To run the analysis:

1. Install R and Quarto.
2. Install the required R packages.
3. Obtain authorized access to the study dataset.
4. Place the dataset in an appropriate local directory.
5. Update the dataset path in `Script_R.qmd`.
6. Render the Quarto document or execute the R code interactively.

Required packages can be installed using:

```r
install.packages(c(
  "readxl",
  "dplyr",
  "gtsummary",
  "logistf"
))

Authors

Jorge Emilio Salazar Flórez, Ronald Guillermo Peláez Sánchez, Luz Stella Giraldo Cardona, and collaborators.

Citation

If using the code from this repository, please cite the associated manuscript.

The full citation will be added after publication.
