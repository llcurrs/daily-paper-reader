---
title: "SatFlow: Generative model based framework for producing High Resolution Gap Free Remote Sensing Imagery."
title_zh: SatFlow：基于生成模型的框架，用于生成高分辨率无间隙遥感影像
authors: "Bharath Chandra Reddy Irigireddy, varaprasad bandaru"
date: 2025-01-24
pdf: "https://openreview.net/pdf?id=0ePi13LA5p"
tags: ["query:multi-modal"]
score: 9.0
evidence: 融合Landsat与MODIS遥感数据生成无间隙影像
tldr: 遥感影像常因云遮挡和卫星重访周期导致数据缺失，SatFlow利用条件流匹配生成模型，融合MODIS高时间低空间与Landsat高空间低时间分辨率影像，生成时空连续的30m无间隙地表反射率产品。实验表明，该方法在可视化质量和下游应用（如植被指数计算）中均显著优于传统时空融合方法，通过条件流匹配学习实现了从粗到精的时空数据重建，并在多个真实场景中验证了鲁棒性，为解决遥感缺失数据问题提供了新范式。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-0epi13la5p/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 841, \"height\": 683, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-0epi13la5p/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1741, \"height\": 614, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-0epi13la5p/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 845, \"height\": 845, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-0epi13la5p/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 865, \"height\": 320, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-0epi13la5p/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 898, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-0epi13la5p/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 630, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-0epi13la5p/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 912, \"height\": 299, \"label\": \"Table\"}]"
motivation: 遥感影像受云遮挡和时频不足制约，难以获得高时空分辨率无间隙数据。
method: 提出SatFlow，基于条件流匹配生成模型融合多源遥感影像生成无间隙产品。
result: 在可视化质量与下游任务中均显著优于传统时空融合方法。
conclusion: 为多源遥感数据融合提供了高效解决方案，适用于农业与环境监测。
---

## Abstract
Frequent, high-resolution remote sensing imagery is crucial for agricultural and environmental monitoring. Satellites from the Landsat collection offer detailed imagery at 30m resolution but with lower temporal frequency, whereas missions like MODIS and VIIRS provide daily coverage at coarser resolutions. Clouds and cloud shadows contaminate about 55\% of the optical remote sensing observations, posing additional challenges. To address these challenges, we present SatFlow, a generative model based framework that fuses low-resolution MODIS imagery and Landsat observations to produce frequent, high-resolution, gap-free surface reflectance imagery. Our model, trained via Conditional Flow Matching, demonstrates better performance in generating imagery with preserved structural and spectral integrity. 
Cloud imputation is treated as an image inpainting task, where the model reconstructs cloud-contaminated pixels and fills gaps caused by scan lines during inference by leveraging the learned generative processes. Experimental results demonstrate the capability of our approach in reliably imputing cloud-covered regions. This capability is crucial for downstream applications such as crop phenology tracking, environmental change detection etc.,

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **核心问题**：高频次、高分辨率的遥感影像对农业与生态环境监测至关重要，但单一传感器难以同时满足高空间分辨率与高时间重访要求。Landsat 提供 30 m 精细空间细节，但重访周期长（10–16 天）；MODIS 每日覆盖但空间分辨率粗糙（500 m）。此外，约 55% 的光学遥感观测受云及云影污染，导致严重的数据缺失。
- **整体含义**：本文提出一种基于生成模型的框架 SatFlow，通过融合低分辨率 MODIS 与 Landsat 观测，生成高分辨率、无间隙的地表反射率影像，将云填补转化为图像修复任务，为下游应用（如作物物候追踪、环境变化检测）提供连续可靠的遥感数据源。

## 2. 论文提出的方法论

- **核心思想**：利用条件流匹配（Conditional Flow Matching, CFM）这一新锐生成范式，将粗分辨率 MODIS 影像与无间隙的 Landsat 合成影像作为条件，从高斯噪声逐步生成高分辨率、无云的 Landsat 风格影像，同时通过掩膜策略修复云污染与扫描线缝隙。
- **关键技术细节**：
  - **条件流匹配建模**：定义从噪声分布 \(x(0)\sim\mathcal{N}(0,I)\) 到目标高分辨率影像 \(x(1)\) 的向量场 \(u(t)\)。通过直接回归线性化概率路径下的向量场（\(u(t)=x_1-x_0\)，概率路径为以线性插值为中心的高斯分布）来训练神经网络 \(u_\theta(x_t, t, c)\)。
  - **训练策略与条件输入**：条件 \(c\) 包括同日期的 MODIS 观测（粗分辨率）和一个由历史 Landsat 清晰像素合成的高分辨率无间隙合成影像。训练时对 MODIS 随机掩码（概率 50%）并随机选取不同的合成影像，使模型学会解耦并有效利用空间与光谱信息。训练目标是最小化预测向量场与真实向量场之间的均方误差。
  - **推理与云修复**：推理时从噪声出发沿向量场积分生成最终影像。云填补采用类似 RePaint 的迭代修复策略：已知像素强制使用 \(x^*_1 - x_0\) 而非模型预测，未知像素由模型生成，逐步融合得到无间隙影像。
  - **模型架构**：基于 U-Net 的架构，包含 ResNet 风格模块与自注意力层；时间步、日序、传感器类型等元数据通过学习嵌入在多尺度注入网络；条件影像与当前状态沿通道维拼接。
  - **整体处理流程**：预处理 MODIS 时间序列（去云插值）→ 利用模型修复 Landsat 云与扫描线缝隙 → 融合处理后的 MODIS 与修复后的 Landsat 合成影像，按需生成高分辨率无间隙产品。

## 3. 实验设计

- **数据集构建**：
  - 使用 Landsat 5–9（30 m，六个光谱波段）与 MODIS MCD43A4 产品（500 m）的 Level 2 地表反射率数据。
  - 时间范围 2000–2024，空间范围美国本土（CONUS），以 2020 年的作物数据层（CDL）分层抽样 20,000 个地点，取四个日期（云覆盖率 <10%）形成 80,000 个训练样本（256×256 像素格网）。2012 和 2015 年作为验证年排除。
  - 构建无间隙 Landsat 合成影像：对历史 Landsat 景象进行质量掩模、去云、去扫描线缝隙并镶嵌。
- **基准方法与对比对象**：
  - 传统时空融合方法：STARFM。
  - 基于条件扩散的方法（DiffCR 风格的扩散模型）。
  - 本文的 CFM 方法在不同推理步数下进行对比（1、3、5、10、50、100 步）。
  - 云填补性能评估：在干净的 Landsat 影像上合成随机云掩膜（10%、25%、50%、75% 覆盖率），对比使用与不使用 MODIS 输入的表现。
- **评价指标**：光谱信息散度（SID）、结构相似性（SSIM）、峰值信噪比（PSNR），均在六波段上计算。

## 4. 资源与算力

- **硬件**：使用两块 NVIDIA RTX A6000 GPU 进行训练。
- **批次设置**：每 GPU 批量为 16 张影像，并采用 4 步梯度累积，有效扩大批量大小。
- **训练时长**：共训练 120 epochs，但未给出具体总训练时间。
- **优化器与学习率**：AdamW，基础学习率 1e-4，余弦学习率衰减配合 6,000 步预热。

## 5. 实验数量与充分性

- **实验组数**：
  - **推理步数消融**：7 种步数设置（1、3、5、10、50、100 步）的系统对比。
  - **方法对比**：与 STARFM、扩散模型在 2500 个验证场景上对比三个指标。
  - **云覆盖率影响**：在 10%、25%、50%、75% 四种云覆盖率下评估有无 MODIS 输入的效果。
  - **定性分析**：展示质量评估掩膜错误导致伪影的案例。
- **充分性与客观性**：
  - 实验设计较为全面，覆盖了关键超参数（推理步数）、融合方法对比、以及条件信息的重要性消融。
  - 采用公认的评价指标（SSIM、PSNR）及遥感特化的 SID，客观量化性能。
  - 训练集与验证集在年份上隔离（排除 2012、2015），并基于整个美国本土多样化地类抽样，增强了泛化能力的评估可信度。
  - 不足之处：未探索不同的流匹配路径标准差 σ 的影响；扩散模型对比可能仅在一种噪声调度下进行；未提供与更近期基于 Transformer 的融合方法对比。

## 6. 论文的主要结论与发现

- CFM 在生成高分辨率 Landsat 风格影像方面显著优于 STARFM 和条件扩散模型，在 SSIM、PSNR、SID 三项指标上均取得更优结果。
- 线性化概率路径使 CFM 能够在极少的推理步数下获得可接受的性能（3 步 SSIM 即达 0.738），50 步左右基本收敛，兼顾效率与精度。
- 融合 MODIS 粗分辨率观测能大幅提升云填补质量，尤其在高云覆盖（75%）条件下，SID 和 SSIM 的提升尤为显著，证明多源融合对恶劣遮挡场景的鲁棒性。
- 提出的掩膜修复策略能够有效利用生成过程重建缺失区域，但会受制于云掩膜的错误分类，影响重建质量。

## 7. 优点

- **方法新颖**：将条件流匹配引入遥感时空融合与云修复，相比扩散模型训练更稳定、推理步数更少，具有生成模型的高保真优势。
- **模块化与可扩展性**：框架可灵活接入 MODIS、VIIRS、Sentinel-1/2 等多源数据，拓展性强。
- **训练策略巧妙**：随机掩码 MODIS 输入促使模型同时学会有 MODIS 和无 MODIS 条件下的生成，增强了实用性。
- **全面的验证**：涵盖推理步数、模型对比、多级云覆盖率消融，并配合定量与定性分析，论证扎实。

## 8. 不足与局限

- **依赖云掩膜精度**：云修复严重依赖 Landsat 产品质量评估掩膜，掩膜误分类会导致明显伪影（论文图 3 所示）。
- **MODIS 时间插值的局限**：MODIS 预处理采用插值填充短暂云隙，在长时间多云或极端事件（火灾、洪水等）时插值失真，无法反映真实地表突变。
- **历史数据限制**：引入 Sentinel‑1/2 等新数据源受限于存档年份（2015 年后），难以构建 2000 年以来的长期一致性数据集。
- **超参数探索不足**：未考察概率路径的标准差 σ 对性能的影响，扩散基线也可能未调至最优。
- **对比方法有限**：仅与 STARFM 和一种条件扩散方法对比，缺少与基于 GAN 或其他前沿时空融合模型（如 ViT 架构）的比较。
- **效率分析缺失**：未报告推断时间或模型参数量，难以判断在真实大规模应用中的计算可行性。

（完）
