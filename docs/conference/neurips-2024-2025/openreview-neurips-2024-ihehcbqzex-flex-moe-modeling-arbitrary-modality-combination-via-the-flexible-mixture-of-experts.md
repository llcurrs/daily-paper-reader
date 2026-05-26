---
title: "Flex-MoE: Modeling Arbitrary Modality Combination via the Flexible Mixture-of-Experts"
title_zh: Flex-MoE：通过灵活的专家混合模型建模任意模态组合
authors: "Sukwon Yun, Inyoung Choi, Jie Peng, Yangfan Wu, Jingxuan Bao, Qiyiwen Zhang, Jiayi Xin, Qi Long, Tianlong Chen"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=ihEHCbqZEx"
tags: ["query:multi-modal"]
score: 7.0
evidence: 灵活的专家混合框架处理任意模态组合与缺失数据
tldr: 针对现有多模态框架难以处理任意缺失模态组合的问题，提出Flex-MoE，一种灵活的专家混合架构。该框架利用模态特定的专家网络和动态融合机制，能够适应推理时的任意输入模态子集。在多个多模态任务上验证了对缺失数据的鲁棒性，为真实场景中模态不完整的多模态学习提供了通用解决方案。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-ihehcbqzex/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1423, \"height\": 387, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ihehcbqzex/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 310, \"height\": 304, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ihehcbqzex/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1440, \"height\": 583, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ihehcbqzex/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 760, \"height\": 349, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ihehcbqzex/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 687, \"height\": 524, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ihehcbqzex/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 799, \"height\": 203, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-ihehcbqzex/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1453, \"height\": 359, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ihehcbqzex/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1453, \"height\": 307, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ihehcbqzex/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 565, \"height\": 312, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ihehcbqzex/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1448, \"height\": 493, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ihehcbqzex/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1441, \"height\": 634, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ihehcbqzex/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 586, \"height\": 401, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ihehcbqzex/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1451, \"height\": 354, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ihehcbqzex/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1314, \"height\": 272, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ihehcbqzex/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1312, \"height\": 279, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ihehcbqzex/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1453, \"height\": 357, \"label\": \"Table\"}]"
motivation: 实际多模态场景中模态任意缺失，现有方法常依赖特定组合或完整数据。
method: 设计模态特定的专家网络与动态融合策略，实现任意模态组合下的推理。
result: 在医学等多模态任务中，模态缺失时性能优于传统方法。
conclusion: 提供了一种灵活鲁棒的多模态学习框架。
---

## Abstract
Multimodal learning has gained increasing importance across various fields, offering the ability to integrate data from diverse sources such as images, text, and personalized records, which are frequently observed in medical domains. However, in scenarios where some modalities are missing, many existing frameworks struggle to accommodate arbitrary modality combinations, often relying heavily on a single modality or complete data. This oversight of potential modality combinations limits their applicability in real-world situations. To address this challenge, we propose Flex-MoE (Flexible Mixture-of-Experts), a new framework designed to flexibly incorporate arbitrary modality combinations while maintaining robustness to missing data. The core idea of Flex-MoE is to first address missing modalities using a new missing modality bank that integrates observed modality combinations with the corresponding missing ones. This is followed by a uniquely designed Sparse MoE framework. Specifically, Flex-MoE first trains experts using samples with all modalities to inject generalized knowledge through the generalized router ($\mathcal{G}$-Router). The $\mathcal{S}$-Router then specializes in handling fewer modality combinations by assigning the top-1 gate to the expert corresponding to the observed modality combination. We evaluate Flex-MoE on the ADNI dataset, which encompasses four modalities in the Alzheimer's Disease domain, as well as on the MIMIC-IV dataset. The results demonstrate the effectiveness of Flex-MoE, highlighting its ability to model arbitrary modality combinations in diverse missing modality scenarios. Code is available at: \url{https://github.com/UNITES-Lab/flex-moe}.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究动机**：多模态学习在医疗等领域至关重要，但真实场景下模态经常缺失。现有方法要么依赖单一模态，要么要求完整模态组合，无法灵活处理任意子集的模态输入。
- **核心问题**：如何设计一个模型，能够在任意模态组合（包括部分缺失）下都保持高性能，而无需为每种组合单独训练或仅依靠完整数据。
- **整体含义**：提出 **Flex-MoE**（Flexible Mixture-of-Experts），一个基于稀疏专家混合的框架，通过动态补全缺失模态和专家泛化‑专业化机制，实现对任意模态组合的鲁棒建模。

## 2. 论文提出的方法论

- **整体流程**：
  1. 按样本可用模态数量降序排序。
  2. 各模态通过独立的模态特定编码器（如 3D‑CNN 处理影像）。
  3. 缺失模态由 **缺失模态银行（Missing Modality Bank）** 提供可学习嵌入，该银行基于观测到的模态组合索引对应的缺失模态嵌入。
  4. 拼接所有模态嵌入后送入 Transformer，其中的前馈层替换为稀疏 MoE 层。
- **缺失模态银行**：
  - 维度为 \(\mathbb{R}^{(2^{|\mathcal{M}|}-1) \times |\mathcal{M}|}\)，其中 \(|\mathcal{M}|\) 为模态总数。
  - 对于样本 \(i\) 的模态 \(m\)，若缺失，则从银行中取 \(\mathbf{B}_{\mathcal{M}\setminus m, m}\)；否则用编码器输出。
- **专家泛化（\(\mathcal{G}\)-Router）**：
  - 先用**全模态样本**训练所有专家，路由采用标准稀疏 Top‑K 门控，并加入负载均衡损失，保证专家被公平激活，习得通用多模态知识。
- **专家专业化（\(\mathcal{S}\)-Router）**：
  - 利用**少模态样本**继续训练，人为设定 Top‑1 门控指向该样本对应模态组合的专属专家。
  - 引入交叉熵损失 \(\mathcal{L}_{ce}\)，让路由学习将特定组合的 Token 分配给指定专家，同时其余 Top‑(K‑1) 专家保持负载均衡。
  - 仅对非 Top‑1 专家计算负载和重要性平衡损失，以确保其他专家也能适度参与。
- **训练策略**：先 warm‑up 阶段使用排序样本，后随机打乱，结合课程学习思想。

## 3. 实验设计

- **数据集**：
  - **ADNI**：阿尔茨海默病数据，4 种模态（影像 I、基因 G、临床 C、生物样本 B），预测疾病阶段（3 分类）。
  - **MIMIC‑IV**：重症监护数据，3 种模态（实验室及生命体征 L、临床笔记 N、ICD‑9 编码 C），预测一年内死亡率（2 分类）。
- **对比方法**：
  - 单模态基线：3D CNN、VGG、ResNet‑18、基于基因的 ResNet‑34 等。
  - 多模态基线：专门针对 AD 的自动编码器融合模型 [59]、GRU 融合模型 [33]；通用多模态框架如 ShaSpec、mmFormer、TF、MulT、MAG、LIMoE、FuseMoE。
- **评估指标**：准确率（ACC）、宏平均 F1、AUC。每个实验重复 3 次报告均值和标准差。
- **数据划分**：训练 70%，验证和测试各 15%（测试/验证仅用全模态交集以保证公平比较）。

## 4. 资源与算力

- 文中声明所有实验使用 **NVIDIA A100 GPU** 完成。
- **未明确说明** GPU 数量、单次训练时长或总计算时数，但提供了超参数搜索范围（学习率、隐藏维度、专家数等），复现难度不大。

## 5. 实验数量与充分性

- **主实验**：在 ADNI 上评估 **11 种模态组合**（从 2 模态到 4 模态），在 MIMIC‑IV 上评估 **4 种组合**，与 10 余个基线对比，涵盖 ACC、F1、AUC 三种指标。
- **消融实验**：移除专家专业化、移除泛化+专业化、去掉缺失模态银行、改变排序方式（随机、升序），验证各组件贡献。
- **敏感性分析**：调整专家数量（16/32）、MoE 层数（1/2）、Top‑K（2/3/4），分析参数影响。
- **复杂度研究**：比较平均迭代时间、GFLOPs、参数量。
- **可解释性实验**：展示缺失模态银行的余弦相似度热图，以及专家激活比率，验证设计合理性。
- 实验设计**充分且公平**：考虑多种缺失场景，消融和敏感性实验覆盖关键超参，对比基线包含领域专用及通用方法，并使用统计均值/标准差。

## 6. 论文的主要结论与发现

- Flex‑MoE 在所有模态组合下均优于现有单模态和多模态基线，特别是在全模态场景下，相较最佳基线（MAG）和最新模型（FuseMoE），提升分别达 **7.6%** 和 **11.07%**。
- 缺失模态银行能捕获不同模态组合间的内在关联，相似组合的嵌入也更相近。
- 专家泛化与专业化设计使模型既保留通用知识，又习得组合特定的专家，路由激活图验证了这一点。
- 稀疏 MoE 设计在维持甚至提升性能的同时，相比部分基线具有更低的计算复杂度和参数量（如参数量仅为 FuseMoE 的约 11%）。

## 7. 优点

- **新颖的缺失处理**：缺失模态银行动态补全，避免对编码器的干扰，且捕获组合间关系。
- **创新的 MoE 设计**：将全模态样本用于泛化、少模态样本用于专业化，利用课程学习思想，有效融合全局与局部知识。
- **灵活且鲁棒**：无需预设固定模态集，适用于任意子集，理论扩展性好。
- **实验扎实**：两个真实医学数据集、多种缺失组合、全面消融与敏感性分析，结果一致。

## 8. 不足与局限

- **评估领域局限**：仅在医学数据集（ADNI、MIMIC‑IV）上验证，缺少通用视觉‑语言或多模态基准（如 MM‑IMDB、CMU‑MOSI）的测试，跨领域泛化性未证实。
- **数据质量依赖**：论文承认效果受限于高质量、全面的患者数据，在数据极其稀疏或噪声大的情况下可能退化。
- **临床部署顾虑**：未深入讨论与现有临床工作流的集成挑战，实际落地还需额外工程与验证。
- **超参敏感性**：专家数、Top‑K 等需根据数据集调整，缺少自动化选择策略，可能增加调参成本。
- **公平性方面未触及**：未分析模型在不同人口统计群组上的偏差风险。

（完）
