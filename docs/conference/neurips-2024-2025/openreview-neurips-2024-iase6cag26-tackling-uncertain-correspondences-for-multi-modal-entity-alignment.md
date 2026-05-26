---
title: Tackling Uncertain Correspondences for Multi-Modal Entity Alignment
title_zh: 处理不确定对应关系的多模态实体对齐
authors: "Liyi Chen, Ying Sun, Shengzhe Zhang, Yuyang Ye, Wei Wu, Hui Xiong"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=IAse6CAG26"
tags: ["query:multi-modal"]
score: 6.0
evidence: 处理多模态实体对齐中的模态缺失与不确定对应
tldr: 针对多模态知识图谱中模态缺失和描述多样性导致的不确定对应问题，提出TMEA方法，通过对齐增强机制提高实体对齐的鲁棒性。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-iase6cag26/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 988, \"height\": 763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-iase6cag26/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1447, \"height\": 742, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-iase6cag26/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1444, \"height\": 343, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-iase6cag26/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1454, \"height\": 656, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-iase6cag26/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1028, \"height\": 742, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-iase6cag26/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1449, \"height\": 684, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-iase6cag26/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 841, \"height\": 525, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-iase6cag26/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1431, \"height\": 715, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-iase6cag26/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 868, \"height\": 377, \"label\": \"Table\"}]"
motivation: 多模态实体对齐中模态缺失和描述差异阻碍实体相似度计算。
method: 设计对齐增强的编码与融合方法处理不确定对应关系。
result: TMEA在缺失模态场景下实现更准确的实体对齐。
conclusion: 为不完整多模态知识图谱融合提供了有效技术。
---

## Abstract
Recently, multi-modal entity alignment has emerged as a pivotal endeavor for the integration of Multi-Modal Knowledge Graphs (MMKGs) originating from diverse data sources. Existing works primarily focus on fully depicting entity features by designing various modality encoders or fusion approaches. However, uncertain correspondences between inter-modal or intra-modal cues, such as weak inter-modal associations, description diversity, and modality absence, still severely hinder the effective exploration of aligned entity similarities. To this end, in this paper, we propose a novel Tackling uncertain correspondences method for Multi-modal Entity Alignment (TMEA). Specifically, to handle diverse attribute knowledge descriptions, we design alignment-augmented abstract representation that incorporates the large language model and in-context learning into attribute alignment and filtering for generating and embedding the attribute abstract. In order to mitigate the influence of the modality absence, we propose to unify all modality features into a shared latent subspace and generate pseudo features via variational autoencoders according to existing modal features. Then, we develop an inter-modal commonality enhancement mechanism based on cross-attention with orthogonal constraints, to address weak semantic associations between modalities. Extensive experiments on two real-world datasets validate the effectiveness of TMEA with a clear improvement over competitive baselines.

---

## 论文详细总结（自动生成）

### 一、论文的核心问题与整体含义

- **研究背景**：多模态知识图谱（MMKG）融合了关系、属性和视觉等多种知识，对构建全面的知识库至关重要。多模态实体对齐（MMEA）旨在匹配来自不同 MMKG 但指向相同现实世界概念的实体。
- **研究动机**：现有方法主要致力于通过设计各种模态编码器或融合方式充分刻画实体特征，但忽视了实体间**不确定对应关系**的挑战，具体包括：
  - **跨模态语义关联弱**（如电影海报图像与属性“发行日期”之间缺乏语义重叠，难以实现跨模态增强）；
  - **属性描述差异大**（不同图谱中同一属性可能使用不同标签，如“Release Date”与“Debut Date”）；
  - **模态缺失**（实体可能完全缺少某类模态数据，容易导致错误匹配）。
- **整体含义**：论文提出一种专门处理多模态实体对齐中不确定对应关系的方法（TMEA），从模态缺失补全、属性描述对齐以及跨模态共性增强三个层面提升对齐性能。

### 二、提出的方法论

TMEA 包含三个核心模块，并采用双向迭代策略与多模态对比学习进行优化。

#### 2.1 多模态知识编码器

- **关系知识编码器**：沿用 TransE 作为基础编码器，结合交换策略学习三元组 `(头实体, 关系, 尾实体)` 的平移嵌入。
- **属性知识编码器**：  
  - 为应对属性描述差异，设计**对齐增强的抽象表示**。  
  - 使用 GPT-3.5 与上下文学习（in-context learning）进行属性对齐过滤，保留可对齐的属性。  
  - 将过滤后的属性三元组转换为抽象句子模板（如“属性名1 是 值1, 属性名2 是 值2 …”），再用预训练 BERT 提取句子嵌入作为属性特征。
- **视觉知识编码器**：使用预训练 ViT 提取图像特征，移除最后一层，得到视觉嵌入。

#### 2.2 缺失模态填补

- **目的**：通过统一不同模态到共享潜在空间，并生成伪特征以补全缺失的视觉或属性模态。
- **方法**：  
  - 将关系+视觉拼接特征、关系+属性拼接特征进行降维；  
  - 利用多个变分自编码器（VAE）分别学习目标模态（属性/视觉）与拼接特征的潜在表示，使同一实体不同模态来源的潜在表示相互靠近（最小化 MSE 损失）；  
  - 推断时，通过拼接特征的潜在表示经 VAE 解码器生成伪特征 `\(\tilde{\mathbf{e}}^A, \tilde{\mathbf{e}}^I\)`。

#### 2.3 跨模态共性增强

- **核心思想**：增强模态间原本微弱的语义关联，提取共性信息以获得更协调的实体表示。
- **机制**：  
  - 采用基于多头交叉注意力（cross-attention）的机制：以某一模态作为查询，另一模态作为键和值，得到提炼后的共性特征。  
  - 对关系、属性、视觉三种模态两两执行交叉注意力，并将原始特征与提炼特征加权融合。  
  - 引入**正交约束损失**：要求“原始特征 − 共性特征”与查询特征正交，迫使差量中不包含与查询相关的信息，从而突出共性。

#### 2.4 优化策略

- **多模态对比损失**（主目标）：对全局融合特征及各 uni-modal 特征，拉近对齐实体对的距离，推开非对齐实体对。
- **联合损失**：TransE 的边际损失、VAE 损失、MSE 损失、正交约束损失与对比损失加权组合。
- **双向迭代策略**：在训练过程中，将双向最近邻实体对不断加入训练集，缓解标注对齐对数量不足的问题。

### 三、实验设计

- **数据集**：  
  - FB15K-DB15K 与 FB15K-YG15K（均源自 FB15K 并分别对齐到 DBpedia 和 YAGO），包含关系、属性和视觉知识。  
  - 使用 20% 对齐实体对作为训练集，其余用于测试。
- **评估指标**：Hits@1/5/10、MRR、MR。
- **对比方法**：  
  - 传统实体对齐方法：IPTransE、GCN-Align、BootEA、SEA、RAC、PEEA、MixTEA 等。  
  - 多模态实体对齐方法：PoE、MMEA、EVA、MSNEA、MCLEA、ACK-MMEA、MoAlign。
- **消融实验**：  
  - 模态消融：分别移除视觉、关系、属性模块（w/o V/R/A）。  
  - 组件消融：去除 MMI、MCE、`\(L_o\)`、`\(L_{mse}\)`、属性预处理（AP）、迭代策略（IT）等。  
- **分析实验**：  
  - 模态缺失比例敏感度（与 MSNEA 对比，从 20% 到 100% 拥有视觉/属性模态）；  
  - 训练标签比例依赖分析（20%、50%、80% 对齐对）。

### 四、资源与算力

- **硬件环境**：实验在配备 2 颗 Intel Xeon Silver 4214R @ 2.40GHz CPU、4 块 NVIDIA RTX 3090 GPU、256 GB 内存的服务器上进行。
- **训练时长**：论文未提及具体训练时间，但声明冻结了预训练 ViT 和 BERT 的参数，这通常会降低计算开销。
- **其他资源**：使用了 GPT-3.5 API 进行属性对齐（非微调，仅做推理）。

### 五、实验数量与充分性

- **实验数量**：  
  - 在两个数据集上进行了性能对比（包含 16 个基线方法）；  
  - 模态消融（3 种）、组件消融（7 种）、模态缺失敏感度实验（含多个比例）、训练标签比例实验（3 种比例）、超参数敏感性分析（λ1、λ2 分别取 6 个值）；  
  - 合计约 **20 组以上**的配置实验。
- **充分性与公平性**：  
  - 基线方法覆盖全面，包括传统和 SOTA 多模态方法，对比基准明确；  
  - 消融实验较充分地验证了各模块贡献；  
  - 模态缺失与标签比例实验揭示了方法鲁棒性；  
  - 实验设置（如 20% 训练数据）与前期工作一致，对比公平。

### 六、主要结论与发现

- TMEA 在两个数据集上均显著优于所有对比方法，相较最强基线 MSNEA，H@1 至少提高 32.8%，MRR 至少提高 26.4%。
- 属性对齐增强（LLM + 上下文学习）能有效处理属性描述差异，抽象句子嵌入优于原始属性使用。
- 缺失模态填补（MMI）提升了不完整模态下的鲁棒性，尤其在视觉模态大量缺失时性能下降更缓。
- 跨模态共性增强（MCE + 正交约束）有效缓解了模态间语义关联弱的问题，去除该模块后性能大幅下降。
- TMEA 在标签样本稀缺时性能依然稳定，表现出较低的标签依赖性。

### 七、优点

- **问题聚焦明确**：首次系统处理多模态实体对齐中的不确定对应（模态缺失、属性差异、跨模态弱关联），具有较强创新性。
- **方法设计精细**：  
  - 巧妙利用 LLM 进行属性对齐和抽象生成，无需额外标注；  
  - VAE 生成伪特征补全缺失模态，且通过共享潜在空间实现模态统一；  
  - 交叉注意力 + 正交约束的共性增强机制增强了跨模态语义对齐。
- **实验全面扎实**：多组消融和分析实验验证了各模块有效性和鲁棒性，统计显著性也得到了说明。
- **性能提升显著**：指标大幅领先同类方法，尤其在 H@1 和 MRR 上表现突出。

### 八、不足与局限

- **LLM 依赖外部知识**：属性对齐使用 GPT-3.5 只在通用语料上训练，缺乏 KG 领域特定知识，可能限制对齐准确性；文中仅用 LLM 做对齐，未微调。
- **模态补全假设**：MMI 假定关系模态总是存在，但现实中孤立实体的关系也可能缺失；伪特征生成质量依赖 VAE 和现有模态质量。
- **对齐标签依赖**：虽然 TMEA 在低标签比例下较鲁棒，但整体仍依赖一定数量的标注对齐对进行训练，未探索完全无监督场景。
- **实验局限**：只在两个公共数据集上验证，未探讨在更大规模或更异构多模态图谱上的泛化能力；未与传统单模态对齐结合软标签策略做更深入对比。
- **未涉及多语言/跨语言场景**：实验数据集为英文知识图谱，未考虑跨语言实体对齐中的特有挑战。

（完）
