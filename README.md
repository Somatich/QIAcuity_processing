# QIAcuity processing

Utilities and project scaffolding for processing **QIAcuity digital PCR (dPCR)** output files and preparing analysis-ready tables, quality-control summaries, and downstream reports.

> Status: initial repository setup. The README describes the intended project structure and workflow; update the command examples once the processing scripts are added.

## Overview

This repository is intended to collect scripts and helper functions for working with QIAcuity dPCR exports. The main goals are:

- import raw QIAcuity export files;
- standardise sample, assay, plate, and replicate metadata;
- validate required columns and flag malformed records;
- calculate or collect concentration/copy-number metrics from exported data;
- generate clean tabular outputs for statistical analysis and reporting;
- make the processing workflow reproducible and easy to rerun.

## Suggested project structure

```text
QIAcuity_processing/
├── data/
│   ├── raw/              # Original QIAcuity exports; do not edit manually
│   ├── interim/          # Intermediate processed files
│   └── processed/        # Final analysis-ready outputs
├── notebooks/            # Exploratory analysis notebooks
├── reports/              # Generated reports, figures, and QC summaries
├── src/                  # Processing code
├── tests/                # Unit tests and small test fixtures
├── README.md
└── requirements.txt      # Python dependencies, if using Python
```

The exact structure can be adjusted as the repository grows.

## Input data

Place original QIAcuity export files in `data/raw/`. Keep raw data unchanged so that results can be reproduced from the original exports.

Recommended file naming pattern:

```text
YYYY-MM-DD_project_plate-or-run_description.ext
```

Example:

```text
2026-05-27_qiacuity_plate01_raw_export.csv
```

## Expected workflow

1. Export data from the QIAcuity software.
2. Save the untouched export files in `data/raw/`.
3. Run the processing script or notebook.
4. Review generated QC summaries.
5. Use files from `data/processed/` for downstream analysis.

## Installation

Clone the repository:

```bash
git clone https://github.com/Somatich/QIAcuity_processing.git
cd QIAcuity_processing
```

If the project uses Python, create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate      # macOS/Linux
# .venv\Scripts\activate       # Windows
```

Install dependencies once `requirements.txt` is added:

```bash
pip install -r requirements.txt
```

## Usage

Add the actual processing command here once the main script is available. A future command may look like this:

```bash
python src/process_qiacuity.py \
  --input data/raw/example_export.csv \
  --output data/processed/example_processed.csv
```

For exploratory analysis, use notebooks in `notebooks/` and save final tables or figures to `data/processed/` or `reports/`.

## Outputs

Typical outputs may include:

- cleaned assay/sample tables;
- replicate-level summaries;
- concentration or copy-number tables;
- QC flags and warnings;
- figures and report-ready summaries.

## Reproducibility notes

- Do not edit files in `data/raw/` manually.
- Keep processing parameters in scripts, configuration files, or notebooks under version control.
- Record software versions and package dependencies.
- Use small anonymised example files for tests when possible.

## Development

Recommended checks before committing changes:

```bash
python -m pytest
```

If formatting or linting tools are added later, document the exact commands here.

## Data privacy

QIAcuity exports may contain sample identifiers or experiment metadata. Do not commit confidential, patient-related, or proprietary raw data to the repository. Prefer anonymised demo data for examples and tests.

## License

No license has been specified yet. Add a `LICENSE` file before distributing or reusing the code outside the project team.
