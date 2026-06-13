---
title: Generating Joint Transcriptomic and Morphological Responses to Drug Perturbations via Rectified Flow
title_zh: 通过整流流生成药物扰动的联合转录组和形态学响应
authors: "Verma, S., Wang, M., Wang, L., Kadadi, S. D., Sola, M., Kazemian, M., Grama, A., Lanman, N. A."
date: 2026-06-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.02.02.703189v3.full.pdf"
tags: ["query:multi-modal"]
score: 6.0
evidence: 联合预测转录组和形态学双模态
tldr: 现有方法孤立建模转录组和形态变化，忽略药物扰动下两者的协同关系。PertFlow基于整流流，从对照状态和药物元数据同时预测基因表达与生成细胞形态图像。在3细胞系40化合物上，转录组预测相关系数0.780，形态生成FID 24.06，病理专家评分7.11-7.89/10。模型成功恢复微管干扰、DNA损伤等已知机制，为联合分子-表型响应预测提供统一框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有方法孤立预测转录组或形态，缺乏对药物扰动下两者同步变化的建模能力。
method: 提出PertFlow，采用整流流以对照状态和药物元数据为条件，联合预测基因表达与生成细胞形态图像。
result: 在3细胞系40化合物上，转录组预测Pearson 0.780，形态生成FID 24.06，专家评分中位数7.11-7.89/10。
conclusion: PertFlow成功恢复已知药物机制，实现转录组与形态的联合预测，具有广泛适用性。
---

## 摘要
动机：预测细胞对药物扰动的响应需要捕捉转录组和形态学变化之间的复杂依赖关系。现有方法孤立地建模这些模态，忽略了药物治疗期间同时发生的关键分子-表型关系。目前没有方法能够从化学扰动中联合预测基因表达谱和细胞形态。结果：我们提出了PertFlow，一个统一的计算框架，该框架同时预测处理后的基因表达（批量RNA-seq）并从对照细胞状态生成细胞形态（Cell Painting图像），条件为药物元数据。在来自3个细胞系和40种化合物（17,242个样本）的配对RNA-seq和成像数据上评估，PertFlow在转录组预测上实现了0.780±0.264的Pearson相关系数，在形态生成上实现了24.06的FID。委员会认证的病理学家对生成图像的中位数相似度评分为7.11-7.89/10。该模型成功恢复了已知的药物机制，包括微管破坏、DNA损伤和MAPK通路抑制，基因富集分析确认了预期的生物学通路（EMT、p53、凋亡）的激活。可用性：代码和预训练模型将在https://github.com/wangmengbo/PertFlow上提供。

## Abstract
Motivation: Predicting cellular responses to drug perturbations requires capturing complex dependencies between transcriptomic and morphological changes. Existing approaches model these modalities in isolation, missing critical molecular-phenotypic relationships that occur simultaneously during drug treatment. No current method jointly predicts gene expression profiles and cellular morphology from chemical perturbations. Results: We introduce PertFlow, a unified computational frame-work that simultaneously predicts treatment gene expression (bulk RNA-seq) and generates cellular morphology (Cell Painting images) from control cellular states, conditioned on drug metadata. Evaluated on paired RNA-seq and imaging data from 3 cell lines and 40 compounds (17,242 samples), PertFlow achieves Pearson correlation of 0.780+-0.264 for transcriptomic prediction and FID of 24.06 for morphological generation. Board-certified pathologists rated generated images with median similarity scores of 7.11-7.89/10. The model successfully recovers known drug mechanisms including microtubule disruption, DNA damage, and MAPK pathway inhibition, with gene enrichment analysis confirming activation of expected biological pathways (EMT, p53, apoptosis). Availability: Code and pretrained models will be available at https://github.com/wangmengbo/PertFlow.