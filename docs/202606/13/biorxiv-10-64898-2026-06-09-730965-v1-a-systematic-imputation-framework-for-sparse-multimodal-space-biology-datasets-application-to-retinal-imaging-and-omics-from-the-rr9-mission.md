---
title: "A systematic imputation framework for sparse, multimodal space biology datasets: application to retinal imaging and omics from the RR9 mission"
title_zh: 一种针对稀疏、多模态空间生物学数据集的系统化插补框架：应用于RR9任务的视网膜成像和组学数据
authors: "Nagesh, V., Sanders, L., Costes, S. V., Avci, P., Sigit, A., Agarwal, A., Haghighi, A., Batool, A., Karouia, F., Chander, A. M., Schmidt, C. M., Gong, J."
date: 2026-06-11
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.09.730965v1.full.pdf"
tags: ["query:multi-modal"]
score: 7.0
evidence: 系统性多模态缺失数据插补框架
tldr: 空间生物学实验样本稀少、数据稀疏且多模态，缺失数据严重阻碍了构建人体对航天响应的可靠模型。本研究提出一个四阶段系统插补框架，通过诊断缺失原因、选择和优化插补策略、评估生物学信号保留度来应对此问题。以NASA RR9任务的视网膜成像与组学数据为例，发现插补能显著增强预测模型性能，但可能掩盖细微的生物学模式，形成关键权衡。该框架为稀疏多模态空间生物数据集提供了实用指导，是迈向数字孪生开发的重要基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 空间生物数据常缺失，阻碍可靠计算模型构建与数字孪生开发。
method: 提出四阶段插补框架：诊断缺失机制、选择优化策略、评估信号保留与下游影响。
result: 插补提升预测模型性能，但可能掩盖细微生物学模式，需权衡。
conclusion: 框架量化了插补权衡，为分析稀疏多模态空间生物数据提供实用指南。
---

## 摘要
空间生物学实验成本高昂、后勤复杂且样本量固有有限，导致数据集经常不完整且高度异质性。数据缺失是构建人体对太空飞行反应可靠计算模型的基本障碍。本研究引入了一个通过插补解决缺失数据的系统化框架。我们开发了一个经过验证的四阶段插补框架，专门设计用于保留数字孪生开发所需的生物信号，同时量化下游分析中的权衡。以NASA RR9任务的视网膜成像和组学数据作为案例研究，我们展示了如何诊断数据缺失的原因、选择和优化合适的插补策略，并严格评估插补后的数据是否仍具有生物学意义。本研究的核心发现是：虽然插补显著提高了预测模型的性能，但同时可能掩盖微妙的生物模式——这是研究人员在应用这些方法之前必须理解的关键权衡。该框架为在空间生物学中处理稀疏、多模态数据集的空间生物学家和数据科学家提供了实用、可操作的指导，并代表了朝着在极端环境中建立更完整、可靠的人类生理数据驱动模型迈出的基础性一步。

## Abstract
Space biology experiments are expensive, logistically complex, and inherently limited in sample size, resulting in datasets that are frequently incomplete and highly heterogeneous (2). Missing data is a fundamental barrier to building reliable computational models of how the human body responds to spaceflight. This work introduces a systematic framework for addressing missing data through imputation. We developed a validated four-stage framework for imputation specifically designed to preserve biological signal needed for digital twin development, while quantifying trade-offs in downstream analyses. Using retinal imaging and omics data from the NASA RR9 mission as a case study (9), we demonstrate how to diagnose why data is missing(10), select and optimize appropriate imputation strategies (5,10), and rigorously evaluate whether imputed data remains biologically meaningful. A key finding of this work is that while imputation substantially improves the performance of predictive models, it can simultaneously obscure subtle biological patterns; a critical trade-off that researchers must understand before applying these methods (11). This framework provides practical, actionable guidance for space biologists and data scientists working with sparse, multimodal datasets in space biology, and represents a foundational step toward more complete and reliable data-driven models of human physiology in extreme environments.