Project Repository — DTSC 5082 (Group 2)

University of North Texas
Course: Data Science Capstone (DTSC 5082)
Section: 020 (Offline)
Group: 2

1. Overview

This repository contains the complete set of source code, Jupyter notebooks, and supporting documentation for our DTSC 5082 Group 2 project.
The project was developed entirely in Google Colab, leveraging multimodal clinical data from the MIMIC-IV database.

Due to the nature of clinical datasets and the computational workflows involved (e.g., ClinicalBERT embeddings, cohort construction, unsupervised clustering, UMAP dimensionality reduction), several intermediate and raw data files are extremely large and exceed standard GitHub upload limitations.

For this reason, only code files, notebooks, and lightweight documentation are included in this repository. All large datasets and outputs are hosted externally.

2. Excluded Files and Rationale

GitHub enforces strict file size limitations:

Maximum file size for direct upload: 100 MB

Repositories cannot reliably support multi-GB datasets

The following categories of files were not uploaded:

2.1 Raw MIMIC-IV Tables

These include high-volume clinical datasets such as:

labevents

discharge

radiology

Each of these tables is several hundred megabytes to multiple gigabytes in size.

2.2 Large Intermediate Outputs

These were generated during analysis and are too large for GitHub:

ClinicalBERT embedding parquet files

Cohort extraction files (structured + multimodal)

UMAP reduced embeddings (20D and 2D)

HDBSCAN cluster outputs

High-dimensional engineered feature matrices

Large visualization and SHAP artifacts

These files are essential for reproducing the project but exceed GitHub storage constraints.

3. Access to Full Project Data and Outputs

All large datasets and outputs required to fully reproduce the workflow are available via Google Drive.

Google Drive Repository (Large Files + Full Colab Environment)

🔗 https://drive.google.com/drive/folders/1e5-gv4B0m7ERHUb_ouctwvvn3V--FD7d?usp=sharing

This Drive folder contains:

Raw MIMIC-IV extracted tables

Complete ClinicalBERT embeddings

Full multimodal feature matrices

UMAP + HDBSCAN outputs

Large modeling results and logs

All artifacts exceeding GitHub’s upload limits

A full copy of the original Colab workspace

4. Reproducibility Instructions

To reproduce the project end-to-end:

Clone/download this GitHub repository
Contains all notebooks (.ipynb), scripts, and documentation.

Access the Google Drive folder (link above).
Download or reference the necessary data files.

Open the notebooks in Google Colab (recommended).

Mount Google Drive inside Colab using:

from google.colab import drive
drive.mount('/content/drive')


Place the large files in the same directory path used during development (preserved in the Drive folder).

Execute each notebook in numerical order (Phase 1 → Phase 10).
The workflow will run successfully once all required files are present.

5. Notes for Reviewers

This repository contains everything GitHub can host within its size limits.

All code is complete and functional.

The Google Drive link provides the entire data environment required for reproduction.

This README formally documents the limitations and provides transparent instructions for accessing the complete dataset.
