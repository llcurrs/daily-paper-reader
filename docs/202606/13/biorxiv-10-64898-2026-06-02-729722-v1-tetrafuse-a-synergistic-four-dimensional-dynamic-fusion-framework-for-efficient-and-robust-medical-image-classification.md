---
title: "TetraFuse: A Synergistic Four-Dimensional Dynamic Fusion Framework for Efficient and Robust Medical Image Classification"
title_zh: "TetraFuse: 一种协同四维动态融合框架，用于高效稳健的医学图像分类"
authors: "Gao, Y., Li, J., Xu, J., Li, Q., Li, Z., Shi, Y., ZHao, G., Wu, X., Zhang, Y."
date: 2026-06-06
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.02.729722v1.full.pdf"
tags: ["query:multi-modal"]
score: 6.0
evidence: 四域动态融合框架
tldr: 医学图像分类中，现有轻量架构因分组卷积导致跨通道信息隔离，难以兼顾精度与效率。TetraFuse从空间、通道、统计和频率四个领域融合特征，提出跨通道动态聚合(CCDA)重构全局通道拓扑，并设计局部方差引导增强(LVGE)和边界注入(HFBI)分别抑制噪声与强化轮廓。在三个数据集上超越SOTA，Tiny版本仅0.345G FLOPs即达高精度。该框架以低计算开销实现强表示能力，适合资源受限的临床环境。
source: biorxiv
selection_source: fresh_fetch
motivation: 轻量架构的分组卷积造成跨通道信息隔离，降低表示能力，且现有方法难以平衡诊断精度与计算效率。
method: 提出TetraFuse四维融合框架：CCDA重建通道拓扑，LVGE滤除浅层噪声，HFBI注入深层边界。
result: 在COVID-19、ISIC 2018、Kvasir数据集上超越SOTA；Tiny模型FLOPs仅0.345G，Kvasir准确率0.926，AUC 0.994。
conclusion: TetraFuse以极低计算需求实现高表示能力，为大规模医学图像分析提供可扩展方案。
---

## 摘要
医学病理图像的准确稳健分类对于计算机辅助诊断至关重要。然而，深度学习模型在高通量临床筛查中的部署面临一个基本挑战：诊断准确性与计算效率之间的权衡。当前的轻量级架构通过分组卷积降低参数复杂度，但往往导致跨通道信息隔离和表示能力下降。在本文中，我们提出TetraFuse，一种新颖的框架，系统性地整合了来自四个互补域的特征：空间、通道、统计和频率。TetraFuse引入了一种新的跨通道动态聚合（CCDA）范式，以可忽略的计算开销重建全局通道拓扑，解决了组间隔离问题。为了平衡感知保真度和效率，我们设计了一种阶段感知的局部增强机制：采用局部方差引导增强器（LVGE）滤除浅层背景噪声，而高频边界注入（HFBI）则强化深层病理轮廓，防止空间过度平滑。在COVID-19、ISIC 2018和Kvasir数据集上的实验结果证实，TetraFuse优于最先进（SOTA）方法。值得注意的是，与ResNet50相比，TetraFuse-Tiny的FLOPs大幅降低了91.53%；在Kvasir数据集上，它仅以0.345G FLOPs实现了0.926的准确率和0.994的AUC。通过结合高表示能力和极低计算需求，TetraFuse为大规模医学图像分析提供了可扩展的解决方案，尤其适用于资源受限的临床环境。

## Abstract
Accurate and robust classification of medical pathology images is pivotal for computer-aided diagnosis. However, the deployment of deep learning models in high-throughput clinical screening faces a fundamental challenge: the trade-off between diagnostic accuracy and computational efficiency. Current lightweight architectures, while reducing parameter complexity through grouped convolutions, often lead to cross-channel information isolation and diminished representational capacity. In this paper, we propose TetraFuse, a novel framework that systematically integrates features from four complementary domains: space, channel, statistics, and frequency. TetraFuse introduces a novel Cross-Channel Dynamic Aggregation (CCDA) paradigm that reconstructs global channel topology with negligible computational overhead, resolving the inter-group isolation issue. To balance perceptual fidelity and efficiency, we design a stage-aware local enhancement mechanism: Local Variance-Guided Enhancer (LVGE) is employed to filter out shallow-stage background noise, while High-Frequency Boundary Injection (HFBI) reinforces deep-stage pathological contours, preventing spatial over-smoothing. Experimental results on the COVID-19, ISIC 2018, and Kvasir datasets confirm that TetraFuse outperforms state-of-the-art (SOTA) methods. Notably, TetraFuse-Tiny achieves a transformative 91.53% reduction in FLOPs compared to ResNet50; on the Kvasir dataset, it achieved an accuracy of 0.926 and an AUC of 0.994 with only 0.345G FLOPs. By combining high representational power with minimal computational demand, TetraFuse offers a scalable solution for large-scale medical image analysis, especially in resource-constrained clinical environments.