

## Overview

WINDMI is a low-dimensional circuit model of the magnetosphere-ionosphere system (Horton & Doxas 1996, 1998; Spencer et al. 2006). This repository implements WINDMI in three configurations of increasing complexity and evaluates substorm onset detection performance against a merged reference catalog of 8,674 isolated substorm onsets spanning 1998–2004.

---

### Notebooks

**`WINDMI_paper_1.ipynb`** — Case Study (January 9–13, 2000)  
Runs WINDMI in all three configurations for a four-day interval and produces Figures 1 and 2 of the paper. Covers ACE data loading, propagation delay computation, coupling voltage calculation, and onset detection.

**`WINDMI_paper_2.ipynb`** — Multi-Year Analysis (1998–2004)  
Runs WINDMI over the full seven-year interval and evaluates detection performance against the merged substorm catalog.

---

## Model Configurations

| Configuration | L, C, Σ | Critical current *I_c* |
|---|---|---|
| Case 1 | Constant | Daily 70th percentile |
| Case 2 | Constant | Rolling 3-hour 70th percentile |
| Case 3 | Time-varying | Rolling 3-hour 70th percentile |

---

## Data Requirements

The following data are required to run the notebooks:

- **ACE Level-2** solar-wind data (1-min, 1998–2004) — [NASA CDAWeb](https://cdaweb.gsfc.nasa.gov/)
- **SuperMAG SML index** — [SuperMAG](https://supermag.jhuapl.edu/)
- **Substorm onset lists** — Forsyth et al. (2015), Frey et al. (2004), Liou (2010), Newell & Gjerloev (2011), Ohtani & Gjerloev (2020)

Update `ACE_dir` and all other hardcoded paths in the notebooks before running.

---

## Dependencies

```
numpy
pandas
scipy
matplotlib
tqdm
```
---

## License

MIT License
