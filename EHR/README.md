This folder contains everything needed to process, generate, and evaluate synthetic EHR data.

1. Data Layout
   
data/raw/ : Raw EHR archives (ZIP files, needs to be unzipped before working with it)

data/clean/ : Cleaned EHR data saved as .csv

data/synthetic/: Generated synthetic datasets (synthpop, vine copula, ctGAN)

2. Cleaning
   
Rscript EHR/cleaning/ehr_cleaning.Rmd

Reads from data/raw/, applies dataset-specific cleaning and rearranging, and writes ehr.csv to data/clean/.

3. Generation
   
Rscript EHR/generation/ehr_data_generation.Rmd

Loads cleaned data, creates synthetic datasets, and saves to data/synthetic/.

4. Evaluation
   
Rscript EHR/evaluation/ehr_evaluation.Rmd

Performs comparisons between synthetic and real data on three levels (uni-, bi-, and multivariate levels).
