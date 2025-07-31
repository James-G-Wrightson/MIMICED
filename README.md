# MIMICED
**Analysis of the MIMIC-IV-ED database**

This is the master repo for three projects that use the MIMIC-IV-ED v2.2 database to explore the frequency, characteristics, and prediction of avoidable emergency department visits. 

## Data
The data for this analysis are from the [MIMIC-IV-ED](https://physionet.org/content/mimic-iv-ed/2.2/) version 2.2 database from Physionet. The data are available to the public, but the analyst will be required to complete the [CITI Data or Specimens Only Research](https://physionet.org/about/citi-course/) training.  This database was linked to the main hosp module from the [MIMIC-IV](https://www.physionet.org/content/mimiciv/3.0/hosp/#files-panel) version 3.0 database to get extra patient and diagnosis data (the files "patients.csv.gz", "diagnoses_icd.csv.gz", and "d_icd_diagnoses.csv.gz"). 
To process the data, the raw .gz.csv files need to be downloaded to the source folder. The MIMIC-IV-ED files need to be downloaded to a folder called 'mimic-iv-ed-2.2', and the hosp files to a folder called 'hosp'.

To create the ‘nyu’ label for potentially avoidable visits, the original (excel) files for both the ICD-9 and ICD-10 codelists must be downloaded from the [NYU Wagner](https://wagner.nyu.edu/faculty/billings/nyued-background) website. The extension files from [Johnstone et al](https://onlinelibrary.wiley.com/doi/full/10.1111/1475-6773.12638?saml_referrer) should also be downloaded for both [ICD-9](https://onlinelibrary.wiley.com/action/downloadSupplement?doi=10.1111%2F1475-6773.12638&file=hesr12638-sup-0006-AppendixS6.txt) and [ICD-10](https://onlinelibrary.wiley.com/action/downloadSupplement?doi=10.1111%2F1475-6773.12638&file=hesr12638-sup-0007-AppendixS7.txt)   

## Requirements
1. The data wrangling was done in R 4.5.0 using Apache Arrow.
2. Packages are managed using pacman, and code is included in the notebook
3. The NLP of the free text chief complaint was done in Python 3.12.2
4. A requirements.txt file is included for the necessary libraries
5. The raw data files must be downloaded before the notebooks can be run

## Workflow
To start, run the [MIMIC data](/1_mimic_data.ipynb) notebook to join and wrangle the data, and then run the [Chief Complaint](/2_chiefcomp.ipynb) notebook to create categories for the free-text chief complaint




