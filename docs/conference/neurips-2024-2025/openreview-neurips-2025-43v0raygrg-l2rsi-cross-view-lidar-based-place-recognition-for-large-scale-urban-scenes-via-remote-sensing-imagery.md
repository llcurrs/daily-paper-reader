---
title: "L2RSI: Cross-view LiDAR-based Place Recognition for Large-scale Urban Scenes via Remote Sensing Imagery"
title_zh: L2RSI：基于遥感影像的大规模城市场景跨视角激光雷达地点识别
authors: "Ziwei Shi, Xiaoran Zhang, Wenjing Xu, Yan Xia, Yu Zang, Siqi Shen, Cheng Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=43v0RAyGrg"
tags: ["query:multi-modal"]
score: 7.0
evidence: 激光雷达与遥感影像跨模态对齐用于地点识别
tldr: 为解决激光雷达地点识别依赖昂贵3D地图的问题，提出L2RSI方法，利用遥感影像作为地图代理，学习点云与遥感影像的跨模态特征对齐。构建大规模城市场景数据集LiRSI-XA，验证了方法的有效性，降低了大范围定位成本。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-43v0raygrg/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1239, \"height\": 388, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-43v0raygrg/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1231, \"height\": 374, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-43v0raygrg/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 794, \"height\": 348, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-43v0raygrg/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1286, \"height\": 559, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-43v0raygrg/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 646, \"height\": 254, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-43v0raygrg/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 646, \"height\": 254, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-43v0raygrg/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1445, \"height\": 596, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-43v0raygrg/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1446, \"height\": 1514, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-43v0raygrg/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 373, \"height\": 355, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-43v0raygrg/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1382, \"height\": 187, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-43v0raygrg/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1444, \"height\": 342, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-43v0raygrg/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 712, \"height\": 222, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-43v0raygrg/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1331, \"height\": 126, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-43v0raygrg/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1263, \"height\": 226, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-43v0raygrg/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 792, \"height\": 234, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-43v0raygrg/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1032, \"height\": 383, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-43v0raygrg/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1416, \"height\": 163, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-43v0raygrg/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1442, \"height\": 234, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-43v0raygrg/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1400, \"height\": 298, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-43v0raygrg/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1223, \"height\": 126, \"label\": \"Table\"}]"
motivation: 激光雷达地点识别依赖高成本3D地图，限制大规模应用。
method: 通过跨视角跨模态学习，将激光雷达点云与遥感影像对齐。
result: 在LiRSI-XA数据集上实现了高效准确的跨模态地点识别。
conclusion: L2RSI为低成本大范围定位提供了一种新途径。
---

## Abstract
We tackle the challenge of LiDAR-based place recognition, which traditionally depends on costly and time-consuming prior 3D maps. 
To overcome this, we first construct LiRSI-XA dataset, which encompasses approximately $110,000$ remote sensing submaps and $13,000$ LiDAR point cloud submaps captured in urban scenes, and propose a novel method, L2RSI, for cross-view LiDAR place recognition using high-resolution Remote Sensing Imagery. This approach enables large-scale localization capabilities at a reduced cost by leveraging readily available overhead images as map proxies. L2RSI addresses the dual challenges of cross-view and cross-modal place recognition by learning feature alignment between point cloud submaps and remote sensing submaps in the semantic domain. Additionally, we introduce a novel probability propagation method based on particle estimation to refine position predictions, effectively leveraging temporal and spatial information. This approach enables large-scale retrieval and cross-scene generalization without fine-tuning. Extensive experiments on LiRSI-XA demonstrate that, within a $100km^2$ retrieval range, L2RSI accurately localizes $83.27\%$ of point cloud submaps within a $30m$ radius for top-$1$ retrieved location. Our project page is publicly available at https://shizw695.github.io/L2RSI/.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义
- **研究背景**：激光雷达（LiDAR）地点识别是自动驾驶与机器人导航的关键技术，能在 GPS 信号弱或缺失时实现全局定位。但现有方法严重依赖预先构建的高精度 3D 地图，地图的获取与维护成本高、周期长，限制了大规模部署。
- **核心问题**：如何摆脱对昂贵 3D 先验地图的依赖，在超大范围（如 100 km² 以上）城市环境中实现高效、准确的激光雷达地点识别。
- **整体思路**：利用覆盖广、成本低、更新快的高分辨率遥感影像（RSI）作为地图代理，通过跨视角、跨模态的特征对齐，实现从车载激光雷达点云到遥感影像库的直接检索定位。同时引入时空序列信息，解决单次查询易产生歧义的问题。

## 2. 方法论
- **核心思想**：将激光雷达点云与遥感影像统一到语义域，通过语义对比学习消除模态与视角差异；并设计时空粒子估计（STPE）利用连续查询的时空约束优化定位结果。
- **关键技术细节**：
  - **数据预处理**：
    - 对遥感影像进行语义分割（提取道路、植被、建筑等），并均匀滑动分割成子图，滤除远离道路的子图，构建语义数据库。
    - 对激光雷达短序列扫描进行配准生成子图，同样进行语义分割（去除强度特征，仅保留相同语义类别），将点云压缩为鸟瞰图（BEV），并利用磁力计提供的方向旋转至北向朝上。
  - **语义对比学习网络**：
    - 使用双分支权重共享的网络（编码器 → GeM池化 → 全连接层）提取全局描述子。
    - 编码器可选用预训练基础模型（默认 MAE-B），在两个模态间共享。
    - 损失函数：对称 InfoNCE 损失，在一个批次内最大化正样本对相似度，最小化负样本对相似度。
  - **时空粒子估计（STPE）**：
    - 将每次查询的 Top-K 检索结果视为粒子，利用连续帧间的相对位姿（由 FastGICP 估计，磁力计校正方向）将过去若干帧的粒子传播到当前时刻。
    - 每帧的粒子聚类为多个高斯分布（GMM），传播后按时间窗口聚合，构建当前时刻位置的概率密度函数，据此对数据库中的候选子图重新排序。
    - 通过采样率 λ 平衡精度与效率，默认 L=50 帧、K=30 个粒子、λ=30%。
- **公式流程**（文字说明）：
  - 位置概率密度建模为高斯混合模型：\( P(x,y) = \sum_{m=1}^M A_m \cdot \exp\left( -\frac{(x-\mu_{x_m})^2}{2\sigma_{x_m}^2} - \frac{(y-\mu_{y_m})^2}{2\sigma_{y_m}^2} \right) \)。
  - 传播后叠加：\( \tilde{P}_j(x,y) \) 为第 j 帧传播后的分布，最终 \( P_t(x,y) = \frac{1}{L} \sum_{j=t-L+1}^t \tilde{P}_j(x,y) \)。
  - 将概率密度分配给数据库中的子图中心区域，得分重排。

## 3. 实验设计
- **数据集**：
  - **LiRSI‑XA**：自建数据集，覆盖厦门翔安区约 100 km²，含约 11 万张遥感子图、1.3 万张点云子图，训练与测试轨迹分离。测试子集按数据库大小分为 S（4 km²）、M（9 km²）、L（16 km²）、G（100 km²）。
  - **LiRSI‑Oxford**：基于 Oxford Radar RobotCar 数据集补充对应遥感影像（约 2.8 km²），完全用于跨场景泛化测试（不微调）。
  - 另扩增了 **LiRSI‑Kitti360** 用于更全面对比。
- **评价指标**：Recall@1 和 Recall@10，正确检索定义为检索结果中心与查询子图中心欧氏距离 < 30 m。
- **对比方法**：
  - 跨模态 3D 地点识别：LIP‑Loc。
  - 跨视角 2D 地点识别：GeoDTR、Sample4Geo、FRGeo。
  - 重排策略：SuperGlobal，以及经典粒子滤波（PF）。
  - 消融实验中还包括不同语义分割策略、不同编码器、不同 STPE 参数等。

## 4. 资源与算力
- **硬件**：所有实验在单块 NVIDIA GTX 3090 GPU（24 GB 显存）上完成。
- **训练配置**：PyTorch 实现，Adam 优化器，学习率 5e-5，批次大小 64，训练 100 个 epoch，使用 StepLR 学习率衰减（每 1000 步乘 0.95）。
- **运行时**：全局描述子提取约 5.8 ms，STPE 在 λ=30% 时额外耗时约 31.7 ms，总时间约 37.5 ms，可实时运行（<100 ms）。

## 5. 实验数量与充分性
- **主要对比实验**：在 LiRSI‑XA 的 4 个数据库规模、LiRSI‑Oxford 两条轨迹、LiRSI‑Kitti360 三个序列上，与 4 种现有方法 + 两种后处理策略对比，共数百个条目。
- **消融实验**：
  - 验证语义信息、STPE、方向的必要性（3 项组合消融）。
  - 分析 STPE 关键参数 L、K、λ 对精度和速度的影响（多组实验）。
  - 探究运动模型失效时的鲁棒性（引入不同强度的偏航和位移噪声）。
  - 评估不同编码器（VGG、ResNet、ConvNeXt、DINOv2、MAE）的影响。
  - 验证 STPE 对现有方法的兼容性（4 种基线 + STPE 提升效果）。
  - 经典粒子滤波与 STPE 的详细对比。
- **充分性与客观性**：实验覆盖多个数据集、多类基线、多维度消融，对比公平（所有方法使用相同预处理语义图像，参数按官方设定）。随机种子固定，主要结果稳定。对噪声与泛化能力进行了量化分析，整体实验设计较为全面。

## 6. 主要结论与发现
- L2RSI 是首个在 100 km² 以上城市场景下，利用遥感影像实现跨视角激光雷达地点识别的方法，打破了依赖 3D 先验地图的限制。
- 语义域对齐可有效弥合点云与遥感影像之间的内容、风格差异，是泛化能力的关键。
- 提出的 STPE 通过高斯混合模型聚合时空信息，显著优于粒子滤波和单帧检索，大幅提升召回率并抑制误匹配。
- 方法在跨场景（Oxford 数据集）上展现出令人鼓舞的泛化能力，Recall@1 超过 40%，但距离实际部署仍有提升空间。

## 7. 优点
- **创新性**：首次将高分辨率遥感影像引入大规模激光雷达地点识别任务，并构建相应数据集，填补了相关空白。
- **方法简洁高效**：通过语义统一和对比学习实现跨模态对齐，训练稳定；STPE 融合时空信息轻量且有效，实时性有保障。
- **泛化性突出**：纯语义域对齐使模型在不经微调的情况下对陌生城市环境仍有较高识别能力。
- **可解释性与兼容性**：方法基于直观的语义对应，STPE 可方便嵌入现有检索式框架中。
- **实验扎实**：多维度的实验对比、参数敏感性分析与鲁棒性测试，说服力强。

## 8. 不足与局限
- **依赖外部方向传感器**：当前系统需要磁力计提供大致准确的朝向（误差容忍约 10° 内），若磁力计失效或严重干扰，性能可能显著退化。
- **场景适用性受限**：主要针对城市道路场景设计，语义稀疏的乡村、旷野等区域效果难以保证；密集树冠遮挡或严重时序变化（如遥感图像与 LiDAR 采集间隔三年以上）会导致语义不一致，影响识别。
- **运动模型噪声敏感**：STPE 依赖相对位姿估计的精度，当动态物体干扰导致 FastGICP 误差增大时，定位性能会下降（但本文已验证一定范围的鲁棒性）。
- **开源与隐私考量**：遥感影像涉及敏感地理信息，数据开放可能受限，对复现与推广存在一定阻碍。
- **跨场景性能仍有提升空间**：在 Oxford 数据集上最高 Recall@1 约 43%，距离大规模实用尚有差距。

（完）
