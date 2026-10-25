# Battery Cycling Quality Analytics

A DMAIC Six Sigma pipeline for battery cycling data — validated on NASA PCoE lithium-ion cycling, with methodology designed to transfer to long-duration iron-air storage quality control.

**Author:** Bhargava Sriram · BITS Pilani Hyderabad (ME, Aug 2027) · Six Sigma Green Belt
**Target role:** Quality Engineer I, battery manufacturing

---

## What this project does

Takes raw cell-cycling data from the [NASA PCoE Battery Prognostics Dataset](https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/) and runs it through a Quality Engineering pipeline:

1. **Parse** NASA's nested MATLAB `.mat` struct into a tidy long-format DataFrame (Parquet).
2. **Visualize** discharge voltage curves across cell life to show degradation emerging cycle by cycle.
3. **Compute** per-cycle discharge capacity two ways (NASA-reported vs. first-principles integration of current) and validate agreement under 1% — a mini Measurement System Analysis.
4. **Fit** linear and exponential degradation models per cell; pick the better fit by R² and predict cycle-to-end-of-life (RUL).

Downstream weeks will add SPC control charts, Cp/Cpk capability study, Weibull reliability analysis, DMAIC phase documentation, and a synthetic iron-air transfer chapter.

---

## Repo structure
