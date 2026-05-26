---
title: Toward Robust Incomplete Multimodal Sentiment Analysis via Hierarchical Representation Learning
title_zh: 面向鲁棒的不完整多模态情感分析的层次表示学习
authors: "Mingcheng Li, Dingkang Yang, Yang Liu, Shunli Wang, Jiawei Chen, Shuaibing Wang, Jinjie Wei, Yue Jiang, Qingyao Xu, Xiaolu Hou, Mingyang Sun, Ziyun Qian, Dongliang Kou, Lihua Zhang"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=XgwTH95kCl"
tags: ["query:multi-modal"]
score: 7.0
evidence: 通过层次表示学习处理不确定模态缺失的鲁棒情感分析
tldr: 针对多模态情感分析中模态不确定缺失问题，提出层次表示学习框架HRLF。通过细粒度表示分解模块充分提取模态内特征，并设计鲁棒融合策略。实验证明在多种缺失情况下性能稳定，为缺失模态下的多模态学习提供新思路。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgwth95kcl/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 721, \"height\": 468, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgwth95kcl/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1436, \"height\": 598, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgwth95kcl/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1431, \"height\": 260, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgwth95kcl/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 784, \"height\": 323, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgwth95kcl/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 630, \"height\": 433, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgwth95kcl/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1436, \"height\": 359, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-xgwth95kcl/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1457, \"height\": 841, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xgwth95kcl/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1458, \"height\": 1586, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xgwth95kcl/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1443, \"height\": 265, \"label\": \"Table\"}]"
motivation: 真实场景中多模态情感分析常面临模态缺失，导致性能下降。
method: 设计HRLF，包含细粒度表示分解和鲁棒融合模块。
result: 在不确定缺失模态设置下取得鲁棒的情感分析结果。
conclusion: HRLF为不完整多模态情感分析提供了有效解决方案。
---

## Abstract
Multimodal Sentiment Analysis (MSA) is an important research area that aims to understand and recognize human sentiment through multiple modalities. The complementary information provided by multimodal fusion promotes better sentiment analysis compared to utilizing only a single modality. Nevertheless, in real-world applications, many unavoidable factors may lead to situations of uncertain modality missing, thus hindering the effectiveness of multimodal modeling and degrading the model’s performance. To this end, we propose a Hierarchical Representation Learning Framework (HRLF) for the MSA task under uncertain missing modalities. Specifically, we propose a fine-grained representation factorization module that sufficiently extracts valuable sentiment information by factorizing modality into sentiment-relevant and modality-specific representations through crossmodal translation and sentiment semantic reconstruction. Moreover, a hierarchical mutual information maximization mechanism is introduced to incrementally maximize the mutual information between multi-scale representations to align and reconstruct the high-level semantics in the representations. Ultimately, we propose a hierarchical adversarial learning mechanism that further aligns and adapts the latent distribution of sentiment-relevant representations to produce robust joint multimodal representations. Comprehensive experiments on three datasets demonstrate that HRLF significantly improves MSA performance under uncertain modality missing cases.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- 多模态情感分析（MSA）利用语言、音频、视觉等多模态信息的互补性来理解人类情感，但在实际应用中常出现模态缺失（如设备故障、隐私限制、传感器噪声等）导致性能下降。
- 论文关注**不确定模态缺失**下的鲁棒多模态情感分析，涵盖两类缺失场景：
  - **模态内缺失**（intra-modality missingness）：部分帧级特征丢失。
  - **模态间缺失**（inter-modality missingness）：整条模态完全缺失。
- 现有方法存在两大不足：
  1. 对不完整模态的复杂交互带来信息冗余和累积误差，不能有效提取情感语义。
  2. 缺乏对表征语义和分布的精细对齐，导致重构不准、联合表征不鲁棒。
- 为此，提出**层次化表征学习框架（HRLF）**，旨在通过分解、语义对齐和分布对齐获得鲁棒的多模态联合表征。

### 2. 论文提出的方法论：核心思想、关键技术细节
HRLF 核心由三个模块组成：
- **细粒度表征分解模块（FRF）**：
  - 将每个模态的低层表征分解为**情感相关表征**‡（sentiment-relevant，跨模态共享、模态无关，鲁棒）和**模态特有表征**‡（modality-specific）。
  - 通过**模态内/间翻译**（intra- and inter-modality translation）学习解耦：将一种模态的情感相关表征与另一模态的模态特有表征结合，解码重建目标模态的低层表征，损失函数为翻译损失 $L_{\text{trans}}$。
  - 通过**情感语义重建**保证重建后的模态仍保有原有情感语义：约束重建后的情感相关表征与原表征一致，损失 $L_{\text{recon}}$。
  - FRF 总损失：$L_{\text{FRF}} = L_{\text{trans}} + L_{\text{recon}}$。

- **层次化互信息最大化机制（HMI）**：
  - 在教师-学生知识蒸馏框架下，教师网络用完整模态训练，学生网络处理缺失模态样本。
  - 提取教师和学生的多尺度联合表征（$E_t^i, E_s^i$），通过最大化它们之间的互信息实现**语义对齐**。
  - 使用 Jensen-Shannon 散度估计互信息下界，交叉最大化损失 $L_{\text{HMI}} = -\sum_{i=1}^3 MI(E_t^i, E_s^i)$。

- **层次化对抗学习机制（HAL）**：
  - 通过多尺度对抗训练逐步对齐教师和学生表征的**潜在分布**。
  - 学生网络生成表征试图欺骗判别器，判别器区分来源（教师/学生），目标函数 $L_{\text{HAL}} = \sum_{i=1}^3 \left[ \log(1 - D_e(E_s^i)) + \log D_e(E_t^i) \right]$。

- 此外，还有**模态随机缺失策略（MSM）**同时模拟两种缺失，KL 散度约束教师和学生 logits 的一致性，以及最终任务损失（分类用交叉熵，回归用 MSE）。
- 总损失：$L_{\text{total}} = L_{\text{task}} + L_{\text{FRF}} + L_{\text{HMI}} + L_{\text{HAL}} + L_{\text{KL}}$。

### 3. 实验设计：数据集/场景、benchmark、对比方法
- **数据集**：
  - MOSI（2,199 视频片段，情感分数 -3 ~ +3）
  - MOSEI（22,856 片段，情感分数 -3 ~ +3）
  - IEMOCAP（4,453 样本，四类情绪识别：高兴、悲伤、愤怒、中性）
- **评价指标**：MOSI/MOSEI 用 MAE（平均绝对误差）和 F1 分数（正/负分类）；IEMOCAP 用 F1 分数。
- **缺失场景**：
  - 模态内缺失：随机丢弃帧级特征，缺失率 p ∈ {0.0, 0.1, …, 1.0}。
  - 模态间缺失：6 种可能的模态组合测试（{l}, {a}, {v}, {l,a}, {l,v}, {a,v}）及平均表现。
- **对比方法**（SOTA）：
  - 完整模态方法：Self-MM, CubeMLP, DMD。
  - 缺失模态方法（联合学习）：MCTN, TransM, CorrKD。
  - 缺失模态方法（生成式）：SMIL, GCNet。
- 所有对比方法均被公平重实现并适配相同实验范式，结果取多次随机种子平均。

### 4. 资源与算力
- 文中明确说明：所有实验基于 PyTorch，使用 **4 块 NVIDIA Tesla V100 GPU** 训练。
- 未给出具体训练时长（epochs 给定了范围 20~50，batch size 16~128，但未说明单次训练耗时），整体算力需求对于该规模实验属于中等水平。

### 5. 实验数量与充分性
- **主要对比实验**：
  - 模态内缺失鲁棒性：在三个数据集上绘制不同缺失率下的性能曲线（F1/MAE）。
  - 模态间缺失鲁棒性：三数据集 × 6 种缺失条件 + 完整模态条件，给出平均与显著性检验。
- **消融实验**：
  - 分别移除 FRF、HMI、HAL 组件，在 MOSI 上展示模态内缺失（曲线）和模态间缺失（表格）的性能变化。
- **定性分析**：
  - 在 IEMOCAP 上可视化不同方法的表征分布（t-SNE 或类似方法），对比聚类效果。
- 实验设置覆盖三种主流基准、两类缺失场景、多种缺失率，与 8 种 SOTA 方法公平比较，并结合消融实验验证每个模块的有效性。总体实验设计**全面且充分**，比较**客观公平**。

### 6. 论文的主要结论与发现
- HRLF 在不确定模态缺失场景下显著提升情感分析性能，对模态内和模态间缺失均表现出最佳鲁棒性。
- 分解出情感相关表征能有效去除任务无关噪声，跨模态翻译和情感重建确保情感语义的精确捕获。
- 层次化互信息最大化和对抗学习分别实现语义与分布层面的精细对齐，使缺失模态下的学生网络能生成鲁棒联合表征。
- 语言模态在情感推断和缺失语义重建中占据主导地位，包含最丰富的情感语义。

### 7. 优点：方法或实验设计上的亮点
- 精细的**表征分解**设计，通过翻译和重建约束真正分离出情感核心信息，解决以往分解粗糙、监督不足的问题。
- 首次在知识蒸馏框架中引入**层次化互信息**与**层次化对抗**进行多层语义和分布的双重对齐，提升知识迁移质量。
- 同时考虑模态内和模态间缺失，贴近真实场景，且通过 MSM 策略统一模拟。
- 在多个基准、多种缺失模式下进行了**系统性评估**和**消融验证**，并包含统计显著性检验，结论可信。
- 与多种类别 SOTA 方法公平对比，覆盖完整模态方法和缺失模态方法。

### 8. 不足与局限
- **复杂缺失场景模拟有限**：仅覆盖随机缺失和整模态缺失，未考虑真实应用中更复杂的非随机、连续块缺失、异步缺失等情况，实际部署时可能性能下降。
- **泛化风险**：仅在三个特定情感数据集上验证，未在其他多模态任务或更多样化领域测试。
- **计算开销**：包含教师-学生双网络、分解器、多尺度对抗和互信息估计，较基线方法可能存在额外推理或训练负担，文中未深入讨论。
- **偏差风险**：情感分析模型可能被恶意滥用，如植入先验偏见识别特定群体情绪，论文虽提及但未提出具体缓解策略。
- **模态假设**：实验基于标准预提取特征，未验证端到端训练或更原始信号的有效性。
- **公平性**：所有实验均用重实现的方法，未与原始论文的超参搜索范围完全等同，可能存在微小偏差。

（完）
