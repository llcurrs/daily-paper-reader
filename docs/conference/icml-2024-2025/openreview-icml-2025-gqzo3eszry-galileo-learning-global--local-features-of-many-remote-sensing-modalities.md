---
title: "Galileo: Learning Global & Local Features of Many Remote Sensing Modalities"
title_zh: Galileo：学习多种遥感模态的全局与局部特征
authors: "Gabriel Tseng, Anthony Fuller, Marlena Reil, Henry Herzog, Patrick Beukema, Favyen Bastani, James R Green, Evan Shelhamer, Hannah Kerner, David Rolnick"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=gqZO3eSZRy"
tags: ["query:multi-modal"]
score: 8.0
evidence: 用于多种遥感模态的多模态Transformer
tldr: 针对遥感数据模态多样、目标尺度差异大的问题，提出Galileo多模态Transformer，通过自监督掩码建模从灵活输入模态中提取多尺度全局与局部特征，在多种遥感任务上展现了强大的表示学习能力，为遥感多模态融合与下游应用提供了高效基础模型。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-gqzo3eszry/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1051, \"height\": 624, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gqzo3eszry/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1672, \"height\": 992, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gqzo3eszry/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 850, \"height\": 525, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gqzo3eszry/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 815, \"height\": 678, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gqzo3eszry/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1729, \"height\": 748, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1754, \"height\": 725, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 620, \"height\": 215, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1046, \"height\": 1287, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1160, \"height\": 578, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 865, \"height\": 252, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 853, \"height\": 326, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 854, \"height\": 326, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 857, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 725, \"height\": 184, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 989, \"height\": 516, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 744, \"height\": 151, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 726, \"height\": 332, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 816, \"height\": 312, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1771, \"height\": 694, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1772, \"height\": 698, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1776, \"height\": 598, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gqzo3eszry/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1387, \"height\": 981, \"label\": \"Table\"}]"
motivation: 遥感数据模态多样，尺度差异大，学习共享表示存在挑战。
method: 提出双全局与局部特征的自监督多模态Transformer，通过掩码建模提取多尺度特征。
result: 在多种遥感模态上实现有效表示学习。
conclusion: 为遥感多模态融合和下游任务提供强大基础模型。
---

## Abstract
We introduce a highly multimodal transformer to represent many remote sensing modalities - multispectral optical, synthetic aperture radar, elevation, weather, pseudo-labels, and more - across space and time. These inputs are useful for diverse remote sensing tasks, such as crop mapping and flood detection. However, learning shared representations of remote sensing data is challenging, given the diversity of relevant data modalities, and because objects of interest vary massively in scale, from small boats (1-2 pixels and fast) to glaciers (thousands of pixels and slow). We present a novel self-supervised learning algorithm that extracts multi-scale features across a flexible set of input modalities through masked modeling. Our dual global and local contrastive losses differ in their targets (deep representations vs. shallow input projections) and masking strategies (structured vs. not). Our Galileo is a single generalist model that outperforms SoTA specialist models for satellite images and pixel time series across eleven benchmarks and multiple tasks.

---

## 论文详细总结（自动生成）

好的，我将基于您提供的论文内容，按照要求生成一份结构化的详细中文总结。

### 1. 论文的核心问题与整体含义

*   **核心问题**：遥感数据包含多种模态（如多光谱光学、合成孔径雷达、高程、天气等）并且目标尺度差异巨大（从小型船只到冰川），但现有的自监督学习方法通常专用于特定模态或数据形状（如图像时间序列或像素时间序列），缺乏一个能统一处理多模态、多时空尺度的通用模型。
*   **整体含义**：本文提出了一个名为 **Galileo** 的通用模型家族，旨在解决上述挑战。通过一个创新的自监督学习算法和全球采样的多模态预训练数据集，Galileo 能够从多种遥感模态和数据形状中学习多尺度的全局与局部特征，并以单一模型权重在多个下游任务中超越现有的专用型最先进模型。

### 2. 论文提出的方法论

*   **核心思想**：提出一种**双目标自监督学习算法**，通过掩码数据建模框架，同时学习遥感数据中的**全局（抽象、低频）** 和**局部（细粒度、高频）** 特征。
*   **关键技术细节**：
    *   **输入标记化**：一个灵活的视觉Transformer能处理时空数据、空间数据、时间数据和静态数据，通过可分离的时空位置编码和通道组嵌入来统一不同输入。
    *   **双损失函数与掩码策略**：
        *   **全局任务**：使用结构化的**时空掩码**（掩盖较大连续时空块），迫使模型进行长距离预测。其目标是“在线”编码器输出的**深层表示**，并通过“目标”编码器（指数移动平均）计算。损失函数采用基于批次负样本的对比损失（PatchDisc B）。
        *   **局部任务**：使用**非结构化随机掩码**（随机掩盖单个标记），迫使模型进行短距离预测。其目标是“目标”编码器浅层线性投影后的**浅层表示**。损失函数采用基于样本内负样本的对比损失（PatchDisc）。
    *   **算法流程**：
        1.  对输入数据进行掩码，生成“可见”部分和“目标”部分。
        2.  “在线”编码器处理可见部分。
        3.  预测器根据目标查询和可见编码进行预测。
        4.  “目标”编码器（梯度停止）处理目标部分，生成深层（全局）或浅层（局部）目标。
        5.  计算预测与目标之间的对比损失，并平均两个损失得到最终损失。

### 3. 实验设计

*   **预训练数据集**：Galileo 使用了一个自建的大规模、全球性多模态数据集，包含 **127,155** 个实例，覆盖了在空间/时间上变化的（Sentinel-1/2）、仅空间变化的（高程、土地覆盖）、仅时间变化的（天气、夜光）和静态的（人口、位置）共**9种**遥感数据模态。
*   **下游任务与基准**：在**11个**涵盖多种应用、领域和数据类型的基准上进行评估。
    *   **图像分类与分割**：GeoBench 中的 m-EuroSat, m-BigEarthNet, m-So2Sat, m-Brick-Kiln, m-Cashew-Plant, m-SA-Crop-Type，以及 MADOS（海洋垃圾分割）、Sen1Floods11（洪水分割）。
    *   **图像时间序列与像素时间序列**：PASTIS（农业分割）、Breizhcrops（作物分类）、CropHarvest（多模态作物分类）。
*   **对比方法**：与一系列最先进的预训练遥感模型进行比较，包括图像专用模型（如 SatMAE, CROMA, SoftCon, DOFA, DeCUR, Prithvi 2.0）和时间序列专用模型（如 Presto），以及一个通用的 AnySat 模型。评估覆盖了线性探测、K近邻和微调三种迁移学习协议，并在 100%、20%、5%、1% 四种训练数据比例下进行。

### 4. 资源与算力

*   **硬件**：所有模型均在 **单个 H100 GPU** 上进行预训练。
*   **模型尺寸与训练时长**：论文提供了三种规格的 ViT，并记录了在 H100 上预训练 500 个 epoch 的 GPU 小时数：
    *   **Galileo ViT-Nano**（0.8M 参数）：消耗 **200** GPU 小时。
    *   **Galileo ViT-Tiny**（5.3M 参数）：消耗 **259** GPU 小时。
    *   **Galileo ViT-Base**（85.0M 参数）：消耗 **573** GPU 小时。

### 5. 实验数量与充分性

*   **实验数量**：论文展示了**数百次**评估，实验数量非常庞大。这包括：
    *   在 **11个** 下游任务基准上进行评估，涵盖 **4种** 训练数据比例和 **3种** 迁移学习协议（kNN、线性探测、微调）。
    *   与超过 **15种** 不同架构的现有模型进行全面对比，并为其扫参。
    *   详尽的**消融研究**：针对全局和局部任务分别进行了消融，分析了掩码策略、目标深度、损失函数等关键组件的影响，并对最终合并算法和数据集模态进行了消融。
*   **充分性与公平性**：实验设计非常充分且客观公平。
    *   为排除输入尺寸和归一化方法的干扰，对**所有基线模型**重新运行了评估，并为其扫参，确保了比较的公平性。
    *   结果展示全面，不仅展示了最优结果，还提供了完整的排名表及详细的消融数据，结论具有高可信度。

### 6. 论文的主要结论与发现

*   **统一的通用模型可以超越专用模型**：Galileo-Base 在图像任务中的平均排名（3.0）和在像素时间序列任务中的平均排名（1.8）均超过所有图像或时间序列的专用模型，证明了通用模型的优越性。
*   **双目标预训练互补且有效**：消融实验证实，全局任务擅长图像分类等需要全局表征的任务，而局部任务擅长分割等需要局部细节的任务。同时应用双重目标不仅提升了模型在不同类型任务上的表现，还显著提高了训练的稳定性和一致性。
*   **多模态和多尺度学习的有效性**：Galileo 通过其灵活的架构和双目标预训练策略，成功地从多样化的遥感数据中学习到了多尺度的特征表示，使其能无缝应用于图像、图像时间序列、像素时间序列等多种输入形状。

### 7. 优点

*   **方法创新**：首次提出“深浅层对比学习”用于自监督学习，通过同时预测浅层输入投影和深层编表示，巧妙地引导模型学习局部和全局特征。这种双目标框架设计新颖且有效。
*   **模型的高度灵活性**：Galileo 是首个能同时处理如此多模态、多空间尺度和多时间尺度输入的通用模型，反映了真实的遥感应用需求，易于集成到现有工作流中。
*   **实验严谨且全面**：对大量基线方法重新评估和扫参，确保了对比的公平性。广泛的消融研究清晰地验证了方法各个组成部分的有效性。提供了不同尺寸模型，权衡了性能与计算成本，具有良好的实用性。
*   **数据与代码开源**：承诺开源模型权重、预训练代码、数据集和评估代码，具有很高的透明度和可复现性。

### 8. 不足与局限

*   **模态支持未在所有基准中体现**：尽管 Galileo 支持多种额外模态，但现有的标准基准数据集大多只包含光学或雷达数据，导致其在预训练中学到的其他模态能力无法在标准基准测试中得到验证和体现。
*   **计算资源需求**：尽管提供了 Nano 和 Tiny 小模型，但训练一个性能最佳的 Base 模型仍需单个 H100 GPU 训练近 24 天，这对计算资源有限的学术机构或个人开发者来说仍然是一个不小的门槛。
*   **预训练数据集偏差**：尽管数据集经过精心设计以保证地理和语义多样性，但仍可能无法完全代表全球所有地区的极端或罕见情况，模型在这些区域的下游性能可能需要进一步验证。
*   **生成能力的缺失**：论文的方法侧重于学习用于判别任务（如分类、分割）的表示，并未探讨模型是否具备像 MAE 那样的生成或像素重建能力。

（完）
