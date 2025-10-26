# Data Availability Statement

**Project:** Subcontractor-Delay-AI — AI-based early detection of subcontractor performance deterioration on FDOT roadway projects.

## What is shared
- **Code (public):** All analysis, parsing, and modeling code is in this GitHub repository under the **MIT License**.
- **De-identified data (public):** Synthetic examples and derived, aggregate features (counts, rates, timelines) are provided in `data/processed/` to reproduce figures and tables **without exposing sensitive project information**.
- **Documentation (public):** Data dictionary and methods live in `docs/`.

## What is restricted (not public)
- **Raw documents:** Daily reports, emails, notices, schedules, and pay applications contain confidential and personally identifying information. These files are **not** posted publicly. File paths may appear in `data/` as placeholders only.
- **Third-party materials:** Any content owned by FDOT/OHLA/subcontractors that cannot be redistributed.

## Access to restricted data
Researchers may request limited access for verification purposes, subject to approval and a data-use agreement (DUA) and redaction requirements.  
**Contact:** [your email or GitHub issues link]

## Ethics & redaction
All shared materials remove personal names, phone numbers, and emails; contract numbers and locations may be coarsened. Aggregates are reported at weekly/monthly levels to avoid re-identification.

## File formats & structure
- **Public artifacts:** CSV/Parquet/JSON summaries in `data/processed/`; figures in `output/`.
- **Code:** Python 3.11 package in `src/`, notebooks in `notebooks/`.
- **Provenance:** Each table has a `source_note` column describing originating document classes (e.g., daily reports, emails).

## Reuse & license
- **Code:** MIT License (see `LICENSE`).
- **Data derivatives:** CC BY 4.0 recommended *(or specify your choice)*. If you adopt this, add a short `LICENSE-DATA` note:
  > Data derivatives © [Year] Caden Himes, licensed under CC BY 4.0.

## Versioning & citation
Releases are versioned on GitHub. If a DOI is minted via Zenodo, cite the **Concept DOI** for the project and the **Version DOI** for a specific release.  
**DOI:** *(insert when available)*

**How to cite this repository:**
> Caden Himes (2025). Subcontractor-Delay-AI: Early warning for subcontractor performance on FDOT projects. Version X.Y.Z. GitHub. DOI: *(insert)*

## Replication
Steps to reproduce key results:
1. Create a Python 3.11 env and install `requirements.txt`.
2. Run `src/pipelines/build_features.py` on `data/processed/` (public aggregates).
3. Open `notebooks/01_eda.ipynb` and `02_model.ipynb` to regenerate figures/tables.

