---
title: "Knowledge-driven annotation for gene interaction enrichment analysis"
collection: publications
category: manuscripts
permalink: /publication/GREA
date: 2025-04-20
venue: 'bioRxiv'
---

+ Authors: Xiaoyu LIU<sup>#</sup>, Anna JIANG<sup>#</sup>, <b>Chengshang LYU</b>, Lingxi CHEN<sup>*</sup>.

+ DOI: [10.1101/2025.04.15.649030](https://doi.org/10.1101/2025.04.15.649030)

![](/images/publications/grea.png)

+ Abstract: Gene Set Enrichment Analysis (GSEA) is a cornerstone for interpreting gene expression data, yet traditional approaches overlook gene interactions by focusing solely on individual genes, limiting their ability to detect subtle or complex pathway signals. To overcome this, we present GREA (Gene Interaction Enrichment Analysis), a novel framework that incorporates gene interaction data into enrichment analysis. GREA replaces the binary gene hit indicator with an interaction overlap ratio, capturing the degree of overlap between gene sets and gene interactions to enhance sensitivity and biological interpretability. It supports three enrichment metrics: Enrichment Score (ES), Enrichment Score Difference (ESD) from a Kolmogorov-Smirnov-based statistic, and Area Under the Curve (AUC) from a recovery curve. GREA evaluates statistical significance using both permutation testing and gamma distribution modeling. Benchmarking on transcriptomic datasets related to respiratory viral infections shows that GREA consistently outperforms existing tools such as blitzGSEA and GSEApy, identifying more relevant pathways with greater stability and reproducibility. By integrating gene interactions into pathway analysis, GREA offers a powerful and flexible tool for uncovering biologically meaningful insights in complex datasets. The source code is available at https://github.com/compbioclub/GREA.
