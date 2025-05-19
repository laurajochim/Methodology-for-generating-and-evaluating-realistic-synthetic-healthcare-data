This folder contains everything needed to process, generate, and evaluate synthetic TCGA BRCA breast cancer data.

1. Data Layout

data/raw/    : Raw TCGA BRCA archives (ZIP files, needs to be unzipped before working with it)

data/clean/  : Cleaned BRCA data saved as .csv

data/synthetic/: Generated synthetic datasets (synthpop, vine copula, ctGAN)

2. Cleaning

Rscript BRCA/cleaning/tcga_cleaning.Rmd

Reads from data/raw/, applies dataset-specific cleaning and rearranging, and writes RPPA_nona.csv to data/clean/.

3. Generation

Rscript BRCA/generation/tcga_data_generation.Rmd

Loads cleaned data, creates synthetic datasets, and saves to data/synthetic/.

4. Evaluation

Rscript BRCA/evaluation/tcga_evaluation.Rmd

Performs comparisons between synthetic and real data on three levels (uni-, bi-, and multivariate levels).
