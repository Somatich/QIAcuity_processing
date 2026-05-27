# QIAcuity processing

This repository contains Jupyter notebooks, intermediate tables, processed data, and generated figures from the digital PCR data analysis associated with the article indexed in PubMed as **PMID: 40796890**.

Publication link: https://pubmed.ncbi.nlm.nih.gov/40796890/

## What is in this repository

The repository is mostly an analysis archive. It includes:

- raw QIAcuity digital PCR export files;
- processed CSV/XLSX tables produced during the analysis;
- Jupyter notebooks used for data processing and plotting;
- generated figures, including heatmaps, scatter plots, and correlation plots.

## Important note

The notebooks are kept here for transparency and reproducibility of the analysis history. They may be outdated and are not guaranteed to run without edits in the current repository layout.

After the original analysis was completed, the directory structure was manually cleaned up and reorganised. As a result, some paths inside the notebooks may no longer match the current folder names or file locations.

At the time the analysis code was written and used, it worked for the data and directory structure available then. To rerun the notebooks now, expect to update paths and possibly some package/environment details.

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

## Directories

- `RAW DATA/` — original QIAcuity digital PCR export files.
- `PROCESSED DATA/` — processed tables generated during analysis.
- `RESULTS/` — generated figures and visual outputs.
- `SCRIPTS/` — Jupyter notebooks used for processing and plotting.
- `.ipynb_checkpoints/` — automatically generated Jupyter checkpoint files.

## Reuse and rerunning

This repository is best treated as a record of the analysis rather than a polished software package.

If you want to rerun the analysis:

1. Open the notebooks in `SCRIPTS/`.
2. Check and update input/output paths.
3. Install missing Python packages based on notebook imports.
4. Run cells step by step and compare newly generated outputs with files in `PROCESSED DATA/` and `RESULTS/`.

## Data privacy

The repository may contain experimental sample names or metadata from digital PCR exports. Check data sensitivity before reuse or redistribution.

## License

This repository is distributed under the MIT License. See `LICENSE` for details.
