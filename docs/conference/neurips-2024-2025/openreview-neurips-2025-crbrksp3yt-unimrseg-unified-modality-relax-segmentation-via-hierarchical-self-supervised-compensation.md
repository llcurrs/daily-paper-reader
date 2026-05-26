---
title: "UniMRSeg: Unified Modality-Relax Segmentation via Hierarchical Self-Supervised Compensation"
title_zh: UniMRSeg：通过层次化自监督补偿的统一模态松弛分割
authors: "Xiaoqi Zhao, Youwei Pang, Chenyang Yu, Lihe Zhang, Huchuan Lu, Shijian Lu, Georges El Fakhri, Xiaofeng Liu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=CrBRKsP3yT"
tags: ["query:multi-modal"]
score: 7.0
evidence: 统一的模态松弛分割网络补偿缺失模态
tldr: 针对多模态医学图像分割中模态不完整导致性能下降和部署成本高的问题，提出统一模态松弛分割网络。通过层次化自监督补偿，在输入、特征和输出级别桥接完整与不完整模态间的表示差距。实验表明，单一模型即可适应多种缺失组合，且性能优于专用组合模型，为实用化多模态分割提供了高效方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-crbrksp3yt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1439, \"height\": 772, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-crbrksp3yt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 702, \"height\": 313, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-crbrksp3yt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1436, \"height\": 843, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-crbrksp3yt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1421, \"height\": 728, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-crbrksp3yt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1454, \"height\": 334, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1448, \"height\": 507, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1444, \"height\": 214, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 731, \"height\": 407, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 646, \"height\": 142, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 649, \"height\": 192, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1450, \"height\": 563, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1450, \"height\": 644, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 659, \"height\": 106, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 620, \"height\": 177, \"label\": \"Table\"}]"
motivation: 实际部署中模态缺失需多种专用模型，成本高且效率低。
method: 采用混合掩码增强与层次化自监督补偿，统一处理任意缺失模态。
result: 在医学图像分割中，单模型在多种缺失场景下达到最优性能。
conclusion: 为多模态分割的实用化部署提供了通用且鲁棒的解决方案。
---

## Abstract
Multi-modal image segmentation faces real-world deployment challenges from incomplete/corrupted modalities degrading performance. While existing methods address training-inference modality gaps via specialized per-combination models, they introduce  high deployment costs by requiring exhaustive model subsets and model-modality matching. In this work, we propose a unified modality-relax segmentation network (UniMRSeg) through hierarchical self-supervised compensation (HSSC). Our approach hierarchically bridges representation gaps between complete and incomplete modalities across input, feature and output levels. 
First, we adopt modality reconstruction with the hybrid shuffled-masking augmentation, encouraging the model to learn the intrinsic modality characteristics and generate meaningful representations for missing modalities through cross-modal fusion.  
Next, modality-invariant contrastive learning implicitly compensates the feature space distance among incomplete-complete modality pairs.  Furthermore, the proposed lightweight reverse attention adapter explicitly compensates for the weak perceptual semantics in the frozen encoder. Last, UniMRSeg is fine-tuned under the hybrid consistency constraint to ensure stable prediction under all modality combinations without large performance fluctuations. Without bells and whistles, UniMRSeg significantly outperforms the state-of-the-art methods under diverse missing modality scenarios on MRI-based brain tumor segmentation, RGB-D semantic segmentation, RGB-D/T salient object segmentation.  The code will be released at \url{https://github.com/Xiaoqi-Zhao-DLUT/UniMRSeg}.

---

## 论文详细总结（自动生成）

### 一、论文的核心问题与整体含义
- **研究动机**：现实场景中多模态图像分割常因传感器故障、临床限制等原因出现模态缺失或损坏，导致性能大幅下降。
- **现有方法局限**：主流解决思路是为每一种可能的模态组合训练专用模型，部署时需要维护庞大的模型库并进行模态匹配，资源消耗大、实用性低。
- **本文目标**：提出 **UniMRSeg**（统一模态松弛分割网络），仅使用**一组**模型参数即可覆盖任意数量的模态缺失组合，实现高效、鲁棒的分割，降低部署成本。

### 二、方法论
- **核心思想**：通过**层次化自监督补偿（HSSC）**，在输入、特征、输出三个层级逐步弥合完整模态与不完整模态之间的表示鸿沟。
- **三阶段训练流程**：
  1. **多粒度模态重建（输入层）**  
     对输入进行三种数据扰动：随机丢失模态（50%概率）、通道顺序随机打乱、空间掩码。之后让模型重建出原始完整模态图像（L1+SSIM损失），迫使编码器学习内在模态特征与跨模态互补能力。
  2. **模态不变对比学习（特征层）**  
     将同一样本的完整模态输入与随机缺失输入构成正样本对，不同样本为负样本对。采用NT-Xent对比损失在多级编码特征上拉开正负对距离，同时结合分割Dice损失联合优化，使特征具备模态不变性。
  3. **不完整模态自适应微调（输出层）**  
     冻结编码器，插入轻量**反向注意力适配器**。适配器利用3D Swin Transformer捕获跨模态互注意力，并通过反向注意力加权，显式补偿缺失模态在冷冻编码器中造成的弱语义。通过**混合一致性约束**（特征级L1损失 + 预测级Dice损失）将完整模态表示蒸馏至不完整分支，保证输出稳定。
- **关键技术细节**：
  - 反向注意力适配器：将原始编码特征与适配特征残差相加，并利用全局平均池化与Sigmoid生成注意力图，反向后强化那些完整模态能感知而缺失模态无法感知的区域。
  - 最终微调时，模型并行处理一个完整模态样本及其全部14种缺失变体（对MRI 4模态而言），仅调整解码器和适配器参数。

### 三、实验设计
- **数据集/场景**：
  - **脑肿瘤分割 (MRI)**：BraTS2020，含4种MRI模态（Flair, T1, T1ce, T2）及3个分割区域，共15种模态组合。
  - **RGB-D 显著性目标分割**：训练集NJUD + NLPR，测试集STERE。
  - **RGB-T 显著性目标分割**：训练集VT5000，测试集VT1000。
  - **RGB-D 语义分割**：SUN-RGBD（37类），室内场景。
- **对比方法**：涵盖各领域的SOTA，如脑肿瘤分割的NestedFormer、SFusion、ShaSpec、PASSION；显著性分割的SSLSOD、CAVER、PopNet、GateNet；语义分割的TokenFusion、CMX、CMXNeXt、MaskMentor。
- **评测指标**：脑肿瘤用Dice分数，显著性分割用S-measure，语义分割用IoU；同时报告各组合平均性能与标准差。

### 四、资源与算力
- **硬件**：所有实验在**一台NVIDIA A800 GPU**上完成。
- **训练设置**：使用AdamW优化器，初始学习率1e-4，权重衰减1e-5，训练300个epoch。仅提及基本数据增强（随机翻转、旋转、裁剪），未明确说明总训练时长。

### 五、实验数量与充分性
- **实验数量**：覆盖**4个不同任务**、多个数据集，对比10余种方法。针对核心模块开展了完整消融实验，包括：
  - 各组件（随机丢弃、洗牌、掩码、对比学习、分割约束、适配器、一致性约束）的逐步增益。
  - 三阶段 vs. 单阶段联合训练。
  - 反向注意力、互注意力、3D Swin Transformer的影响。
  - 不同补偿层级的组合效果（输入/特征/输出级）。
- **充分性与公平性**：实验设计系统，对比方法均采用官方代码或统一重新训练，缺失模态处理方式一致；多任务、多模态交叉验证了方法的泛化能力；消融实验有力地支撑了各模块的必要性。整体实验充分且客观。

### 六、主要结论与发现
- **性能卓越**：UniMRSeg在所有任务的**全部模态组合**上均取得最优或领先性能，平均Dice/S-measure/IoU最高，且**标准差最低**，表明在不同缺失程度下输出一致性更好。
- **层次补偿有效**：输入重建、特征对比、输出一致性三个层级协同互补，逐步提升对缺失模态的鲁棒性，最终在脑肿瘤分割上平均Dice提升超44.6%。
- **统一性**：仅用单一模型参数即可适应任意缺失情况，无需模态识别或模型切换，显著降低部署复杂度。

### 七、优点
- **创新性强**：首次将重建、对比学习、适配器压缩三阶段自监督有机统一，形成输入-特征-输出三层补偿闭环。
- **实用导向**：“一模型通吃”的思路直接解决多模态部署成本问题，对真实场景友好。
- **精巧的适配器设计**：反向注意力机制与冻结编码器的组合在极少量参数下完成有效补偿，不影响表示稳定性。
- **实验充分**：横跨医学与自然图像、2D与3D、不同模态组合，提供了丰富的对比与消融证据。

### 八、不足与局限
- **训练流程复杂**：三阶段分步训练增加了工程实施和时间成本，目前未探讨如何合并或加速。
- **缺失组合已知**：训练时模拟了全部可能的缺失组合，若模态数量继续增长，组合数爆炸可能带来训练资源压力。
- **缺少在线自适应讨论**：部署后若遇到训练中未见的缺失模式或噪声，模型是否仍鲁棒未做分析。
- **未提供训练耗时统计**：虽然硬件信息有了，但缺少每阶段的训练时间对比，不易评估实际性价比。
- **对某些下游任务的针对性**：方法主要针对分割，对回归、检测等任务的可迁移性尚未验证。

（完）
