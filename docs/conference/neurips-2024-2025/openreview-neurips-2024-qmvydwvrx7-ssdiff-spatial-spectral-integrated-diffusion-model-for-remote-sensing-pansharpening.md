---
title: "SSDiff: Spatial-spectral Integrated Diffusion Model for Remote Sensing Pansharpening"
title_zh: SSDiff：用于遥感图像锐化的空间-光谱集成扩散模型
authors: "Yu Zhong, Xiao Wu, Liang-Jian Deng, Zihan Cao, Hong-Xia Dou"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=QMVydwvrx7"
tags: ["query:multi-modal"]
score: 9.0
evidence: 全色锐化融合多模态遥感图像的空间与光谱信息
tldr: 针对遥感图像全色锐化任务，提出空间-光谱集成扩散模型SSDiff，从子空间分解角度将锐化视为空间与光谱成分的融合。该模型利用空间与光谱分支分别学习细节与特征，并通过子空间分解实现高效融合。实验表明其能生成高质量高分辨率多光谱图像，为遥感图像融合提供新范式。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-qmvydwvrx7/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1432, \"height\": 428, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qmvydwvrx7/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 542, \"height\": 384, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qmvydwvrx7/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1459, \"height\": 591, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qmvydwvrx7/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1066, \"height\": 531, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qmvydwvrx7/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1455, \"height\": 727, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qmvydwvrx7/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1026, \"height\": 747, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qmvydwvrx7/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1456, \"height\": 846, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qmvydwvrx7/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1457, \"height\": 975, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-qmvydwvrx7/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1442, \"height\": 1052, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qmvydwvrx7/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1235, \"height\": 340, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qmvydwvrx7/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1002, \"height\": 170, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qmvydwvrx7/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1193, \"height\": 457, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qmvydwvrx7/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1059, \"height\": 280, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qmvydwvrx7/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1446, \"height\": 491, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qmvydwvrx7/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 810, \"height\": 138, \"label\": \"Table\"}]"
motivation: 现有全色锐化方法难以同时保留空间细节与光谱保真度。
method: 提出SSDiff，从子空间分解出发，用空间和光谱分支学习并融合特征。
result: SSDiff在生成高分辨率多光谱图像上取得优越性能。
conclusion: SSDiff为遥感图像融合提供了一种新颖有效的扩散模型方法。
---

## Abstract
Pansharpening is a significant image fusion technique that merges the spatial content and spectral characteristics of remote sensing images to generate high-resolution multispectral images. Recently, denoising diffusion probabilistic models have been gradually applied to visual tasks, enhancing controllable image generation through low-rank adaptation (LoRA). In this paper, we introduce a spatial-spectral integrated diffusion model for the remote sensing pansharpening task, called SSDiff, which considers the pansharpening process as the fusion process of spatial and spectral components from the perspective of subspace decomposition. Specifically, SSDiff utilizes spatial and spectral branches to learn spatial details and spectral features separately, then employs a designed alternating projection fusion module (APFM) to accomplish the fusion. Furthermore, we propose a frequency modulation inter-branch module (FMIM) to modulate the frequency distribution between branches. The two components of SSDiff can perform favorably against the APFM when utilizing a LoRA-like branch-wise alternative fine-tuning method. It refines SSDiff to capture component-discriminating features more sufficiently. Finally, extensive experiments on four commonly used datasets, i.e., WorldView-3, WorldView-2, GaoFen-2, and QuickBird, demonstrate the superiority of SSDiff both visually and quantitatively. The code is available at https://github.com/Z-ypnos/SSdiff_main.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究背景**：全色锐化（Pansharpening）是将高空间分辨率的全色（PAN）图像与低空间分辨率的多光谱（MS）图像融合，生成高分辨率多光谱图像（HrMSI）的关键技术。
- **现有问题**：传统深度学习方法常将 PAN 和 MS 图像耦合输入，忽视了两者深层信息的差异性；双分支网络虽然能区分学习，但结构复杂难以局部微调；基于扩散模型的方法尚未针对全色锐化任务设计区分性特征学习机制。
- **整体含义**：本文从子空间分解视角出发，将全色锐化定义为空间成分与光谱成分的融合过程，提出空间-光谱集成扩散模型 SSDiff，旨在更充分地捕获和融合空间细节与光谱特征，提升融合质量。

### 2. 方法论：核心思想、关键技术细节
- **整体架构**：
  - 采用空间分支与光谱分支分别学习 PAN 的空间细节和 LrMSI（上采样后的低分辨率多光谱图像）的光谱特征。
  - 每个分支包含编码器-解码器结构，空间分支使用 ResNet 块，光谱分支通过 MLP 和交替投影融合模块（APFM）进行信息融合。
- **交替投影融合模块（APFM）**：
  - 基于线性代数中的向量投影（Lemma 1）和子空间分解（Definition 1），将自注意力机制推广为空间域与光谱域之间的交替投影。
  - 公式化表示为：空间域特征投影为 `Tspa = Softmax((Ta Tb^T)/√S') Tc^T`，光谱域特征投影为 `Tspe = Softmax((Tc Td^T)/√((S')^3/HW)) Ta^T`，再通过元素乘融合为 `Tf us = Tspa ⊙ Tspe`。
- **频率调制跨分支模块（FMIM）**：
  - 使用傅里叶滤波器提取空间分支的高频信息，注入光谱分支时对部分通道乘以常数（1.2, 1.4, 1.6），以缓解低频信息过重问题，提升去噪性能。
- **LoRA 式分支交替微调（L-BAF）**：
  - 在 APFM 投影过程中，通过截断梯度传播，交替更新空间分支和光谱分支参数，实现类似 LoRA 的低秩适应，避免过拟合并捕获更区分性特征。
- **训练目标**：将扩散模型的预测目标从噪声 ϵ 改为干净图像 x0，损失函数为 `Lsimple = E[||x0 − xθ(xt, c, t)||1]`，并将预测对象改为 HrMSI 与上采样 LrMSI 的差值。

### 3. 实验设计
- **数据集**：
  - WorldView-3（8波段）、WorldView-2（8波段）、GaoFen-2（4波段）、QuickBird（4波段）。
  - 按照 Wald 协议构建降分辨率数据集（有 GT）和全分辨率数据集（无 GT）。
- **对比方法**：
  - 传统方法：BDSD-PC、MTF-GLP-FS、BT-H。
  - 深度学习方法：PNN、DiCNN、MSDCNN、FusionNet、CTINN、LAGConv、MMNet、DCFNet、PanDiff（同为扩散模型）。
- **评估指标**：
  - 降分辨率：SAM、ERGAS、Q2n/Q4、SCC。
  - 全分辨率：Dλ、Ds、HQNR。
- **训练与测试细节**：
  - 训练迭代次数：WV3 150k、GF2 100k、QB 200k，微调节点 30k 迭代。
  - 扩散过程：训练时间步 1000，采样时间步 10。
  - 优化器：AdamW，初始学习率 0.001，微调节点 0.0001。

### 4. 资源与算力
- **硬件配置**：Intel i7-12700K CPU，2 块 NVIDIA RTX 3090 GPU（24 GB 显存），128 GB 内存。
- **软件环境**：PyTorch 1.7.0，Python 3.8.5，Linux 系统。
- **单图推理时长**：10 个采样步下约 7.417 秒。
- **训练时长**：论文未明确给出总训练时间，但提供了迭代次数（如 WV3 150k），可估算所需计算量。

### 5. 实验数量与充分性
- **主要实验组数**：
  - 4 个数据集（WV3、WV2、GF2、QB）上的降分辨率和全分辨率结果（表 1、表 6、图 7、图 8）。
  - 消融实验：解耦分支有效性（6 种变体）、FMIM 有无、微调策略（4 种模式）。
  - 泛化实验：用 WV3 训练的模型测试 WV2（表 4）。
  - 效率对比：各方法单张推理时间（表 7）。
- **充分性与公平性**：
  - 实验涵盖主流卫星数据和多种 SOTA 方法，指标全面，消融对照丰富；所有 DL 方法在同一 GPU 环境下复现，公平性较好。
  - 但缺少统计显著性检验（如标准差或置信区间），且未详细报告训练耗时。

### 6. 主要结论与发现
- SSDiff 在四个数据集上均取得 SOTA 性能，尤其在 SAM、ERGAS、HQNR 等指标上优势明显，误差图显示融合结果更贴近真值。
- 空间-光谱分支解耦设计与 APFM 有效捕获了区分性特征，优于单纯拼接或 LoRA 方式。
- FMIM 通过频率调制能进一步提升模型性能。
- L-BAF 交替微调方法比全参数微调或仅微调单分支效果更好，能避免过拟合。
- SSDiff 在跨数据集泛化测试中表现最佳，说明其泛化能力强。

### 7. 优点
- **新颖的理论支撑**：从向量投影和子空间分解出发，将自注意力推广为交替投影，理论解释清晰。
- **有效的结构设计**：双分支解耦学习、APFM 融合、频率调制模块，各组件通过消融验证均有贡献。
- **精细的微调策略**：L-BAF 在无额外参数的前提下提升性能，类似 LoRA 思想。
- **全面的实验验证**：涵盖多个数据集、多种对比方法和多角度消融实验，结果令人信服。

### 8. 不足与局限
- **推理效率**：扩散模型采样步数较多，单张推理约 7.4 秒，远慢于 CNN 方法（如 DCFNet 0.55 秒），可能限制实时应用。
- **超参数敏感**：FMIM 引入了不同层级的通道乘系数（1.2,1.4,1.6），增加调参难度，且未讨论其敏感性。
- **实验透明度**：未提供训练总时长、标准差误差棒或多次运行统计检验，仅给出均值，可重复性细节待补充。
- **适用范围**：主要针对四波段/八波段多光谱图像，向高光谱或更多源融合扩展的验证缺失。
- **潜在偏差**：训练和测试均采用模拟降质数据，与真实卫星成像物理模型的 gap 可能未充分讨论。

（完）
