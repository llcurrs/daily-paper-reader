---
title: Generalized Multimodal Fusion via Poisson-Nernst-Planck Equation
title_zh: 基于泊松-能斯特-普朗克方程的广义多模态融合方法
authors: "Jiayu Xiong, Jing Wang, Hengjing Xiang, Jun Xue, Chen Xu, Zhouqiang Jiang"
date: 2024-05-14
pdf: "https://openreview.net/pdf?id=XgkrXpHl5j"
tags: ["query:multi-modal"]
score: 5.0
evidence: 提出基于物理方程的广义多模态融合方法，可应用于遥感传感器融合
tldr: GMF利用泊松-能斯特-普朗克方程解决多模态融合中的特征提取、数据完整性和维度一致性挑战，从信息熵和梯度反向传播角度重新定义优化目标，为遥感等领域的多模态数据融合提供了通用框架。
source: NeurIPS-2024-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1361, \"height\": 463, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1437, \"height\": 726, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1327, \"height\": 755, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1420, \"height\": 785, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1440, \"height\": 502, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1402, \"height\": 421, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1433, \"height\": 1637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1403, \"height\": 1459, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1401, \"height\": 483, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1402, \"height\": 488, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1412, \"height\": 560, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1386, \"height\": 606, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1419, \"height\": 469, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xgkrxphl5j/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1448, \"height\": 1349, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-xgkrxphl5j/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1440, \"height\": 476, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xgkrxphl5j/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1458, \"height\": 459, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xgkrxphl5j/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1368, \"height\": 423, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xgkrxphl5j/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1439, \"height\": 149, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xgkrxphl5j/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1455, \"height\": 218, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xgkrxphl5j/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1452, \"height\": 227, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xgkrxphl5j/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1459, \"height\": 675, \"label\": \"Table\"}]"
motivation: 现有多模态融合方法在特征提取、数据完整性、维度一致性及下游任务适应性方面存在不足。
method: 提出PNP方程驱动的广义多模态融合方法，结合信息熵和梯度流重新定义优化目标，实现高效特征融合。
result: 该方法在多模态任务上表现出优越的融合性能和泛化能力，有效处理了数据完整性问题。
conclusion: GMF为多模态融合提供了新颖的物理方程视角，有望广泛应用于遥感等多传感器领域。
---

## Abstract
Previous studies have highlighted significant advancements in multimodal fusion.    Nevertheless, such methods often encounter challenges regarding the efficacy of feature extraction, data integrity, consistency of feature dimensions, and adaptability across various downstream tasks.
This paper proposes a generalized multimodal fusion method (GMF) via the Poisson-Nernst-Planck (PNP) equation, which adeptly addresses the aforementioned issues.
Theoretically, the optimization objective for traditional multimodal tasks is formulated and redefined by integrating information entropy and the flow of gradient backward step.      Leveraging these theoretical insights, the PNP equation is applied to feature fusion, rethinking multimodal features through the framework of charged particles in physics and controlling their movement through dissociation, concentration, and reconstruction.
Building on these theoretical foundations, GMF disassociated features which extracted by the unimodal feature extractor into modality-specific and modality-invariant subspaces, thereby reducing mutual information and subsequently lowering the entropy of downstream tasks. 
The identifiability of the feature's origin enables our approach to function independently as a frontend, seamlessly integrated with a simple concatenation backend, or serve as a prerequisite for other modules.
Experimental results on multiple downstream tasks show that the proposed GMF achieves performance close to the state-of-the-art (SOTA) accuracy while utilizing fewer parameters and computational resources. Furthermore, by integrating GMF with advanced fusion methods, we surpass the SOTA results.

---

## 论文详细总结（自动生成）

# 论文总结：基于泊松-能斯特-普朗克方程的广义多模态融合方法 (GMF)

## 1. 核心问题与整体含义

- **研究动机**：多模态学习旨在融合不同感官（如图像、音频、视频）的信息以提升下游任务性能。现有多模态融合方法通常基于若干不完整假设，限制了泛化能力：
  - **特征维度一致性假设**：不同模态的输出特征维度必须对齐，导致特征表达冗余或不足。
  - **数据可靠性假设**：训练和推理时模态完整，对缺失模态异常敏感。
  - **下游任务适用性单一**：匹配类任务（NMT）需模态不变特征，检测类任务（EMT）更需模态特定特征，现有方法难以同时满足。
  - **特征提取有效性受损**：融合阶段的损失函数会通过梯度反向传播影响特征提取器，导致其特征趋同、丧失模态特异性，削弱单模态表征能力。

- **整体含义**：论文提出一种广义的多模态融合方法GMF，从信息熵理论和泊松-能斯特-普朗克方程（PNP方程）出发，重新定义多模态学习的优化目标，将特征视为“带电粒子”，通过物理规律控制特征运动，实现模态不变与模态特定成分的解耦和重组。该方法旨在成为一种独立于特征提取器、下游任务和模态数量的前置融合模块，具有极低的计算开销和参数规模，同时显著提升融合鲁棒性与泛化性。

## 2. 方法论

### 核心思想
- 从**信息熵**角度，多模态学习的本质是**在不增加下游任务条件熵的前提下，最小化融合阶段的联合熵**。经典目标易使融合损失干扰特征提取，导致单模态特征退化。
- 引入**PNP方程**作为物理类比：将模态特征分解为“正电荷”（模态不变特征）和“负电荷”（模态特定特征），通过外加“电势”（损失函数）驱动粒子定向移动，实现解耦和聚集，最终在物质守恒（重建损失）约束下重构原始特征。

### 关键技术细节
- **特征解离与浓缩**：
  - 每个模态的特征通过线性映射 $P^{(j)}_{dis}$ 升维至 $n \cdot l^{(j)}$（$n>2$），称为“溶解”。
  - 在该高维空间中，以前 $b^{(j)}$ 维作为模态不变部分，剩余作为模态特定部分。
  - 不变部分通过 $P^{(j)}_{cinv}$ 投影到统一的紧凑维度 $l^*$（取所有模态中最小维度），特定部分通过 $P^{(j)}_{cspec}$ 保持原维度 $l^{(j)}$。
  - 最终输出将另一模态的不变特征与自身的特定特征拼接，形成具有明确组成的新特征。
- **重建损失引导**：利用 $P^{(j)}_{recon}$ 将输出特征映射回原始特征空间，以MSE重建损失 $L_{dis}$ 作为外部激励，迫使解离过程保留全部信息，从而保证梯度方向与下游任务一致，避免特征提取器退化。
- **理论支撑**（论文中四个定理/猜想）：
  - 定理3.1：多模态优化应满足 $\min H(Y|C(F[·]))$ 且各模态提取器同时最小化自身条件熵。
  - 定理3.2：特征存在最优维度，过高或过低均损害表征。
  - 定理3.3：线性升维再降维无法超越原始性能，但随放大倍数 $n$ 增加可无限逼近。
  - 定理3.4：在PNP方程框架下，可逆的解离-浓缩过程允许特征完全重构，对应于重建损失。
- 算法流程（见算法1-3）：输入多模态特征 $\rightarrow$ 溶解并分割为不变/特定 $\rightarrow$ 跨模态拼装 $\rightarrow$ 线性重建 $\rightarrow$ 输出融合特征与重建损失。

### 公式/算法说明（文字描述）
1. 对于模态 $j$，特征 $f^{(j)}$ 经溶解矩阵 $P_{dis}^{(j)} \in \mathbb{R}^{n l^{(j)} \times l^{(j)}}$ 得到高维 $\hat{Z}^{(j)}$。
2. 以边界 $b^{(j)} = \lfloor b \cdot n l^{(j)} \rfloor$ 分割出不变部分 $(\hat{Z}^{(j)})_{inv}$ 和特定部分 $(\hat{Z}^{(j)})_{spec}$。
3. 不变部分通过 $P_{cinv}^{(j)} \in \mathbb{R}^{l^* \times b^{(j)}}$ 浓缩到公共维度 $l^*$，特定部分通过 $P_{cspec}^{(j)} \in \mathbb{R}^{l^{(j)} \times (n l^{(j)}-b^{(j)})}$ 保持原维度。
4. 输出特征 $Z^{(j)}$ 由另一模态的不变成分与自身特定成分拼接而成。
5. 重建损失 $L_{dis} = \sum_j \| f^{(j)} - P_{recon}^{(j)} Z^{(j)} \|^2$ 约束整个解离-浓缩过程。

## 3. 实验设计

### 数据集与任务
- **VGGSound**（音频-视频事件分类，EMT）：约20万样本，评估准确率（ACC）。考察特征提取器冻结/训练两种设置，并测试单模态（缺失）性能。
- **FakeAVCeleb**（深度伪造检测，EMT）：严重类别不平衡，以AUC为主指标，ACC为辅。考察不同特征提取器（包括与MAE结合）的性能上限。
- **ActivityNet**（图像-视频检索，NMT）：评估mAP@K，采用多种输入特征维度组合（128-4096, 4096-4096, 128-128），测试不等长融合的必要性。

### 基准方法与对比
- **EMT对比**：AVoiD-DF, MISA, UAVM, DrFuse, MBT, Perceiver 等（均采用相同特征提取器 R(2+1)D-18 + ResNet-18 以公平比较），以及GMF与这些方法的组合（如G-MBT, G-Perceiver）。
- **NMT对比**：CLIP, METER, Perceiver, MAP-IVR 等，采用与AP-IVR相同的预提取特征。
- **深度伪造**：额外对比 Joint-AV, VFD, Emo-Foren, MDS 等专用方法。

### 实验设置
- 固定随机种子（1），无数据增强，无预训练参数（除VGGSound的特征提取器使用Kinetics预训练）。
- 超参数：SGD优化器，学习率0.01，batch size 64，20 epoch，学习率调度器ReduceLROnPlateau。
- 评估指标包括准确率、AUC、mAP、参数量、FLOPs、CPU推理时间。

## 4. 资源与算力

- **硬件**：所有实验在**单块 NVIDIA RTX 4090 GPU**（@2.64 GHz）上进行训练和测试；推理时间测量使用**AMD R9 5900X CPU**（@4.5 GHz）。
- **训练时长**：论文未明确报告每个实验的具体训练时间。
- **软件**：使用PyTorch，通过apex优化显存占用（优化级别O1）。
- 参数量和FLOPs在实验表格中有详细记录，例如VGGSound上GMF仅5.25M参数、0.01G FLOPs，远低于对比方法（例如Perceiver 45.05M参数、45.59G FLOPs）。

## 5. 实验数量与充分性

### 实验组数
- **VGGSound**：包括冻结/训练提取器两种主实验，每种测试单模态、双模态共6个指标，并记录参数量、FLOPs及推理时间。同时有GMF与MBT、Perceiver的组合实验。
- **ActivityNet**：三种维度组合（128-128, 4096-4096, 128-4096），对比多种NMT方法。
- **FakeAVCeleb**：对比多种特征提取器（R(2+1)D, sLSTM, ConvNeXT, MAE等）及GMF变体（GMF-MAE），并扩展至专用深度伪造检测方法。
- **理论验证实验**（附录）：CIFAR-10/100上ResNet/MobileNet/ViT验证最优维度存在；ImageNet上ResNet系列验证线性映射性能恢复；梯度流、残差分析等。
- 总计**至少10张以上的表格/图**，覆盖不同任务、模态缺失、特征维度、方法组合等多个维度。

### 充分性与公平性
- **公平性**：在VGGSound和ActivityNet上均采用**统一特征提取器**，仅替换融合模块，排除了特征提取差异的干扰。
- **充分性**：实验兼顾NMT与EMT两大类任务，考虑模态缺失鲁棒性，验证了理论声称的优势。
- **局限性**：所有实验固定随机种子且无统计误差条，可能低估结果波动；没有在不同随机种子或交叉验证下重复实验。

## 6. 主要结论与发现

- GMF以**极少的参数（约5M）和计算量（0.01G FLOPs）**，在VGGSound事件分类上达到与更大模型（如Perceiver, MBT）相当的准确率，且对**缺失模态表现极为鲁棒**（单模态性能下降微小）。
- 在ActivityNet图像-视频检索任务中，GMF在不等长融合（128-4096）下取得**超越SOTA的mAP**，证明了处理不一致特征维度的优势。
- 与MAE等先进特征提取器结合时（GMF-MAE），在FakeAVCeleb深度伪造检测上取得**近乎完美的AUC（99.97%）**，验证了方法性能上限的提升。
- 作为**前置模块**与其他融合方法组合（G-MBT, G-Perceiver）时，不仅能进一步提高性能，还可赋予它们对缺失模态的鲁棒性。
- 理论分析揭示了多模态学习应遵循的熵减约束，以及线性映射与最优维度对性能的影响，为设计简洁高效的融合模块提供了新视角。

## 7. 优点

- **理论创新**：首次将PNP物理方程引入多模态融合，结合信息熵，形成完整的理论框架（定理3.1-3.4），解释融合阶段梯度对齐和特征解耦的必要性。
- **极简实现**：GMF仅包含4个线性矩阵，无注意力、门控或复杂结构，易于实现和集成。
- **高泛化性**：独立于特征提取器和下游任务，可作为即插即用的前端模块。
- **鲁棒性突出**：显式处理模态缺失，单模态性能打幅高于其他方法。
- **计算高效**：参数量和FLOPs降低1-2个数量级，推理速度快。
- **实验说服力强**：在多类任务、多组对比中，均保持公平比较（统一特征提取器），且展示了与SOTA方法组合的增益。

## 8. 不足与局限

- **参数随维度线性增长**：GMF由全连接层构成，当输入特征维度极高时（如4096-4096），参数量会显著增加（如119M），虽仍比某些方法小，但失去了轻量优势。
- **超参数固定**：实验中统一采用倍数 $n=4$ 和边界比例 $b=1/2$，未探索这些超参数对性能的影响，可能非最优。
- **模态数量限制**：主要实验仅为双模态（音频+视频或图像+视频），虽在理论中提及可扩展至多模态，但未给出 $d\ge3$ 时的实验验证。
- **统计严谨性不足**：所有实验仅运行单次（随机种子固定为1），无误差条或多轮重复，无法评估结果的随机波动。
- **缺乏大规模或真实分布外测试**：数据集规模有限（VGGSound、FakeAVCeleb等），未在更大规模或更真实的缺失模态场景（如随机缺失率）下测试。
- **与强非线性方法结合的上限**：GMF作为前端时，后端模块依然可能引入复杂计算，且两者结合后的总体性能增益与后端选择强相关，未能完全消除后端对梯度的影响。
- **潜在偏差**：GMF的解耦效果依赖于重建损失的平衡，若重建损失过弱可能导致特征解耦不充分，但论文未给出对该超参数的敏感性分析。

（完）
