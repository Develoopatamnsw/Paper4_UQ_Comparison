# Paper4_UQ_Comparison

Code, predictions, and calibration data accompanying the manuscript:

**"Calibrated Uncertainty Quantification for Lithium-Ion Battery Knee-Point Prediction: A Systematic Benchmark with Mandatory Conformal Post-Processing and Cross-Chemistry Validation"**

Tran Thanh Trang, Tran Nhut Tam — submitted to *Reliability Engineering & System Safety* (RESS).

---

## Overview

This repository contains the full reproducibility package for a fourteen-method uncertainty-quantification (UQ) benchmark for early lithium-ion battery knee-point (pre-RUL) prediction, including:

- Training scripts for all UQ methods (deep ensembles, Bayesian LSTM, Gaussian Process, NGBoost, SNGP, Laplace, CQR-PINN-Knee, and the PINN-Knee variants).
- Per-cell prediction files (`.npz`) for every method, budget, and fold.
- Calibration residuals and computed metrics (CSV).
- Scripts to regenerate all figures and tables.

## Datasets

- **Severson LFP** (110 cells) — publicly available at https://data.matr.io/1/
- **Tongji NCM** (19 cells) — Zhu et al., *Nat. Commun.* 13 (2022) 2261.

The datasets themselves are not redistributed here; please obtain them from the original sources above. A cached feature file is provided for fast end-to-end reproduction where licensing permits.

## Repository structure

```
Scripts/        Training + analysis scripts (one per UQ method, plus figure/table generation)
Predictions/    Per-cell prediction .npz files (per method / budget / fold)
Metrics/        Aggregated metrics, per-fold tables, calibration data (CSV)
Figures/        Generated manuscript and supplementary figures
README.md       This file
LICENSE         MIT License
```

## Reproducibility

- Random seeds are documented per method.
- Cross-validation uses a fixed seed so the same cells are assigned to identical folds across all methods.
- A cached copy of the Severson features is provided so the fastest pipeline can be re-run on CPU; the full grid runs on a single GPU.

See Section 4.5 (Reproducibility) and the Supplementary Material of the manuscript for full details.

## Citation

If you use this code or data, please cite the manuscript (citation to be updated upon publication).

## License

Released under the MIT License — see [LICENSE](LICENSE).
