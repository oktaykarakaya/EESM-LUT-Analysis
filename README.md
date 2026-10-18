# EESM-LUT Analysis

Python and Google Colab code for numerical analysis of finite-element-analysis (FEA) lookup tables for an externally excited synchronous machine (EESM).

## Overview

This project examines the differences between separately interpolated incremental-matrix maps and derivatives of interpolated flux-linkage maps. The analysis covers:

- Grid-knot and off-grid Jacobian consistency and local Hurwitz stability
- Interpolation, grid-resolution, and operating-domain sensitivity
- Fixed-step numerical integration using Euler, Heun, RK4, and related benchmarks
- Secondary residual-corrected Euler diagnostics and robustness checks

## Repository Structure

```text
EESM-LUT-Analysis/
├── EESM_LUT_Colab.ipynb   # Google Colab analysis notebook
└── README.md              # This file
```

## How to Run

1. Open `EESM_LUT_Colab.ipynb` in [Google Colab](https://colab.research.google.com/).
2. Run the cells in order. When prompted, upload **one ZIP file** containing `Parameters.mat` and `Tables.mat`.
3. Keep `FULL_RUN = True` to run the complete analysis. Computation-intensive stages can take considerable time, especially without a GPU.
4. After a successful full run, the notebook creates downloadable ZIP archives containing the results and validation records.

No Google Drive mount or separate reference-metrics CSV is required.

## Outputs

The full-run results archive is designed to include:

- **8 figures:** Figures 2–6 and S1–S3 (PNG, 600 dpi); Figure 1 is intentionally excluded
- **11 tables:** Tables 1–9 and S1–S2 (CSV)
- **2 additional diagnostic CSV files** under `Results/Diagnostics`

Internal consistency checks and run information are saved separately. The notebook's checks do not replace an independent comparison with reported numerical results.

## Dependencies

The main Python libraries are `numpy`, `pandas`, `scipy`, `matplotlib`, `torch`, and `optuna`. The notebook includes an installation step for Optuna if needed.

## Data

The input data are provided by Bergheim and Jonczyk for a 100 kW externally excited synchronous machine:

[Zenodo dataset — DOI: 10.5281/zenodo.18822007](https://doi.org/10.5281/zenodo.18822007)

The source MAT files are **not included** in this repository. Data use is subject to the original dataset's terms.

## Citation

If you use this code or the associated analysis, please cite:


## License

No separate code license is specified here.

## Contact

For questions about the code or analyses: [karakaya@balikesir.edu.tr](mailto:karakaya@balikesir.edu.tr)
