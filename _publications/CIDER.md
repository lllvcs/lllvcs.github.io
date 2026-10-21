---
title: "CIDER: Counterfactual-Invariant Diffusion-based GNN ExplaineR for Causal Subgraph Inference"
collection: publications
category: manuscripts
permalink: /publication/CIDER
date: 2026-10-20
venue: 'The Innovation'
---

+ Authors: Qibin ZHANG<sup>#</sup>, <b>Chengshang LYU</b>, Lingxi CHEN, Pei CHEN, Rui LIU<sup>*</sup>, Luonan CHEN<sup>*</sup>.

+ DOI: [10.1016/j.xinn.2026.101607](https://doi.org/10.1016/j.xinn.2026.101607)

![](/images/publications/CIDER.png)

+ Abstract: Inferring causal edges or subgraphs corresponding to a specific biological phenotype or label based solely on measured data is an important yet challenging task, distinct from inferring causal nodes/genes. The lack of transparency and explainability of conventional Graph Neural Network (GNN) Explainers hinders understanding of their results and underlying mechanisms. To address this issue, we propose a novel method of causal edge/subgraph inference, called CIDER: Counterfactual-Invariant Diffusion-based GNN ExplaineR, by implementing both counterfactual and diffusion implementations. In other words, it is a model- and task-agnostic framework for generating causal explanations based on a counterfactual-invariant and diffusion process, which provides not only causal subgraphs from counterfactual implementation, but also reliable causal edges due to a diffusion process. Specifically, CIDER is first formulated as an inference task that generatively models two distributions: one for the causal subgraph and the other for the spurious subgraph. To enhance reliability, we further model the CIDER framework as a diffusion process. Thus, using the causal subgraph distribution, we can explicitly quantify the contribution of each subgraph to a phenotype/label in a counterfactual manner, which represents the causal strength of each subgraph. We evaluate CIDER on both synthetic and real-world datasets, demonstrating its superiority over state-of-the-art methods. Further, CIDER shows its ability to elucidate causal genes and the cell-type network, thereby significantly facilitating the identification of underlying biological mechanisms at the molecular level.

+ The source code is available at [https://github.com/qibin9807/CIDER](https://github.com/qibin9807/CIDER).