---
title: aNy-way ICA and its application to estimate cortico-thalamo-cerebellar functional links in schizophrenia
title_zh: 任意阶ICA及其在精神分裂症中估计皮质-丘脑-小脑功能连接的应用
authors: "Duan, K., Silva, R. F., Rahaman, M. A., Fu, Z., Liu, J., Kochunov, P., van Erp, T. G. M., Shultz, S., Calhoun, V. D."
date: 2026-06-25
pdf: "https://www.biorxiv.org/content/10.1101/2025.06.02.657541v2.full.pdf"
tags: ["query:multi-modal"]
score: 6.0
evidence: 基于独立成分分析的多模态数据融合方法
tldr: 多模态数据融合面临不同尺度和模型阶数不一致的挑战。本文提出aNy-way ICA方法，通过高斯独立向量分析优化跨模态加载相关性，同时保持各模态内独立性，允许各模态不同模型阶数。模拟显示该方法在噪声下准确性更高。应用于精神分裂症4D fMRI数据，识别出皮质-丘脑-小脑环路，其异常连接可区分患者与对照并与认知缺陷相关，跨数据集可重复。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有融合方法要求相同模型阶数或正交约束，难以处理不同尺度多模态数据。
method: aNy-way ICA结合IVA-G优化跨模态加载相关性与各模态ICA独立性，允许不同模型阶数。
result: 模拟中优于其他方法；真实数据发现高阶丘脑核、视觉皮质、默认网络和小脑后叶的功能连接在精神分裂症中异常。
conclusion: 该环路可能构成精神分裂症“认知共济失调”的神经基础，跨数据集稳定可重复。
---

## 摘要
国际和国家级生物库收集的多模态数据具有不同的尺度和模型阶数，为疾病机制提供了独特且互补的见解。我们提出了一种新颖、灵活且高效的数据融合方法——任意阶独立成分分析（aNy-way ICA）。aNy-way ICA通过高斯独立向量分析（IVA-G）优化链接成分的整个载荷相关结构，同时通过独立的ICA优化独立性，从而融合N维多模态或多域数据。该方法允许不同模态/域具有不同的模型阶数，并能在任意数量的模态或域中检测多个链接源，无需对源施加正交性约束。模拟结果表明，与其他方法相比，aNy-way ICA能够更准确地识别设计源和载荷以及真实的协方差模式，尤其在噪声条件下。将aNy-way ICA应用于融合精神分裂症的4维多域fMRI数据，我们识别出一个皮质-丘脑-小脑回路，突显了高阶丘脑核、视觉皮层、默认模式网络和小脑后叶之间的功能连接。这些功能连接在两个独立数据集中得到验证。高阶丘脑核、视觉皮层和默认模式网络之间的连接能够区分精神分裂症患者与对照组，并且这种异常连接与发现和验证数据集中的多种认知缺陷相关，表明所识别的皮质-丘脑-小脑回路可能是精神分裂症“认知共济失调”的基础。

## Abstract
Multimodal data collected by international and national biobanking efforts have distinct scales and model orders and provide unique and complementary insights into disease mechanisms. We propose a novel, flexible and efficient data fusion approach, aNy-way independent component analysis (aNy-way ICA). aNy-way ICA fuses N-way multimodal or multidomain data by optimizing the entire loading correlation structure of linked components via Gaussian independent vector analysis (IVA-G) and simultaneously optimizing independence via separate ICAs. This allows for distinct model orders for different modalities/domains and multiple linked sources detection across any number of modalities or domains without requiring orthogonality constraints on sources. Simulation results demonstrate that aNy-way ICA identifies the designed sources and loadings, as well as the true covariance patterns, with improved accuracy compared to other approaches, especially under noisy conditions. Applying aNy-way ICA to fuse 4D multi-domain fMRI data in schizophrenia, we identified a cortico-thalamo-cerebellar circuit, highlighting the functional linkages among higher order thalamic nuclei, the visual cortex, default mode network, and the posterior lobe of cerebellum. Their function links were replicated in two independent datasets. The connection among higher order thalamic nuclei, the visual cortex, and default mode network discriminates schizophrenia from controls and this aberrant connection is related to multiple cognitive deficits in both discovery and replication datasets, indicating the identified cortico-thalamo-cerebellar circuit may underlie "cognitive dysmetria" in schizophrenia.