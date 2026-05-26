---
title: "Miss-ReID: Delivering Robust Multi-Modality Object Re-Identification Despite Missing Modalities"
title_zh: Miss-ReID：面向模态缺失的鲁棒多模态物体重识别
authors: Ruida Xi
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=7x5X6gTCUH"
tags: ["query:multi-modal"]
score: 7.0
evidence: 解决多模态物体重识别中的模态缺失问题
tldr: 多模态物体重识别技术在模态完整时表现优异，然而实际应用中常面临模态缺失问题，导致识别精度大幅下降。为解决这一挑战，本文提出Miss-ReID框架，首次同时支持模态缺失的训练和推理场景。其核心设计包括模态间特征交互与动态重构机制，能够有效弥补缺失信息，在多个主流数据集上进行的实验表明，即使在严重模态缺失条件下，该方法仍保持较高的检索准确率，显著优于现有方法，为鲁棒多模态检索系统的落地提供了关键技术支持。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-7x5x6gtcuh/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1438, \"height\": 486, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7x5x6gtcuh/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1454, \"height\": 590, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7x5x6gtcuh/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1439, \"height\": 283, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7x5x6gtcuh/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1447, \"height\": 204, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7x5x6gtcuh/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1324, \"height\": 1203, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7x5x6gtcuh/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1447, \"height\": 532, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7x5x6gtcuh/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1461, \"height\": 1322, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-7x5x6gtcuh/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1392, \"height\": 418, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7x5x6gtcuh/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1452, \"height\": 607, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7x5x6gtcuh/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1456, \"height\": 527, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7x5x6gtcuh/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1443, \"height\": 568, \"label\": \"Table\"}]"
motivation: 真实多模态重识别常面临模态缺失，现有模型在缺失输入下性能大幅下降。
method: 提出Miss-ReID框架，通过跨模态交互和动态特征重构，首次同时支持模态缺失的训练与推理。
result: 实验表明，在多种模态缺失率下，Miss-ReID显著优于现有方法，保持高检索准确率。
conclusion: 为真实场景中鲁棒多模态检索提供了有效且实用的解决方案，推动了缺失模态学习的发展。
---

## Abstract
Multi-modality object Re-IDentification (ReID) targets to retrieve special objects by integrating complementary information from diverse visual sources.
However, existing models that are trained on modality-complete datasets typically exhibit significantly degraded discrimination
during inference with modality-incomplete inputs.
This disparity highlights the necessity of developing a robust multi-modality ReID model that remains effective in real-world applications. For that, this paper delivers a flexible framework tailored for more realistic multi-modality retrieval scenario, dubbed as Miss-ReID, which is the first work to friendly support both the modality-missing training and inference conditions. The core of Miss-ReID lies in compensating for missing visual cues via vision-text knowledge transfer driven by Vision-Language foundation Models (VLMs), effectively mitigating performance degradation. In brief, we capture diverse visual features from accessible modalities first, and then build memory banks to store heterogeneous prototypes for each identity, preserving multi-modality characteristics. Afterwards, we employ structure-aware query interactions to dynamically distill modality-invariant object structures from existing localized visual patches, which are further reversed into pseudo-word tokens that encapsulate the identity-relevant structural semantics.
In tandem, the inverted tokens, integrated with learnable modality prompts, are embedded into crafted textual template to form the personalized linguistic descriptions tailored for diverse modalities.
Ultimately, harnessing VLMs' inherent vision-text alignment capability, the resulting textual features effectively function as compensatory semantic representations for missing visual modalities, after being optimized with some memory-based alignment constraints.
Extensive experiments demonstrate our model's efficacy and superiority over state-of-the-art methods in various modality-missing scenarios, and our endeavors further propel multi-modality ReID into real-world applications.

---

## 论文详细总结（自动生成）

# 论文总结：Miss-ReID: Delivering Robust Multi-Modality Object Re-Identification Despite Missing Modalities

## 1. 论文的核心问题与整体含义
- **研究动机**：多模态物体重识别（ReID）通过融合RGB、近红外（NIR）、热红外（TIR）等互补信息提升识别鲁棒性。然而现有方法均假设训练和推理阶段所有模态完整可用，实际应用中因传感器故障、隐私保护等原因常出现部分模态缺失，导致模型性能急剧下降。
- **核心问题**：如何在模态缺失的**训练和推理**场景下，保持高效、鲁棒的多模态物体重识别。
- **整体含义**：本文首次提出同时支持模态缺失训练和推理的柔性框架 Miss-ReID，利用视觉-语言基础模型（VLMs）的跨模态对齐能力，用文本语义补偿缺失的视觉信息，推动多模态 ReID 走向现实部署。

## 2. 论文提出的方法论
Miss-ReID 主要由三个协同模块构成：

### (1) 基于记忆的异构身份原型表示 (M-bHIPR)
- 利用共享的视觉编码器（来自预训练 CLIP）提取各可用模态的视觉特征。
- 为每个模态维护一个独立记忆库，存储每个身份的原型向量（特征中心）。
- 原型初始化：身份 k 在模态 m 的所有观测样本特征平均；若无样本则零初始化。
- 更新方式：指数滑动平均（EMA），动量系数 α=0.2，避免跨模态特征污染。
- 损失：模态内 ClusterNCE 对比损失，增强身份区分性。

### (2) 模态不变物体结构建模 (M-iOSM)
- 观察到物体结构（部位空间关系、场景元素组成）在不同模态间具有一致性。
- 用一组可学习的“结构探针”查询向量 Q，通过多头注意力机制从各模态的局部图像块中提取模态不变的结构特征。
- 将各模态的结构特征按跨模态平均融合，得到最终的模态不变结构表示 si。
- 结构特征受标签平滑交叉熵损失和三元组损失监督。

### (3) 语言驱动的缺失模态补全 (L-dMMC)
- 用轻量反转网络（MLP）将结构特征 si 映射为“身份伪词”$w^{inv}$，编码身份相关的结构语义。
- 将伪词与可学习的模态特定提示 $P^m$ 嵌入预设文本模板（如“An image of a [伪词] person, who shows the [模态m] attributes.”），经冻结的文本编码器生成文本特征 $\tilde{f}^m_i$。
- 当模态 m 缺失时，该文本特征作为该模态的补偿表示；可用时作为重建表示。
- 优化：记忆库驱动的文本-视觉对比损失 $L^{m}_{T2V}$，使文本特征与模态内对应身份的原型对齐。
- L-dMMC 模块在训练 20 个 epoch 后引入，以稳定训练。

### 总体目标函数
包含视觉/结构/文本分支的三元组损失、标签平滑交叉熵损失，以及上述两个对比损失，通过平衡权重 λ1、λ2 联合优化。

## 3. 实验设计
- **数据集**：
  - 行人 ReID：RGBNT201（3模态）
  - 车辆 ReID：RGBNT100（3模态）
- **模态缺失模拟**：训练时按预设缺失率元组（如 η=(0.1,0.1,0.1) 表示每种模态10%概率缺失）随机将样本置为零张量；推理时直接排除对应模态的图像。
- **评估设置**：
  - 指标：mAP 和 Rank-1 准确率。
  - 场景：1 个模态完整场景 (RNT) + 6 个模态缺失场景（如 R̸NT 缺RGB），同时报告所有缺失场景的平均值。
- **对比方法**：PCB、TOP-ReID、DeMo、IDEA（行人）；DENet、TOP-ReID、DeMo（车辆）。
- **自身消融**：逐步添加 M-bHIPR、M-iOSM、L-dMMC 模块，验证各自贡献。
- **缺失率鲁棒性**：变化三元缺失率 (0.0,0.0,0.0) 到 (0.5,0.5,0.5)，观察性能衰减。
- **扩展评估**（附录）：49 种“查询-画廊”模态组合的实际场景、t-SNE 特征分布、注意力区域可视化等。

## 4. 资源与算力
- **硬件**：单块 NVIDIA RTX A6000 GPU，48 GB 显存。
- **软件**：PyTorch 实现，预训练 CLIP 作为视觉和文本编码器。
- **训练配置**：总 50 epoch，L-dMMC 自第 20 epoch 引入；可学习模块用 Adam 优化器，学习率 5e-3（模态提示）和 3.5e-4（其它）；文本编码器冻结。
- **未明确说明**：单次训练的具体时长（如小时数）文中未提供。

## 5. 实验数量与充分性
- **实验组数**：至少包括：
  - 行人数据集上的模块消融（6种组合 × 2种训练设置）= 12项结果；
  - 行人数据集 SOTA 对比（5种方法 × 7种推理场景）；
  - 车辆数据集 SOTA 对比（4种方法 × 7种推理场景）；
  - 不同缺失率影响（6组缺失率 × 7种推理场景）；
  - 附录中 49 种真实场景矩阵评估；
  - 可视化分析（注意力、特征分布、排序列表）。
- **充分性与客观性**：实验覆盖了两种对象类型（人、车），多种缺失配置，与多个 SOTA 公平对比，并在附录中补充了丰富的真实场景鲁棒性验证和可视化，消融严格，论证充分。

## 6. 论文的主要结论与发现
- Miss-ReID 是**首个**能够在模态缺失训练和推理双重条件下工作的多模态 ReID 框架，无需数据完整性假设。
- 利用 VLM 的视觉-文本对齐能力，将缺失的视觉模态补偿为语义对齐的文本特征，有效缓解性能衰减。
- 在多种缺失场景下，Miss-ReID 相比现有 SOTA 方法展现出**最低的性能下降率**和**最高的平均检索精度**，尤其在极端缺失情况下优势明显。
- 证明了基于记忆库的原型存储、模态不变结构提取和语言驱动补全的协同设计是解决模态缺失 ReID 的有效途径。

## 7. 优点
- **问题实际性强**：首次系统处理“训练+推理双缺失”的真实应用痛点。
- **方法论新颖**：巧妙融合 VLM 的文本嵌入补偿缺失视觉，构建了“结构→伪词→文本特征”的生成式补全通路。
- **模块协同设计**：M-bHIPR 保持模态特异性，M-iOSM 提取跨模态共性，L-dMMC 完成语义补偿，分工明确，效果叠加。
- **实验全面扎实**：多数据集、多缺失率、多评估指标，对比广泛，可视化丰富，提升了结论可信度。
- **可扩展性**：模板和提示的设计使框架易于适配不同对象类型（行人/车辆）。

## 8. 不足与局限
- **极端缺失敏感**：文中指出在完全模态崩塌等极端情况下性能仍有限，需进一步研究。
- **模态种类受限**：当前仅针对 RGB、NIR、TIR 三种常见视觉模态，对事件相机、LiDAR、音频等更多模态的扩展未验证。
- **幻觉风险**：依赖 VLM 进行文本补偿时，生成的语义可能偏离真实缺失模态的信息，尤其在未见过的对象或场景下可能存在伪影。
- **计算开销**：引入反转网络和文本编码增加参数量（从 86.4M 到 89.6M）和计算量（34.3G 到 43.6G FLOPs），但换取了显著精度提升。
- **训练稳定性**：L-dMMC 需滞后 20 个 epoch 加入，增加了调参复杂度。
- **数据集偏差**：实验仅基于现有 ReID 基准，未测试更通用的多模态识别任务或域外场景。

（完）
