---
title: "Learning Shift-Invariant Graph Representations for Cox Survival on Multi-Modal Cancer Data"
collection: publications
category: conferences
permalink: /publication/InvGraphCox
date: 2026-08-24
venue: '2nd International Symposium on Computational Biology with AI'
---

+ Authors: Ka Ho NG<sup>#</sup>, <b>Chengshang LYU<sup>#</sup></b>, Anna JIANG, Yinhu LI, Lingxi CHEN<sup>*</sup>.

+ DOI: [10.64898/2025.11.30.691365](https://doi.org/10.64898/2025.11.30.691365)

+ Abstract: The clinical utility of survival prediction models is often limited by their inability to generalize across multi-center cohorts due to distribution shifts. Conventional solutions, such as independence-driven reweighting, fail to account for the latent topological relationships between patients, thereby missing critical structural information. We introduce InvGraphCox, a deep learning framework designed to overcome these limitations by enforcing distributional shift-robust via graph-based learning. Unlike standard approaches, InvGraphCox models the patient population as a k-nearest-neighbor graph, utilizing a Variational Graph Autoencoder (VGAE) to capture local manifold structures. This is coupled with a cohort-wise alignment mechanism that disentangles site-specific bias from true prognostic signals. We validate the framework on diverse tasks, including stable biomarker identification on curated gene sets, representation learning on high-dimensional transcriptomics (Ovarian and Breast Cancer), and risk profiling using mixed-type clinical data. InvGraphCox achieves superior discrimination and calibration compared to state-of-the-art baselines, demonstrating that incorporating population topology is essential for robust survival analysis in heterogeneous environments.

+ Preprint: [BioRxiv](https://doi.org/10.64898/2025.11.30.691365)