# Paper4_UQ_Comparison

Code, predictions, and calibration data accompanying the manuscript:

"Calibrated Uncertainty Quantification for Lithium-Ion Battery Knee-Point Prediction: A Systematic Benchmark with Mandatory Conformal Post-Processing and Cross-Chemistry Validation"

Tran Thanh Trang, Tran Nhut Tam — submitted to Reliability Engineering & System Safety (RESS).

---

## Overview

This repository contains the full reproducibility package for a fourteen-method uncertainty-quantification (UQ) benchmark for early lithium-ion battery knee-point (pre-RUL) prediction:

- Training scripts for all UQ methods (deep ensembles, Bayesian LSTM, Gaussian Process, NGBoost, SNGP, Laplace, CQR-PINN-Knee, and the PINN-Knee variants).
- Per-cell prediction files (.npz) for every method, budget, and fold.
- Calibration residuals and computed metrics (CSV).
- Scripts to regenerate all figures and tables.

## Datasets

- Severson LFP (110 cells) — publicly available at https://data.matr.io/1/
- Tongji NCM (19 cells) — Zhu et al., Nat. Commun. 13 (2022) 2261.

The datasets themselves are not redistributed here; please obtain them from the original sources above.

## Repository structure

- Scripts/ — training and analysis scripts
- Predictions/ — per-cell prediction .npz files
- Metrics/ — aggregated metrics, per-fold tables, calibration data (CSV)
- Figures/ — generated manuscript and supplementary figures

## Reproducibility

Random seeds are documented per method. Cross-validation uses a fixed seed so the same cells are assigned to identical folds across all methods. See Section 4.5 and the Supplementary Material of the manuscript for full details.

## License

Released under the MIT License — see LICENSE.
