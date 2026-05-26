---
title: Learning Compact Semantic Information for Incomplete Multi-View Missing Multi-Label Classification
title_zh: 面向不完整多视图缺失多标签分类的紧致语义信息学习
authors: "Jie Wen, Yadong Liu, Zhanyan Tang, Yuting He, Yulong Chen, Mu Li, Chengliang Liu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=RbsfEuYNTA"
tags: ["query:multi-modal"]
score: 8.0
evidence: 利用紧凑语义信息学习实现不完整多视图缺失多标签分类
tldr: 该论文针对不完整多视图数据下的缺失多标签分类问题，指出当前对比学习方法在一致性表示学习上存在局限，导致共享信息提取瓶颈。为此提出通过信息瓶颈原理最小化任务无关冗余信息，学习紧致语义表示。实验表明方法在多个不完整视图数据集上取得优异分类性能。虽然未直接使用遥感数据，但其处理缺失模态和多标签联合学习的思路可迁移至遥感图像分析，为缺失模态下的多模态遥感分类提供了有效方法论支撑。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-rbsfeuynta/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 854, \"height\": 337, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-rbsfeuynta/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 852, \"height\": 356, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-rbsfeuynta/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1706, \"height\": 748, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-rbsfeuynta/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 850, \"height\": 376, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-rbsfeuynta/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1713, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-rbsfeuynta/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 849, \"height\": 378, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-rbsfeuynta/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1611, \"height\": 449, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-rbsfeuynta/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1717, \"height\": 374, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-rbsfeuynta/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1369, \"height\": 546, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-rbsfeuynta/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1775, \"height\": 1145, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-rbsfeuynta/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 862, \"height\": 363, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-rbsfeuynta/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 919, \"height\": 282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-rbsfeuynta/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1132, \"height\": 386, \"label\": \"Table\"}]"
motivation: 不完整多视图学习中，有限监督与缺失数据导致判别表示难以学习。
method: 利用信息瓶颈原理最小化冗余信息，提取紧致共享语义表示。
result: 在多个不完整视图多标签数据集上分类性能大幅提升。
conclusion: 紧致语义信息学习有效解决了缺失视图下的多标签分类，可推广至遥感缺失模态问题。
---

## Abstract
Multi-view data involves various data forms, such as multi-feature, multi-sequence and multimodal data, providing rich semantic information for downstream tasks. The inherent challenge of incomplete multi-view missing multi-label learning lies in how to effectively utilize limited supervision and insufficient data to learn discriminative representation. Starting from the sufficiency of multi-view shared information for downstream tasks, we argue that the existing contrastive learning paradigms on missing multi-view data show limited consistency representation learning ability, leading to the bottleneck in extracting multi-view shared information. In response, we propose to minimize task-independent redundant information by pursuing the maximization of cross-view mutual information. Additionally, to alleviate the hindrance caused by missing labels, we develop a dual-branch soft pseudo-label cross-imputation strategy to improve classification performance. Extensive experiments on multiple benchmarks validate our advantages and demonstrate strong compatibility with both missing and complete data.

---

## 论文详细总结（自动生成）

# 论文总结：面向不完整多视图缺失多标签分类的紧致语义信息学习

## 1. 核心问题与整体含义
- **研究问题**：针对实际应用中多视图数据（如多特征、多模态）普遍存在的视图缺失和标签缺失双重问题，开展不完整多视图缺失多标签分类（iM3C）研究。
- **动机与背景**：
  - 传统多视图多标签学习方法通常假设数据完全观测，但真实场景中视图和标签同时缺失的现象十分常见（如医疗诊断中部分报告缺失、标注不全）。
  - 现有基于对比学习的缺失多视图方法，在缺失情况下对跨视图一致性信息的提取能力有限，导致共享语义表示学习出现瓶颈。
  - 用硬伪标签填补缺失标签时，简单 Top‑1 或固定数量策略容易忽略真实多标签分布或引入噪声，造成误差累积。
- **整体含义**：提出一种紧致语义信息学习框架 COME，通过最大化跨视图互信息来压缩任务无关冗余信息，并结合双分支软伪标签交叉填补策略，在有限监督和不完整数据下提升多标签分类性能。

## 2. 方法论
**核心思想**：从“多视图共享信息对下游任务充分性”出发，学习一个既紧致又充分的跨视图联合表示，并利用双分支协同训练生成可靠的软伪标签来缓解监督缺失。

**关键技术细节**：
- **紧致共享表示学习**
  - 在标准缺失多视图对比学习（最大化视图间互信息）的基础上，引入基于专家混合（MoE）的互信息增强策略。
  - 最大化原始数据与跨视图联合表示之间的互信息，推导出变分下界，将其转化为两项重构损失：
    - **视图内重构**：用该视图表示重建自身视图。
    - **跨视图重构**：用某视图表示重建另一视图。
  - 结合重构损失与对比损失，实现“最小且充分的共享表示”，防止信息过度压缩或崩溃。
- **双分支软伪标签交叉填补**
  - 构建两个结构相同但独立的模型分支（A 和 B）。
  - 每个分支对缺失类别生成软伪标签，并通过动态阈值机制（随训练轮次由严到松）筛选高置信预测。
  - 分支 A 使用分支 B 生成的软伪标签作为额外监督，反之亦然，形成交叉填补，避免自我回环放大错误。
- **联合训练目标**
  - 总损失：对比损失 + 视图内重构损失 + 跨视图重构损失 + 双分支交叉熵分类损失。
  - 训练算法清晰给出双分支参数独立更新的流程。

## 3. 实验设计
- **数据集**：五个标准多视图多标签数据集，均包含六种手工特征视图（GIST、HSV、DenseHue、DenseSIFT、RGB、LAB）。
  - Corel5k（4,999 样本，260 标签），Pascal07（9,963 样本，20 标签），ESPGame（20,770 样本，268 标签），IAPRTC12（19,627 样本，291 标签），Mirflickr（25,000 样本，38 标签）。
- **缺失模拟**：
  - 视图缺失：每个视图随机屏蔽 50% 样本，保证每样本至少有一个视图可用。
  - 标签缺失：每个类别随机移除 50% 的正、负标签。
  - 训练/测试划分：随机抽取 70% 作为训练集。
- **对比方法**：CDMM、DM2L、LVSL、iMVWL、NAIM3L、DICNet、UPDGD‑Net、SIP。针对不能处理缺失的方法（CDMM、LVSL 等）进行了均值填充等适配处理。
- **评估指标**：基于 AP、1‑HL、1‑RL、AUC、1‑OE、1‑Cov 六个指标（越高越好），与先前工作对齐。

## 4. 资源与算力
- 论文未明确提及训练所使用的 GPU 型号、数量、显存规模以及具体训练时长等算力信息。

## 5. 实验数量与充分性
- **主要实验**：在 50% 视图缺失、50% 标签缺失的设定下，在五个数据集上与八种方法全面对比，给出六项指标的均值和标准差。
- **缺失率变化实验**：在 Pascal07 上测试不同视图缺失率（0%、30%、50%、70%）和不同标签缺失率（0%、30%、50%、70%）下的性能，表明视图缺失影响更严重。
- **完整数据实验**：在无任何缺失的理想数据集上评估所有方法，展示 COME 的强泛化能力，结果以雷达图展示。
- **消融实验**：在 Corel5k 和 Pascal07 上拆分损失项（视图内重构、跨视图重构、伪标签损失），验证各组件均有正向贡献，且跨视图重构最为关键。
- **参数敏感性分析**：考察损失平衡系数 \(\lambda_1, \lambda_2\) 对性能的影响，显示模型对参数变化鲁棒。
- **均衡性分析**：探究对比损失系数 \(\beta\) 与重构损失的平衡关系，展示信息压缩与重建的 trade‑off。
- 实验涵盖多种缺失比例、多个数据集、消融和参数分析，数量充分，对比方法覆盖近期相关工作和经典基准，比较公平。

## 6. 主要结论与发现
- 提出的 COME 在五个数据集的不完整场景下全面优于现有八种方法，且在全数据场景下依然取得最优或竞争性结果，证明方法具有强鲁棒性和泛化能力。
- 最大化跨视图互信息的信息增强策略有效缓解了缺失数据下对比学习的局限性，使共享表示更紧致且保留任务关键信息。
- 双分支交叉软伪标签填补策略能比传统硬标签方法减少错误累积，提升多标签分类性能。
- 相较标签缺失，视图缺失对模型性能的负面影响更大。

## 7. 优点
- 创新性地将“最小充分表示”理念与多视图缺失场景结合，从信息论角度设计损失函数，理论动机清晰。
- 提出的跨视图重构与对比学习联合优化框架，兼顾信息压缩与有效性保持，实验证明其设计有效。
- 双分支软伪标签交叉生成策略，通过动态阈值和外部监督有效避免了自训练中的确认偏差。
- 模型对任意视图和标签缺失比例均有良好适应性，无需针对特定缺失模式做调整。
- 大量实验设计细致（包括完整数据适配、多级缺失率、消融与参数分析），结论可信。

## 8. 不足与局限
- **算力开销未说明**：未报告模型的计算复杂度、推理速度或训练资源需求，不便评估实际部署成本。
- **特征依赖**：实验均采用手工提取的六种视觉特征，未在其他模态（如文本、语音）或端到端深度学习特征上验证，跨模态通用性有待探索。
- **缺失模式单一**：仅模拟随机的视图和标签缺失，未考虑块缺失、非随机缺失等更复杂的现实情况。
- **双分支结构开销**：双分支网络会带来额外存储和计算，论文未讨论该成本与性能提升之间的权衡。
- **标签数量分布影响**：未深入分析当标签数量极多或极不平衡时伪标签策略的稳定性，可能导致低置信类别被长期忽略。
- **浅层模型**：解码器与拼接融合方式较为简单，可能限制更复杂高维数据下的表示能力。

（完）
