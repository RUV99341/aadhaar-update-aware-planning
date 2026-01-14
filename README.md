# UIDAI Data Hackathon 2026 — Aadhaar Enrolment & Update Lifecycle Analysis

![Hackathon](https://img.shields.io/badge/Hackathon-UIDAI%20Data%20Hackathon%202026-blue)
![Python](https://img.shields.io/badge/Python-Data%20Science-green)

Author: Ritesh Verma

Project Summary

This repository contains an analysis of Aadhaar enrolment, biometric updates, and demographic updates provided for the UIDAI Data Hackathon 2026. The goal is to surface operationally actionable insights — national and local trends, update-heavy locations, and planning indicators that go beyond enrolment-only metrics.

Key Goals

- Compare enrolment vs update activity over time and geography.
- Identify states/districts with disproportionately high update workload.
- Produce update-load indices useful for resource planning.

Datasets

The analysis uses three aggregated, anonymized datasets supplied for the hackathon (stored under `data/raw/`).

- Enrolment: new Aadhaar registrations by age group.
- Biometric updates: biometric update activity by age group.
- Demographic updates: demographic detail updates by age group.

Repository Structure

- [data/](data/) — raw and cleaned CSVs (sensitive data removed/aggregated).
- [notebooks/](notebooks/) — sequential analysis notebooks:
	- `01_data_understanding.ipynb` — schema and coverage checks
	- `02_eda.ipynb` — exploratory analysis and visuals
	- `03_insights_models.ipynb` — synthesis, indices and maps
- [visuals/](visuals/) — charts and static exports used in the report
- [report/](report/) — final write-up and presentation-ready figures

Quick Start

1. Create a Python environment and install dependencies:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

2. Place raw datasets in `data/raw/` (as provided by the hackathon).

3. Start Jupyter and run notebooks in order:

```powershell
jupyter notebook
# Open and run
# notebooks/01_data_understanding.ipynb
# notebooks/02_eda.ipynb
# notebooks/03_insights_models.ipynb
```

Notes on reproducibility

- The notebooks use standard libraries listed in `requirements.txt`.
- Notebooks are ordered to build from schema checks → EDA → insights.
- Charts exported to `visuals/charts/` are referenced in the report.

Key Findings (summary)

- Enrolment volumes are increasingly driven by children; adult enrolment has saturated in many regions.
- Biometric and demographic updates form a sustained operational workload exceeding enrolment-only planning in several districts.
- Update activity is geographically concentrated — a small set of states/districts account for a large share of updates.

Recommendations (operational)

- Use update-load indices (notebooks supply calculation) for staffing and infrastructure allocation.
- Prioritize update-heavy districts for targeted support and monitoring.
- Separate enrolment and update planning where feasible to avoid resource contention.

Limitations

- Data is aggregated and privacy-preserving; individual-level behavior cannot be inferred.
- Update reasons are not provided, limiting causal interpretation.

Credits & License

This analysis was created for the UIDAI Data Hackathon 2026. Use of the hackathon datasets is subject to the hackathon's terms. Code in this repository is provided under the MIT License.

Contact

For questions or collaboration, open an issue or contact the author: Ritesh Verma.

—
Updated README for hackathon submission. See the notebooks in [notebooks/](notebooks/).