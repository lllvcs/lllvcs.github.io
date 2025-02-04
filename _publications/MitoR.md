---
title: "MitoR: Predicting T-cell Mitochondria Hijacking from Tumor Single-cell RNA Sequencing Data"
collection: publications
category: manuscripts
permalink: /publication/MitoR
date: 2025-01-24
venue: 'Under Review'
paperurl: 'https://github.com/compbioclub/MitoR'
citation: ''
---

+ Authors: Anna Jiang<sup>#</sup>, <b>Chengshang Lyu</b><sup>#</sup>, Yue Zhao<sup>*</sup>.

+ Abstract: T cells play a crucial role in the immune system by identifying and eliminating tumor cells. Malignant cancer cells can hijack mitochondria (MT) from nearby T cells, affecting their metabolism and weakening their immune functions. This phenomenon, observed through co-culture systems and fluorescent labeling, has been further explored with the development of the MERCI algorithm, which predicts T-cell MT hijacking in cancer cells using single-cell RNA (scRNA) sequencing data. However, MERCI is limited by its reliance on a linear model and its inability to handle data sparsity. To address these challenges, we introduce MitoR, a computational algorithm using a Poisson-Gamma mixture model to predict T-cell MT hijacking from tumor scRNA data. In performance comparisons, MitoR demonstrated improved performance compared to MERCI’s on real-world scRNA data scRNA-bench1 (Top AUROC: 0.761, Top Accuracy: 0.769) and scRNA-bench2 (Top AUROC: 0.730, Top Accuracy: 0.733). Additionally, MitoR showed an average 4.14% increase in AUROC and an average 3.86% increase in accuracy over MERCI in all rank strategies and simulated datasets. In conclusion, using MitoR to analyze scRNA data can provide new insights into tumor immune evasion by accurately predicting T-cell MT hijacking with greater AUROC and accuracy than existing methods.
