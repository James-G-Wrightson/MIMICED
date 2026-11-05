# MIMICED
**Analysis of the MIMIC-IV-ED database**

This repository builds the analysis data for a study of avoidable emergency department visits in the MIMIC-IV-ED v2.2 database.

## Data
The data for this analysis are from the [MIMIC-IV-ED](https://physionet.org/content/mimic-iv-ed/2.2/) version 2.2 database from Physionet. The data are available to the public, but the analyst is required to complete the [CITI Data or Specimens Only Research](https://physionet.org/about/citi-course/) training. This database was linked to the main hosp module from the [MIMIC-IV](https://www.physionet.org/content/mimiciv/3.0/hosp/#files-panel) version 3.0 database to get extra patient and diagnosis data (the files "patients.csv.gz", "diagnoses_icd.csv.gz", and "d_icd_diagnoses.csv.gz"). 
To process the data, the raw .csv.gz files must be downloaded into this folder: the MIMIC-IV-ED files into `mimic-iv-ed-2.2/ed/` and the hosp files into `hosp/`. The Diagnosis (NYU ED) label also needs four third-party code-list files; the next section lists them.

## Required external files (download manually)
The data notebook (`1_mimic_data.ipynb`) checks for these files at the start and stops, naming any that are missing, where to get them and where to put them. They cannot be fetched by script (the hosts block non-browser downloads), so download each one in a web browser and save it in this `MIMICED/` folder under exactly the name shown.

The four code lists below are third-party files, licensed by their authors. They are not redistributed in this repository, and `.gitignore` excludes them (`*.xlsx`, `hesr12638-sup-*.txt`) so they cannot be committed by accident.

| File name expected by the notebook | Source | Columns the notebook uses |
|---|---|---|
| `NYU ED Algorithm - ICD10 Codes - Updated 2.4.25.xlsx` | NYU Wagner, Billings ED algorithm page: <https://wagner.nyu.edu/faculty/billings/nyued-background> ("Download list of ICD-10 codes"). The page now links a later version (`Updated 5.5.25`); the 2.4.25 version used here is at <https://wagner.nyu.edu/files/faculty/NYU%20ED%20Algorithm%20-%20ICD10%20Codes%20-%20Updated%202.4.25.xlsx> | first sheet: `ICD10`, `ICD10_Description` (dropped), `Non_Emergent`, `Emergent__PC_Treatable`, `ED_Care_Needed__Preventable_Avoi`, `ED_Care_Needed__not_Preventable`, `Alcohol`, `Drug`, `Injury`, `Psych`, `Unclassified` |
| `NYU_ED_Algorithm_-_ICD-9_Codes_-_6.23.15.xlsx` | Same NYU Wagner page ("Download list of ICD-9 codes") | first sheet: `discharge_dx`, `Dx_Name`, `Dx_Short_Name` and `post2009` (dropped), `Non_Emergent`, `Emergent__PC_Treatable`, `ED_Care_Needed__Preventable_Avoi`, `ED_Care_Needed__not_Preventable_`, `Alcohol`, `Drug`, `Injury`, `Psych`, `Unclassified` |
| `hesr12638-sup-0007-appendixs6.txt` | Johnston KJ, Allen L, Melanson TA, Pitts SR. A "Patch" to the NYU Emergency Department Visit Algorithm. *Health Services Research* 2017;52(4):1264–1276. doi:[10.1111/1475-6773.12638](https://doi.org/10.1111/1475-6773.12638); PubMed Central [PMC5517669](https://pmc.ncbi.nlm.nih.gov/articles/PMC5517669/). Supporting information, Appendix S6 (ICD-9). Wiley may serve it under a different name (e.g. `hesr12638-sup-0006-AppendixS6.txt`): rename it to the name in the first column | tab-separated: `ICD9`, `noner`, `epct`, `edcnpa`, `edcnnpa`, `injury`, `psych`, `alcohol`, `drug` |
| `hesr12638-sup-0007-appendixs7.txt` | Johnston et al. 2017 (as above), supporting information, Appendix S7 (ICD-10) | tab-separated: `icd10`, `noner`, `epct`, `edcnpa`, `edcnnpa`, `injury`, `psych`, `alcohol`, `drug` |

The notebook reads the two NYU lists, then replaces any NYU code that also appears in the Johnston et al. extension with the extension's row (same code and ICD version), and adds the extension's other codes. Each visit's primary diagnosis code is looked up in this combined list by code and ICD version, and the visit is labelled potentially avoidable when the non-emergent plus emergent/primary-care-treatable probabilities sum to more than 0.5. `nyu_source_summary.csv` (written by the notebook) gives counts only: rows read from each list, codes overridden, and how many diagnosis codes and visits matched each source.

The MIMIC files are also required, from PhysioNet (credentialed access; see Data above): `ed/diagnosis.csv.gz`, `ed/edstays.csv.gz`, `ed/medrecon.csv.gz`, `ed/pyxis.csv.gz`, `ed/triage.csv.gz` and `ed/vitalsign.csv.gz` from [MIMIC-IV-ED 2.2](https://physionet.org/content/mimic-iv-ed/2.2/) in `MIMICED/mimic-iv-ed-2.2/ed/`, and `patients.csv.gz`, `d_icd_diagnoses.csv.gz` and `diagnoses_icd.csv.gz` from the [MIMIC-IV 3.0](https://physionet.org/content/mimiciv/3.0/) hosp module in `MIMICED/hosp/`. These are also excluded by `.gitignore`.

## Requirements
1. The data wrangling was done in R 4.5.2 using Apache Arrow.
2. R packages are installed and loaded with `pacman` at the start of the notebook.
3. The clustering of the free-text chief complaint was done in Python 3.12 (3.12.13 in the locked environment).
4. The Python environment is defined in `pyproject.toml` and locked in `uv.lock` (see "Python environment (uv)" below); `requirements.txt` is exported from the lock file for pip users.
5. The raw data files and the four code lists must be downloaded before the notebooks can be run.

### Recorded package versions
`pacman` installs whichever package versions are current on the day, so the notebooks are not pinned by default. Two files record a combination known to work:

- **R** — `renv.lock`, captured on R 4.5.2. To install those exact versions into a project-local library, run `renv::restore()` from this folder. This is optional; the notebooks run normally without it, using `pacman` as before.
- **Python** — `pyproject.toml` + `uv.lock` (exported to `requirements.txt`). Three of its pins are load-bearing and are explained in comments at the top of `pyproject.toml` and `requirements.txt`. Do not relax them: with any of the three left unpinned, pip resolves a combination in which `2_chiefcomp.ipynb` cannot import its libraries or load its model.

### Python environment (uv)
The Python notebook (`2_chiefcomp.ipynb`) uses a [uv](https://docs.astral.sh/uv/)-managed environment defined in `pyproject.toml` and locked in `uv.lock` (Python 3.12). From this folder:

```
uv sync                                   # builds .venv from uv.lock
uv run python -m ipykernel install --user --name mimiced --display-name "mimiced (uv)"
```

Then select the "mimiced (uv)" kernel in Jupyter. `requirements.txt` is exported from `uv.lock` (`uv export --no-hashes --format requirements-txt -o requirements.txt`, with the explanatory comment block re-added at the top) for anyone using pip. Do not relax the `numpy==1.26.4`, `scipy==1.13.1` or `transformers==4.51.3` pins. The `.venv/` folder is excluded by `.gitignore`.

## Workflow
Run the [data](1_mimic_data.ipynb) notebook to join and wrangle the data, then the [chief complaint](2_chiefcomp.ipynb) notebook to create categories for the free-text chief complaint.

The data notebook writes two files: `ed_join_cc.parquet`, one row per ED visit with a discharge diagnosis (the analysis data), and `ed_no_diagnosis.parquet`, the small number of visits without one, carried through the same pipeline so they can be described; their Diagnosis label is NA because there is nothing to classify.

### Choosing and checking the clusters (`2_chiefcomp.ipynb`)
`2_chiefcomp.ipynb` cleans the free-text chief complaint, embeds it with a BioBERT sentence transformer, reduces the vectors to 80 principal components and clusters them with k-means. Every step is seeded (`RANDOM_STATE = 42`) and every slow step is cached, so the labels are reproducible from the raw data. The number of clusters is chosen from a scan of k = 2 to 100: for each k the notebook records inertia and the silhouette, and for k = 2 to 19, 25, 30, 40, 50, 60, 75, 90 and 100 the agreement (adjusted Rand index) between the seed-42 fit and 20 further random starts. Neither curve has a peak or an elbow, so k is taken as the smallest value on the scan at which the solution is reproducible to Steinley's "good" standard (median ARI at least 0.80) while the silhouette is above the 0.25 floor below which Kaufman and Rousseeuw describe no substantial structure: **k = 75**. Each cluster is named automatically after its most common cleaned complaint, so no label is written by hand. The grid neighbours k = 50 and k = 100 are written out for the supplement's sensitivity tables.

```
uv run jupyter nbconvert --to notebook --execute --inplace \
    --ExecutePreprocessor.timeout=-1 2_chiefcomp.ipynb
```

Caches (all excluded by `.gitignore` except the csv files): `chiefcomp_embeddings.npy` (the 768-dimensional vectors, 1.3 GB; about 80 minutes to compute), `chiefcomp_pca80.npy` and `chiefcomp_pca_variance.npy`, `chiefcomp_ref_labels.npz` (the seed-42 labels for every k scanned), `chiefcomp_validity_k.csv` (inertia and silhouette by k; about 90 minutes to compute) and `chiefcomp_stability.csv` (one row per k and random start; several hours, and any k added to the scan is computed and appended without refitting the others). With the caches present the notebook runs in a few minutes; delete a file to recompute that step. Outputs for the analysis notebooks: `chiefcomp_clustered.parquet` (`stay_id`, `chiefcomplaint`, `cc_cleaned`, `cluster`, `cluster_name`; k = 75), `chiefcomp_clustered_k50.parquet` and `chiefcomp_clustered_k100.parquet` (`stay_id` plus `cluster_k50` / `cluster_name_k50` and the same for 100), `chiefcomp_cluster_names.csv` (every cluster at k = 75, 50 and 100 with its name, size and most common complaints and phrases), and the two figures `chiefcomp_figure_1_pca_variance.png` and `chiefcomp_validity_k.png`.

The original analysis used k = 12 chosen by eye from the elbow plot and left the PCA unseeded, so its labels could not be regenerated. That run is kept, unused, in `archive_k12/`: the old notebook, its labels (`chiefcomp_clustered.parquet`), the pickle with its embeddings (`chiefcomp_data.pkl`, from which `chiefcomp_embeddings.npy` was extracted), the k = 8 and 14 sensitivity files and naming aids, and its figure.





