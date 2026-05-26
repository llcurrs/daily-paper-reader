---
title: "DUNIA: Pixel-Sized Embeddings via Cross-Modal Alignment for Earth Observation Applications"
title_zh: DUNIA：通过跨模态对齐实现地球观测应用的像素级嵌入
authors: "Ibrahim Fayad, Max Zimmer, Martin Schwartz, Fabian Gieseke, Philippe CIAIS, Gabriel Belouze, Sarah Brood, Aurélien de Truchis, Alexandre d'Aspremont"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=JXCiQteuOv"
tags: ["query:multi-modal"]
score: 8.0
evidence: 从图像与LiDAR中学习像素级嵌入用于地球观测任务
tldr: 针对地球观测中自监督多模态学习方法主要生成斑块级嵌入、缺乏细粒度空间信息的问题，DUNIA提出一种图像与全波形LiDAR数据的跨模态对比学习框架，通过像素级对齐生成高分辨率嵌入。在七个环境监测任务（包括冠层高度、植被覆盖度等）的零样本评估中，DUNIA显著优于现有方法，并展现出对多种模态融合的泛化能力，从而可灵活支持多种下游任务，减少了对大规模标注数据的依赖，为遥感领域多源数据融合与应用提供了新的技术路线。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 858, \"height\": 476, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1669, \"height\": 1092, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1762, \"height\": 1333, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1697, \"height\": 588, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1576, \"height\": 1390, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1580, \"height\": 1407, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1582, \"height\": 1442, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1725, \"height\": 955, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1591, \"height\": 2038, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1574, \"height\": 2002, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1577, \"height\": 2006, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jxciqteuov/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1577, \"height\": 2011, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1646, \"height\": 519, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1778, \"height\": 363, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1210, \"height\": 350, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1711, \"height\": 348, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 787, \"height\": 193, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 703, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 461, \"height\": 195, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 569, \"height\": 195, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 743, \"height\": 312, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1305, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 898, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 695, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 696, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 870, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jxciqteuov/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1022, \"height\": 171, \"label\": \"Table\"}]"
motivation: 现有自监督多模态方法产生粗粒度嵌入，限制与LiDAR等模态的精细整合。
method: 提出DUNIA，通过图像与全波形LiDAR跨模态对齐学习像素级嵌入。
result: 在七个环境监测任务的零样本评估中性能显著优于基准方法。
conclusion: 为遥感多模态融合提供了细粒度特征表示，拓展了自监督学习的应用。
---

## Abstract
Significant efforts have been directed towards adapting self-supervised multimodal learning for Earth observation applications. However, most current methods produce coarse patch-sized embeddings, limiting their effectiveness and integration with other modalities like LiDAR. To close this gap, we present DUNIA, an approach to learn pixel-sized embeddings through cross-modal alignment between images and full-waveform LiDAR data. As the model is trained in a contrastive manner, the embeddings can be directly leveraged in the context of a variety of environmental monitoring tasks in a zero-shot setting. In our experiments, we demonstrate the effectiveness of the embeddings for seven such tasks: canopy height mapping, fractional canopy cover, land cover mapping, tree species identification, plant area index, crop type classification, and per-pixel waveform-based vertical structure mapping. The results show that the embeddings, along with zero-shot classifiers, often outperform specialized supervised models, even in low-data regimes. In the fine-tuning setting, we show strong performances near or better than the state-of-the-art on five out of six tasks.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究动机**：当前地球观测领域中的自监督多模态模型（如掩码自编码器 MAE、对比模型）大多产生粗糙的“块级”嵌入，限制了与像 GEDI 全波形 LiDAR 这类高分辨率主动传感器数据的有效融合。
- **核心问题**：缺少能够在像素级别上同时理解地表水平结构（如土地覆盖、树种）与垂直结构（如冠层高度、植被密度）的统一表示，而这对精准环境监测至关重要。
- **整体含义**：DUNIA 提出一种像素级跨模态对比学习框架，使模型能够从单一卫星图像中生成具有精细空间粒度的嵌入，并可直接用于多种监测任务的零样本检索甚至波形生成，大幅减少对任务特定标注的依赖。

### 2. 提出的方法论
- **核心思想**：通过双对齐策略学习两个像素级嵌入空间——一个用于水平结构（像素‑像素对齐），另一个用于垂直结构（像素‑波形对齐），二者从同一预训练编码器出发但通过独立解码器解耦。
- **架构组成**：
  - **预训练模型**：以 Sentinel‑1 & 2 中值合成图像为输入，采用 ViT 编码器加两个分层解码器，分别输出 \\(O^V\\)（垂直用）和 \\(O^H\\)（水平用），每个解码器最高分辨率层附加邻域注意力（NA）以增强局部关系。
  - **波形模型**：基于 VQ‑VAE 对 GEDI 全波形进行编码，得到 \\(O^W\\)，与 \\(O^V\\) 对齐，并通过 RVQ 量化实现离散表示，保留语义结构。
  - **多时序图像 AE**：用 ConvLSTM 构建的 U‑Net 处理多日期 S‑1&2 图像序列，输出经时序池化后得到 \\(O^T\\)，与 \\(O^H\\) 分层对齐。
- **对齐损失**：
  - 像素‑波形对齐：使用 Zero‑CL（实例与特征去相关）损失，无需负样本，适合小批量波形样本。
  - 像素‑像素对齐：使用分层 VICReg（方差‑不变性‑协方差）损失，应用于解码器四个分辨率的输出。
- **重建损失**：MSE 分别重建波形、多时序图像和单日期图像，确保空间与结构信息保留。
- **波形生成**：在训练好的潜在空间上，以 \\(O^V\\) 为条件训练潜在扩散模型（LDM），可依据像素嵌入生成对应的完整 GEDI 波形。

### 3. 实验设计
- **预训练数据集**：
  - **Sentinel‑1 & 2**：覆盖法国本土的 10 m 分辨率合成图像（14 个波段），包括单日期中值合成（用于主模型）和三期合成（用于多时序 AE）。
  - **GEDI**：约 1900 万条经严格质量筛选的叶季全波形数据，搭配树高、冠层覆盖度、植被面积指数等标签。
- **下游任务及评估基准**：
  - **垂直结构**：冠层高度、冠层覆盖度、植物面积指数、波形检索/生成（均用 GEDI 标签）。
  - **水平结构**：树种识别（PureForest，13 类）、土地覆盖（CLC+ Backbone，11 类）、作物分类（PASTIS，18 类）。
  - 评估指标：分类用加权 F1，回归用 RMSE 与 Pearson 相关，波形相似性用 Pearson 相关。
- **对比方法**：SatMAE、DOFA、DeCUR、CROMA、AnySat，使用与 DUNIA 相同的数据与设定进行重训练或微调。
- **评估设定**：零样本（检索库 KNN 投票）和微调（仅训练最后邻域注意力层及新输出头）两种模式，重点考察低标注量下的表现。
- **实验量**：除主结果外，还包括不同检索库大小、KNN 值、微调样本量、消融实验（损失函数、共享解码器、分层 VICReg、邻域注意力、嵌入方向敏感性），以及生成波形评估、输入尺寸鲁棒性、时间稳定性、单/多模态对比等，累计数十组对照实验。

### 4. 资源与算力
- **预训练（DUNIA）**：1 张 NVIDIA A6000 (48 GB)，batch size 60，训练 250K 步，使用 Lion 优化器。
- **扩散模型**：同样在 A6000 上以 batch size 4096 训练 100K 步。
- **微调及测评**：未特别说明其他 GPU，可视为在同一设备完成，资源需求对单卡友好。

### 5. 实验数量与充分性
- 论文系统性地涵盖了 **7 个下游任务** 的零样本与微调评估，并与 **5 个同领域最新模型** 比较。
- 设置了大量 **消融实验**：验证两种对比损失在小样本场景的适用性、独立解码器与共享解码器的差异、分层 VICReg 的增益、邻域注意力与普通卷积的对比、嵌入方向（OV vs OH）对任务匹配的重要性。
- 进一步分析了 **鲁棒性与稳定性**：不同检索库规模、输入图像尺寸、单日期与中值复合图像、单/多模态数据源、跨年度泛化能力等。
- 实验设计公平，所有基线均使用相同数据按官方设定重训，细节附于附录，整体充分且涵盖面广。

### 6. 论文的主要结论与发现
- 像素级跨模态嵌入使 DUNIA 在冠层高度、冠层覆盖度、植被面积指数等垂直结构任务上 **零样本性能超越专业监督模型**。
- 在低样本微调后（如仅 5K 标注图像），DUNIA 在这些任务上 **显著领先** 于现有 Earth Observation 基础模型，并与数据需求更大的 AnySat 相当。
- 模型可以成功 **检索甚至生成完整 GEDI 波形**（相关系数 r 达 0.78），这是其他方法无法直接实现的。
- 零样本分类对土地覆盖和树种识别具有强竞争力；但对作物分类效果较差，主要因单日期复合图像无法充分捕捉物候变化。
- 分层 VICReg、独立解耦解码器与邻域注意力的设计均对最终表现有重要贡献。

### 7. 优点
- **像素级细粒度表示**：彻底解决了现有 EO 基础模型仅产生块级嵌入的局限，便于与 LiDAR 点/波形直接对齐。
- **双对齐策略与解耦设计**：显式分离水平与垂直结构理解，使同一模型可应对多样任务，支持跨模态检索。
- **跨任务零样本能力强**：仅通过检索无需任何额外训练即可获得高精度地图，尤其对小样本场景价值极大。
- **波形生成能力**：首次展示从光学图像生成 GEDI 全波形，为垂直结构精准重建提供新途径。
- **评估全面且公平**：与多类 SOTA 方法在相同数据、相同设置下比较，实验结果可重复且可信。

### 8. 不足与局限
- **时序信息利用有限**：预训练模型输入为单期中值合成图像，虽辅以多时序 AE 提供部分物候信号，但对需精细时序变化的任务（如作物分类）表现不足。
- **区域泛化未验证**：预训练数据仅覆盖法国本土，模型在其他气候带或土地覆盖类型上的表现未知，跨区域微调或预训练可能是必要的。
- **生成质量存在波动**：扩散模型生成的波形虽然相关性尚可，但与真实波形仍有一定差距，且对小样本低数据场景依赖度高。
- **输入模态固定**：目前仅适配 Sentinel‑1&2（固定 14 波段、10 m 分辨率），尚未展示对多分辨率、多传感器（如高分辨率光学、SAR 不同模式）的自适应能力。
- **未涉及动态变化检测**：实验主要评估静态属性映射，对于森林扰动、作物轮作变化等时序变化任务缺乏讨论。
- **计算成本虽可控，但非实时**：零样本推理需执行检索和加权投票，在大区域制图时会产生额外延迟（如表 H6 所示）。

（完）
