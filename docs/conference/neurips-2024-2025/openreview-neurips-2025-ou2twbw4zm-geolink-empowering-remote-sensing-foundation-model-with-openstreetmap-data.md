---
title: "GeoLink: Empowering Remote Sensing Foundation Model with OpenStreetMap Data"
title_zh: GeoLink：利用OpenStreetMap数据增强遥感基础模型
authors: "Lubin Bai, Xiuyuan Zhang, Siqi Zhang, Zepeng Zhang, Haoyu Wang, Wei Qin, Shihong Du"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=ou2TWBW4zm"
tags: ["query:multi-modal"]
score: 9.0
evidence: 融合OpenStreetMap数据与遥感影像进行基础模型预训练
tldr: 针对现有遥感基础模型仅利用影像而忽略地理上下文的问题，提出GeoLink框架，将OpenStreetMap数据与遥感影像多模态融合。通过跨模态对齐和自监督预训练策略，从OSM数据中提取多粒度学习信号增强模型。实验表明，GeoLink在多种遥感任务上提升性能，展示了利用开放地理数据增强遥感智能的潜力。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou2twbw4zm/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1423, \"height\": 530, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou2twbw4zm/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1436, \"height\": 1112, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou2twbw4zm/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1402, \"height\": 931, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou2twbw4zm/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 683, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou2twbw4zm/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1422, \"height\": 526, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou2twbw4zm/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1439, \"height\": 724, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou2twbw4zm/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1437, \"height\": 583, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou2twbw4zm/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1418, \"height\": 1406, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ou2twbw4zm/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1434, \"height\": 916, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 283, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1443, \"height\": 304, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 854, \"height\": 262, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 637, \"height\": 269, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1324, \"height\": 659, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 708, \"height\": 223, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1341, \"height\": 297, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1431, \"height\": 816, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1437, \"height\": 533, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1049, \"height\": 149, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1035, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1281, \"height\": 205, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1058, \"height\": 219, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ou2twbw4zm/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1403, \"height\": 185, \"label\": \"Table\"}]"
motivation: 遥感基础模型缺乏与地理上下文数据的有效融合，模态差异大。
method: 利用跨模态对齐与自监督学习，将OSM多粒度信息融入遥感预训练。
result: 在多个下游任务中，GeoLink显著优于仅使用影像的基线模型。
conclusion: 为遥感基础模型融合开放地理数据提供了新范式。
---

## Abstract
Integrating ground-level geospatial data with rich geographic context, like OpenStreetMap (OSM), into remote sensing (RS) foundation models (FMs) is essential for advancing geospatial intelligence and supporting a broad spectrum of tasks. However, modality gap between RS and OSM data, including differences in data structure, content, and spatial granularity, makes effective synergy highly challenging, and most existing RS FMs focus on imagery alone. To this end, this study presents GeoLink, a multimodal framework that leverages OSM data to enhance RS FM during both the pretraining and downstream task stages. 
Specifically, GeoLink enhances RS self-supervised pretraining using multi-granularity learning signals derived from OSM data, guided by cross-modal spatial correlations for information interaction and collaboration. It also introduces image mask-reconstruction to enable sparse input for efficient pretraining. For downstream tasks, GeoLink generates both unimodal and multimodal fine-grained encodings to support a wide range of applications, from common RS interpretation tasks like land cover classification to more comprehensive geographic tasks like urban function zone mapping. Extensive experiments show that incorporating OSM data during pretraining enhances the performance of the RS image encoder, while fusing RS and OSM data in downstream tasks improves the FM’s adaptability to complex geographic scenarios. These results underscore the potential of multimodal synergy in advancing high-level geospatial artificial intelligence. Moreover, we find that spatial correlation plays a crucial role in enabling effective multimodal geospatial data integration. Code, checkpoints, and using examples are released at [GitHub](https://github.com/bailubin/GeoLink_NeurIPS2025).

---

## 论文详细总结（自动生成）

# 论文分析总结：GeoLink——利用 OpenStreetMap 数据增强遥感基础模型

## 1. 核心问题与研究背景
- **核心问题**：现有的遥感基础模型（RS FMs）几乎完全依赖遥感影像进行预训练，忽略了地面级地理上下文数据（如 OpenStreetMap, OSM）所提供的丰富语义、社会经济学信息。两者之间存在显著的**模态鸿沟**（数据结构、内容、空间粒度不同），导致难以有效协同。
- **研究动机**：OSM 作为最大的志愿者地理信息数据库，包含点、线、面等矢量对象及其标签，能够为遥感解译提供显式位置上下文、消除视觉歧义，并补充影像无法提供的城市功能、社会经济等深层次信息。然而，现有融合方法多为间接转换（如栅格化、生成标签或描述文本），丢失了空间信息，且依赖于手动、任务特定的处理，与基础模型的大规模、任务无关范式不匹配。
- **整体含义**：本文提出 **GeoLink 多模态框架**，旨在**直接利用原始 OSM 矢量数据**，通过空间显式的跨模态交互，在预训练和下游任务阶段增强遥感基础模型，从而推动更高级的地理空间人工智能。

## 2. 方法论
GeoLink 通过**多粒度学习信号**和**空间感知的跨模态融合**，将 OSM 数据注入遥感预训练与下游任务中。

- **OSM 图构建**：
  - 将 OSM 地图建模为**异构图**，节点为点（point）、折线（polyline）、多边形（polygon），边表示它们之间的空间拓扑关系（如包含、相交、相切等）。
  - 节点初始特征：利用预训练 BERT 模型对每个 OSM 对象的“标签-值”对进行编码，并按其全局出现频率加权平均，获得语义初始化向量。

- **多粒度跨模态学习信号**：
  - **区域-图像级对齐**：使用对比学习（InfoNCE）将聚合后的OSM区域编码与遥感图像编码对齐，将OSM中的结构化语义传递给图像编码器。
  - **对象-补丁级融合**：设计**位置感知的交叉注意力融合编码器**，利用正弦位置嵌入（对点直接使用，对线/面则采样关键点后取均值）为每个向量元素提供空间坐标，从而在图像补丁和 OSM 对象之间建立精确的跨模态关联，生成细粒度的混合表征。

- **掩码策略与预训练目标**：
  - **掩码输入**：随机掩码大量的图像补丁（如75%）和部分 OSM 节点（20%），仅输入可见部分以加速训练。
  - **三大损失函数**：
    1.  **L_rec**（遥感重建损失）：解码器重建被掩码的图像补丁的均方误差。
    2.  **L_cont**（对比损失）：区域级OSM与图像编码之间的 InfoNCE 损失。
    3.  **L_cst**（空间一致性损失）：融合编码器输出的混合 OSM-RS 对象编码与被掩码节点的原始特征之间的均方误差，强制保持空间语义一致性。
  - **总损失**：L = αL_rec + βL_cont + γL_cst（默认 α=1, β=0.01, γ=0.01）。

- **下游任务适配**：
  - 预训练后，模型可输出**单模态（遥感图像编码）** 和**多模态（混合 RS-OSM 补丁编码）** 两种特征，以灵活支持遥感解译任务（分类、分割、变化检测）及综合性地理任务（城市功能区制图、人口/碳排放估算）。

## 3. 实验设计

- **预训练数据集**：基于 SkyScript-top30 构建，包含 1,271,431 对遥感图像（RGB，分辨率 0.1m-30m）与对应区域的 OSM 数据。
- **下游基准与方法对比**：
  - **单模态任务**：
    - **图像分类**：7 个数据集（MLRSNet, EuroSAT, RESISC-45 等），采用 kNN、线性探测（LP）、微调（FT）三种协议评估。
    - **语义分割与变化检测**：4 个数据集（Five-Billion-Pixels, AI4SmallFarms, SpaceNet7, xView2），使用 UperNet 解码器，在冻结与微调设置下评估。
    - 对比 6 个基线模型：GASSL, MMEarth, Scale-MAE, Cross-Scale MAE, CROMA, DOFA。
  - **多模态地理任务**（自建数据集，包含芝加哥、新加坡、深圳等区域）：
    - **城市功能区（UFZ）分割**：9 类，使用 UperNet。
    - **城中村（UV）识别**：二分类语义分割。
    - **人口密度（POP）与碳排放（CO₂）估计**：使用两层 MLP 回归。
    - 对比：Scale-MAE 单模态、Scale-MAE+OSM、GeoLink 单/多模态。

- **消融与鲁棒性实验**：
  - 学习目标组合、RS 和 OSM 掩码比率、融合模块的位置嵌入、OSM 编码器变体（GCN/Transformer）。
  - OSM 数据完整性（随机移除 0%-50% 对象）。
  - 少样本设置（仅 10% 训练数据）。
  - 损失权重调整。

## 4. 资源与算力
- **硬件**：4 块 NVIDIA RTX6000 GPU（48GB 显存）。
- **精度与优化**：bfloat16 混合精度，使用 AdamW 优化器（β₁=0.9, β₂=0.95），权重衰减 0.05。
- **预训练配置**：批量大小 2640，基础学习率 1e-4，余弦退火调度。仅预训练 **60 个 epoch**（含 5 个 warmup），显著快于传统 MAE 类方法（如 Scale-MAE 需 800 轮）。

## 5. 实验数量与充分性
- **实验组别丰富**：涵盖 7 个分类数据集 × 3 种协议，4 个分割/变化检测数据集 × 2 种设置，4 个多模态任务 × 4 种模型配置，以及多个消融研究（至少 15 种变体）。整体实验量巨大。
- **充分性与客观性**：
  - 对比基线全面，包含单模态（同光谱）与多模态（跨光谱）方法。
  - 每个实验重复 3 次不同随机种子取平均，确保统计稳定性。
  - 消融实验系统性地考察了核心设计组件对单模态和多模态下游性能的影响。
  - 可视化（T-SNE、区域制图）辅助验证表征质量和实际应用效果。
  - 评估协议客观，如分类任务固定数据划分，分割任务遵循 PANGAEA 基准。

## 6. 主要结论与发现
- **预训练增益显著**：引入 OSM 数据后，GeoLink 的遥感图像编码器在分类任务（尤其 kNN 和少样本下）全面超越所有对比基线，表明学习到的表征更结构化、更通用。
- **多模态融合提升复杂任务适应性**：在城市功能区、人口/碳排放等需要多源信息的任务中，GeoLink 的多模态融合性能大幅领先单模态模型，证明了 OSM 语义对地理综合理解的补充作用。
- **空间关联是融合关键**：消融实验显示，移除位置嵌入会导致多模态性能显著下降，揭示空间先验在跨模态地理数据对齐中的核心地位。
- **训练高效且鲁棒**：掩码策略使预训练仅需 60 轮即收敛；模型对 OSM 数据完整性表现出较强鲁棒性，在模拟 50% 对象缺失时仍保持竞争力。

## 7. 优点
- **新颖的直接融合范式**：区别于传统的间接转换，直接处理原始异构矢量数据，保留完整的空间与语义信息。
- **空间感知的细粒度交互**：利用位置嵌入和交叉注意力，在对象-补丁级别建立精确的空间关联，突破了以往仅全局对齐的限制。
- **统一而灵活的框架**：同时输出单模态和多模态特征，既能增强通用遥感解译，又能处理复合型地理任务，适用性广。
- **实验设计与验证极为扎实**：基准全面、对比公正、消解透彻、可视化丰富，并有丰富附录提供细节。

## 8. 不足与局限
- **光谱模态单一**：当前仅支持 RGB 图像输入，未扩展到多光谱/SAR 等多传感器数据，限制了在更广泛遥感场景中的应用。
- **位置嵌入的局限性**：对线和面采用关键点采样后均值化的位置嵌入，可能造成空间细节的过平滑，影响精细几何特征的捕捉。
- **OSM 质量依赖**：虽然实验验证了对 OSM 不完整的鲁棒性，但标签质量（错误或过时的地区）在实际应用中仍可能造成性能波动。
- **对比基线的光谱对齐局限**：部分基线模型（如 CROMA、MMEarth）训练时使用了额外光谱波段，虽然在测试时通过零填充适配 RGB 输入，但并非完全公平的理想对比。

（完）
