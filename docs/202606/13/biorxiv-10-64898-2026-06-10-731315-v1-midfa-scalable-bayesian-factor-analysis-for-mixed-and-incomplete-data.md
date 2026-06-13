---
title: "MIDFA: Scalable Bayesian Factor Analysis for Mixed and Incomplete Data"
title_zh: "MIDFA: 面向混合和不完全数据的可扩展贝叶斯因子分析"
authors: "Hutchings, G., Samartsidis, P., Donnay, C., Gaetano, L., Fisher, E., Nichols, T. E., Holmes, C., Häring, D. A., Ganjgahi, H."
date: 2026-06-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.10.731315v1.full.pdf"
tags: ["query:multi-modal"]
score: 6.0
evidence: 面向混合和不完整数据的贝叶斯因子分析
tldr: 大规模流行病学数据常包含混合类型、高维度和结构化缺失。本文提出MIDFA，一种可扩展贝叶斯因子分析框架，采用半参数高斯copula建模混合数据，利用连续spike-and-slab先验实现稀疏因子载荷，通过印度自助餐过程非参数学习潜维度，并开发EM算法处理缺失值。在模拟和实际多发性硬化数据上，方法能识别共享潜结构，用于MRI降维提取超越传统统计的特征。该工作为混合不完全数据提供了统一、可扩展的稀疏因子分析方案。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有因子分析难以同时应对混合数据类型、高维度和结构化缺失，需统一的稀疏可扩展框架。
method: 结合半参数高斯copula与连续spike-and-slab先验，通过印度自助餐过程学习维度，基于EM算法处理缺失数据。
result: 在多发性硬化数据上识别出临床与影像共享潜结构，并提取出超越全脑统计的MRI特征。
conclusion: MIDFA为混合不完全数据提供可扩展稀疏因子分析，适用于大规模生物医学研究。
---

## 摘要
概率潜变量模型是揭示高维数据集结构的强大工具，尤其在生物医学应用中。随着大规模流行病学研究（如英国生物库）的日益普及，带来了重要的建模挑战，包括混合数据类型、高维性和结构化缺失。现有方法解决了其中一些问题，但很少有提供一个统一且可扩展的框架来同时处理这些问题。在此，我们提出一个可扩展的贝叶斯因子分析框架，旨在应对这些挑战。我们的方法将半参数高斯copula模型与连续尖峰-平板先验相结合，以诱导稀疏且可解释的因子载荷。使用印度自助餐过程先验从数据中非参数地学习潜在维度的数量。对于模型拟合，我们开发了一个期望最大化算法，自然地处理缺失数据。我们通过全面的仿真研究验证了所提方法。此外，我们使用诺华-牛津多发性硬化症数据集以两种方式展示了所提模型。首先，我们识别出MS临床和神经影像变量之间共享的潜在维度，刻画疾病结构，同时展示了模型处理多种数据类型和结构化缺失的能力。其次，我们将模型用于结构MRI数据的降维，提取下游分析的特征，这些特征超越了传统的全脑汇总统计。在这些应用中，我们的方法识别出稀疏的潜在结构，并提供了超出传统方法所获得的见解。

## Abstract
Probabilistic latent variable models are a powerful tool for uncovering structure in high-dimensional datasets, particularly in biomedical applications. The increasing availability of large-scale epidemiological studies, such as the UK Biobank, poses important modelling challenges, including mixed data types, high dimensionality, and structured missingness. Existing approaches address some of these issues, but few provide a unified and scalable framework for handling them simultaneously. Here, we propose a scalable Bayesian factor analysis framework designed to address these challenges. Our method combines a semiparametric Gaussian copula model with a continuous spike-and-slab prior to induce sparse and interpretable factor loadings. The number of latent dimensions is learned nonparametrically from the data using an Indian buffet process prior. For model fitting, we develop an expectation-maximisation algorithm that naturally accommodates missing data. We validate the proposed method through comprehensive simulation studies. In addition, we showcase the proposed model using the Novartis-Oxford Multiple Sclerosis dataset in two ways. First, we identify latent dimensions shared across MS clinical and neuroimaging variables, characterising disease structure while demonstrating the model's ability to handle multiple data types and structured missingness. Second, we use the model for dimensionality reduction of structural MRI data, extracting features for downstream analysis that go beyond traditional whole-brain summary statistics. In those applications, our method identifies sparse latent structures and provides insights beyond those obtained from traditional approaches.