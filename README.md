# QIAcuity processing

Utilities and notebooks for processing **QIAcuity digital PCR (dPCR)** output files and preparing analysis-ready tables, quality-control summaries, figures, and downstream reports.

## Overview

This repository contains raw QIAcuity export files, processed data tables, analysis notebooks, and generated figures. The main goals are:

- collect and organise raw QIAcuity export files;
- process and normalise assay output tables;
- generate analysis-ready CSV/XLSX files;
- create heatmaps, scatter plots, correlation plots, and polar-coordinate visualisations;
- keep the QIAcuity analysis workflow reproducible.

## Repository structure

```text
QIAcuity_processing/
├── .ipynb_checkpoints/
├── PROCESSED DATA/
├── RAW DATA/
├── RESULTS/
│   ├── correlations/
│   ├── heatmaps/
│   └── scatters/
└── SCRIPTS/
```

## Input data

Original QIAcuity export files are stored in `RAW DATA/`. Keep raw data unchanged so that results can be reproduced from the original exports.

Current raw data files:

- `psapsgpl1-analysis.csv`
- `psapsgpl3 kid tes spl si uncvsir3 hrt lun-analysis.csv`
- `psapvsir2-analysis.csv`
- `slccdh2-analysis.csv`
- `slcvsir1-analysis.csv`
- `slcvsir3 unccdh3 kid tes-analysis.csv`
- `unccdh1-analysis.csv`
- `uncsgpl2-analysis.csv`

## Expected workflow

1. Export data from the QIAcuity software.
2. Save the untouched export files in `RAW DATA/`.
3. Run or update the analysis notebooks in `SCRIPTS/`.
4. Save processed tables to `PROCESSED DATA/`.
5. Save generated figures to `RESULTS/`.
6. Use processed CSV/XLSX files and exported figures for downstream analysis and reporting.

## Installation

Clone the repository:

```bash
git clone https://github.com/Somatich/QIAcuity_processing.git
cd QIAcuity_processing
```

If running the notebooks locally, create and activate a Python virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate      # macOS/Linux
# .venv\Scripts\activate       # Windows
```

Install the packages required by the notebooks. A `requirements.txt` file is not present yet, so dependencies should currently be installed manually based on notebook imports.

## Usage

Open the notebooks in JupyterLab or Jupyter Notebook:

```bash
jupyter lab SCRIPTS/
```

Main notebooks:

- `SCRIPTS/heatmap.ipynb` — heatmap generation and related visualisation steps;
- `SCRIPTS/scatters.ipynb` — well-level scatter plot generation and statistical filtering.

Processed outputs are stored in `PROCESSED DATA/`, and generated figures are stored in `RESULTS/`.

## Outputs

Current output categories include:

- processed Excel and CSV tables in `PROCESSED DATA/`;
- correlation plots and polar-coordinate figures in `RESULTS/correlations/`;
- SVG heatmaps in `RESULTS/heatmaps/`;
- well-level scatter plot JPG files in `RESULTS/scatters/`.

## Reproducibility notes

- Do not edit files in `RAW DATA/` manually.
- Keep notebook parameters and processing assumptions documented.
- When adding new scripts, document input files, output files, and required packages.
- Consider adding a `requirements.txt` or `environment.yml` file to make the Python environment reproducible.
- Consider moving exploratory or temporary notebook checkpoints out of version control if they are not needed.

## Data privacy

QIAcuity exports may contain sample identifiers or experiment metadata. Do not commit confidential, patient-related, or proprietary raw data to the repository. Prefer anonymised demo data for examples and tests.

## License

No license has been specified yet. Add a `LICENSE` file before distributing or reusing the code outside the project team.
