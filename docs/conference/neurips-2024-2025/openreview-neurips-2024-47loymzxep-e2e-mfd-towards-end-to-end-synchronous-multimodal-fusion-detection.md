---
title: "E2E-MFD: Towards End-to-End Synchronous Multimodal Fusion Detection"
title_zh: E2E-MFD：面向端到端同步多模态融合检测
authors: "Jiaqing Zhang, Mingxiang Cao, Weiying Xie, Jie Lei, DaixunLi, Wenbo Huang, Yunsong Li, Xue Yang"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=47loYmzxep"
tags: ["query:multi-modal"]
score: 6.0
evidence: 端到端多模态融合检测
tldr: 该文针对自动驾驶中多模态融合检测训练复杂的问题，提出端到端同步优化算法E2E-MFD，通过单阶段训练和梯度矩阵优化实现融合与检测最优解。实验显示在公共多模态数据集上性能领先。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-47loymzxep/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1434, \"height\": 462, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-47loymzxep/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1389, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-47loymzxep/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1167, \"height\": 411, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-47loymzxep/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1311, \"height\": 428, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-47loymzxep/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1415, \"height\": 306, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-47loymzxep/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1312, \"height\": 368, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-47loymzxep/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1313, \"height\": 440, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-47loymzxep/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1299, \"height\": 368, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-47loymzxep/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1090, \"height\": 1202, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-47loymzxep/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1022, \"height\": 1098, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-47loymzxep/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1022, \"height\": 1075, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-47loymzxep/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1171, \"height\": 1098, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-47loymzxep/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1449, \"height\": 323, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-47loymzxep/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1299, \"height\": 582, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-47loymzxep/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1447, \"height\": 485, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-47loymzxep/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 800, \"height\": 179, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-47loymzxep/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 801, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-47loymzxep/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 660, \"height\": 195, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-47loymzxep/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 664, \"height\": 212, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-47loymzxep/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1209, \"height\": 213, \"label\": \"Table\"}]"
motivation: 现有多模态融合检测训练流程复杂。
method: 提出E2E-MFD，单阶段同步联合优化。
result: 在KITTI等数据集上实现最优检测。
conclusion: 端到端优化提升多模态融合检测性能。
---

## Abstract
Multimodal image fusion and object detection are crucial for autonomous driving. While current methods have advanced the fusion of texture details and semantic information, their complex training processes hinder broader applications. Addressing this challenge, we introduce E2E-MFD, a novel end-to-end algorithm for multimodal fusion detection. E2E-MFD streamlines the process, achieving high performance with a single training phase. It employs synchronous joint optimization across components to avoid suboptimal solutions associated to individual tasks. Furthermore, it implements a comprehensive optimization strategy in the gradient matrix for shared parameters, ensuring convergence to an optimal fusion detection configuration. Our extensive testing on multiple public datasets reveals E2E-MFD's superior capabilities, showcasing not only visually appealing image fusion but also impressive detection outcomes, such as a 3.9\% and  2.0\% $\text{mAP}_{50}$ increase on horizontal object detection dataset M3FD and oriented object detection dataset DroneVehicle, respectively, compared to state-of-the-art approaches.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
*   **核心问题**：现有的多模态融合检测（MFD）方法通常采用**多阶段、级联的训练范式**（先训练融合网络，再训练检测网络，或者逐步联合训练），过程繁琐、效率低下，且容易陷入**单个任务的局部最优解**，难以获得能同时出色完成图像融合与目标检测的统一模型。
*   **整体含义**：本文旨在提出一种**端到端的同步联合学习框架**（E2E-MFD），将图像融合和目标检测整合为**单阶段训练过程**，通过同步优化和梯度对齐策略，使两个任务相互促进，最终在生成高质量融合图像的同时，显著提升目标检测精度。

### 2. 论文提出的方法论
*   **核心思想**：设计并行架构，将图像融合子网络与目标检测子网络进行**同步联合优化**，并引入**梯度矩阵任务对齐（GMTA）** 技术来消除两个任务在共享参数上的优化冲突。
*   **关键技术细节**：
    *   **对象-区域-像素系统发生树（ORPPT）**：作为融合网络，模拟人类从粗到细的视觉感知过程。它包含一个**像素特征挖掘模块（PFMM）** 和多个**区域特征精炼模块（RFRM）**。通过引入可学习的区域提示，将特征映射为区域掩码，从而提取多粒度的区域表示，并与像素级特征融合，重建出细节丰富且目标突出的融合图像。
    *   **粗到细扩散过程（CFDP）**：作为检测网络，基于扩散模型（DiffusionDet）构建检测头。它将目标检测建模为从噪声边界框逐步去噪恢复出真实边界框的过程，能够辅助融合网络更好地关注目标区域。
    *   **梯度矩阵任务对齐（GMTA）**：针对共享参数，计算融合任务和检测任务的梯度矩阵。通过**条件数**衡量梯度系统的稳定性（理想条件数为1，即梯度正交且等长）。GMTA通过对梯度矩阵进行奇异值分解（SVD）并重新缩放，强制使其满足最优条件数，从而**消除任务间的梯度支配和冲突**，确保共享参数收敛到对两个任务均有利的配置。
    *   **损失函数**：融合损失由结构相似性损失（$L_{SSIM}$）、目标感知像素损失（$L_{pixel}$，区分目标和背景区域）和多尺度梯度损失（$L_{grad}$）组成。总损失为融合损失与检测损失（$L_d$）的加权和。

### 3. 实验设计
*   **数据集与场景**：
    *   **图像融合**：在 **TNO**、**RoadScene** 和 **M3FD** 数据集上评估。
    *   **目标检测**：在 **M3FD**（水平框）和 **DroneVehicle**（旋转框，无人机视角）数据集上评估。
    *   场景覆盖了自动驾驶道路交通、夜间监控、无人机航拍等。
*   **Benchmark与对比方法**：
    *   **纯融合方法**：DIDFuse, U2Fusion, PIAFusion, SwinFusion, CDDFuse。
    *   **融合-检测联合方法**：Tardal, MetaFusion。
    *   **端到端目标检测方法**：CFT, ICAFusion。
    *   **单模态检测器**：以可见光（RGB）或红外（IR）图像单独作为输入，使用YOLOv5s、LSKNet等检测器。
    *   评价指标包括融合质量指标（EN, MI, VIF）和检测精度指标（$\text{mAP}_{50}$, $\text{mAP}_{50:95}$）。

### 4. 资源与算力
*   论文明确提到所有实验均使用 **1块 NVIDIA GeForce RTX 3090 GPU** 完成。
*   在M3FD数据集上，E2E-MFD完成训练的时间为 **2小时50分32秒**，显著快于其他多阶段训练方法（如MetaFusion需6小时47分）。模型推理生成一幅融合图像耗时0.014秒。

### 5. 实验数量与充分性
*   **实验数量较多**：包括4个数据集上的多组主实验对比、多组消融实验（GMTA有效性、不同MTL方法对比、GMTA迭代频率、ORPPT分支数量、CFDP模块及提案框数量），以及梯度矩阵可视化分析。
*   **实验充分性与客观性**：
    *   对比方法全面，涵盖了纯融合、联合学习、端到端检测和单模态基准等多个类别。
    *   消融实验设计细致，逐步验证了每个提出模块的有效性，并分析了超参数（如梯度对齐频率、分支数）的影响。
    *   实验是公平的，在统一的硬件环境下，使用公开数据集和标准评价指标，并在检测任务中固定了多种下游检测器（YOLOv5s、LSKNet）进行公平对比，验证了融合图像质量的普适性。

### 6. 论文的主要结论与发现
*   E2E-MFD能够在一个**单阶段、端到端的训练流程**中，同时高效地完成图像融合和目标检测任务，训练时间大幅缩短。
*   提出的**GMTA技术**能够有效缓解多任务学习中的梯度支配和冲突问题，使共享参数收敛到更优的配置，直接提升了融合和检测两个任务的性能。
*   **ORPPT和CFDP**的协同设计，让融合网络能捕获从像素到区域的精细细节，同时感知目标语义，生成了视觉上更清晰、检测上更友好的融合图像。
*   在多个公开数据集上，E2E-MFD在**图像融合质量指标和检测精度上均超越了现有最先进方法**（如在M3FD上$\text{mAP}_{50}$提升3.9%，DroneVehicle上提升2.0%）。

### 7. 优点
*   **高效的训练范式**：将复杂的多阶段训练简化为单阶段端到端同步优化，显著提升了训练效率。
*   **创新的梯度对齐方法**：GMTA从数值优化稳定性（条件数）的角度，巧妙地解决了异构任务间的梯度冲突问题，具有较强的理论启发性。
*   **多粒度融合结构**：ORPPT模仿人类视觉感知，从对象、区域到像素进行多层级特征建模，设计精巧且与任务需求高度契合。
*   **极强的实验验证**：实验覆盖4个数据集、多种任务（水平/旋转框检测）、多组消融和可视化分析，结论扎实且令人信服。

### 8. 不足与局限
*   **模态局限性**：模型仅在**可见光-红外**这两种模态上进行了验证。论文承认，受限于社区数据集资源，尚未在其他多模态组合（如深度图、高光谱等）上验证方法的泛化能力。
*   **潜在的应用偏差**：模型对目标区域的感知依赖于数据集提供的真实边界框，当应用于包含有害或敏感内容的场景时，其性能可能受到影响，但这主要源于数据本身而非模型。
*   **扩散模型的推理开销**：虽然训练效率高，但基于扩散过程的检测头在推理时需迭代去噪，其推断速度（0.014秒/图）相比一些单阶段检测器可能不占优势，不过论文未深入讨论此点。

（完）
