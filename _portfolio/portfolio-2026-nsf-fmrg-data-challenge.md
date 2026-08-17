---
title: "NSF Future Manufacturing Data Challenge 2026 (Top-5 Finalist) - Physics-Anchored Probabilistic Prediction of Local Laser-Track Geometry in DED"
excerpt: "Team RAMP's finalist entry: a physics-anchored, calibrated probabilistic pipeline that predicts local laser-track geometry (width, centreline, boundaries, contour) in directed energy deposition from in-situ melt-pool thermal video, SEM, and process metadata — evaluated on a held-out track printed below every training power"
advisor: ""
video: "https://www.youtube.com/watch?v=-i8yLJjuH38"
video_show: false
video_thumbnail: ""
slides: ""
slide_show: false
slide_thumbnail: ""
poster: "/images/2026_nsf_fmrg_track21.png"
publication: ""
github: "https://github.com/abhishekhanchate/nsf-fmrg-data-challenge"
project_link: "https://sites.google.com/tamu.edu/nsf-future-data-challenge/"
scholarurl: ""
selected: true
collection: portfolio
date: 2026-07-31
keyword: "Artificial Intelligence, Advanced Manufacturing, Uncertainty Quantification"
---

Team **RAMP** (H. Sinan Bank, Colorado State University; N. Bircan Bugdayci, Michigan State University) was selected as one of the **top-five finalists** in the [NSF Future Manufacturing Data Challenge 2026](https://sites.google.com/tamu.edu/nsf-future-data-challenge/) (NSF FMRG-2328395), organized by Texas A&M University. Although technical issues during the live finalist presentation (July 31, 2026) prevented the judges from evaluating it, the full presentation is available on [YouTube](https://www.youtube.com/watch?v=-i8yLJjuH38).

## The Challenge

The organizers released a [multimodal directed energy deposition (DED) dataset](https://arxiv.org/abs/2607.07965) of single laser tracks on stainless steel 316L: in-situ melt-pool thermal image sequences (Stratonics ThermaViz), post-process SEM of the substrate (Zeiss EVO MA10), and white-light profilometry height maps (Bruker ContourGT-K), for bead-on-plate scans at 300, 350, and 400 W. The task was to predict the **local** track geometry as a **calibrated probability distribution** — not a single global width statistic — for a held-out track printed at **200 W, below every training condition**, i.e., a small-*N* downward-extrapolation problem.

## Our Approach

<figure style="text-align: center;">
  <img src="/images/2026_nsf_fmrg_pipeline.png" alt="RAMP pipeline: data layer, alignment, target/feature extraction, probabilistic models, evaluation harness, and once-only Track-21 evaluation" style="max-width: 100%; height: auto;">
  <figcaption style="margin-top: 0.5em;"><em>End-to-end pipeline with leakage guardrails and a once-only, never-tuned-on final evaluation on the held-out 200 W track.</em></figcaption>
</figure>

- **Common physical coordinate.** All modalities are registered through a laser-stop-anchored frame-to-position map over a shared 20–100 mm window.
- **Missingness-aware label extraction.** Reference geometry is extracted from profilometry with 37–56% missing entries, using the *measurability* of the surface (rather than height alone) to localize the track and its two edges.
- **Robust thermal features.** Percentile-of-peak and intensity-gradient segmentation with scale-invariant descriptors, so features do not depend on uncalibrated radiance.
- **Leakage-safe SEM branch.** A track-masked frozen encoder supplies substrate context without leaking the label region.
- **Physics-anchored tiered model portfolio.** A heteroscedastic Gaussian process with an Eagar–Tsai-motivated power-law mean *w̄(P) = k (P − P₀)₊^γ* and a distributional gradient-boosting cross-check; a simulation-pretrained convolutional conditional neural process is promoted only if it beats them under identical, pre-registered evaluation gates. The parametric law sets the width *level*; the measured melt-pool extent sets the along-track *shape* — both label-free inputs.
- **Honest calibration under extrapolation.** Conformalized quantile regression with an explicit three-tier coverage-claim hierarchy (guaranteed / diagnostic / indicative), verified by a leave-one-power-out audit.

## Outcome and Findings

- Every deep alternative failed its pre-registered promotion gate (the neural process on pretraining-seed stability, the mixture ensemble on downward extrapolation), and substrate SEM contributed nothing across four instrument families — so the shipped model is the physics-anchored Gaussian process (development CRPS 64.7 µm; leave-one-power-out coverage 1.00 at both nominal levels).
- On the audited held-out 200 W track the model reproduces the along-track fluctuation in amplitude but not in phase, and an exact error decomposition attributes most of the boundary error to *centreline placement* rather than width.
- Central finding: under small-*N* downward extrapolation, **calibration and physical admissibility — not architecture — were the binding constraints**, and the residual local fluctuation is not recoverable from any released input we tested.

## Materials

- Presentation video (Top-5 Finalists, Team RAMP): [YouTube](https://www.youtube.com/watch?v=-i8yLJjuH38)
- Challenge website: [NSF Future Manufacturing Data Challenge](https://sites.google.com/tamu.edu/nsf-future-data-challenge/)
- Organizers' dataset paper: [arXiv:2607.07965](https://arxiv.org/abs/2607.07965) · Organizers' repository: [nsf-fmrg-data-challenge](https://github.com/abhishekhanchate/nsf-fmrg-data-challenge)
- Our report and code will be shared as a submodule of the organizers' repository once the detailed repository is released; a preprint of the full write-up is in preparation.

## Acknowledgments

Thanks to the organizers — Himanshu Balhara, Abhishek Hanchate, Bimal Nepal, Satish Bukkapatnam, Drew Casey, Woohyun Cho, and Shashank Galla — for preparing the competition and sharing the dataset, and to the CSU Walter Scott, Jr. College of Engineering for access to the SAIDIE cluster, used alongside our [GPU Workstations](https://github.com/bankh/GPU_Compute).
