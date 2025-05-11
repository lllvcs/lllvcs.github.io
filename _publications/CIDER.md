---
title: "CIDER: Counterfactual-Invariant Diffusion-based GNN Explainer for Causal Subgraph Inference"
collection: publications
category: manuscripts
permalink: /publication/CIDER
date: 2024-07-28
venue: 'arXiv'
---

+ Authors: Qibin Zhang<sup>#</sup>, <b>Chengshang LYU</b>, Lingxi CHEN, Qiqi Jin, Luonan Chen<sup>*</sup>.

+ DOI: [10.48550/arXiv.2407.19376](https://doi.org/10.48550/arXiv.2407.19376)

![](/images/publications/cider.jpg)

+ Abstract: Inferring causal links or subgraphs corresponding to a specific phenotype or label based solely on measured data is an important yet challenging task, which is also different from inferring causal nodes. While Graph Neural Network (GNN) Explainers have shown potential in subgraph identification, existing methods with GNN often offer associative rather than causal insights. This lack of transparency and explainability hinders our understanding of their results and also underlying mechanisms. To address this issue, we propose a novel method of causal link/subgraph inference, called CIDER: Counterfactual-Invariant Diffusion-based GNN ExplaineR, by implementing both counterfactual and diffusion implementations. In other words, it is a model-agnostic and task-agnostic framework for generating causal explanations based on a counterfactual-invariant and diffusion process, which provides not only causal subgraphs due to counterfactual implementation but reliable causal links due to the diffusion process. Specifically, CIDER is first formulated as an inference task that generatively provides the two distributions of one causal subgraph and another spurious subgraph. Then, to enhance the reliability, we further model the CIDER framework as a diffusion process. Thus, using the causal subgraph distribution, we can explicitly quantify the contribution of each subgraph to a phenotype/label in a counterfactual manner, representing each subgraph's causal strength. From a causality perspective, CIDER is an interventional causal method, different from traditional association studies or observational causal approaches, and can also reduce the effects of unobserved confounders. We evaluate CIDER on both synthetic and real-world datasets, which all demonstrate the superiority of CIDER over state-of-the-art methods.
