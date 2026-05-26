---
title: How Do Images Align and Complement LiDAR? Towards a Harmonized Multi-modal 3D Panoptic Segmentation
title_zh: 图像如何对齐并补充LiDAR？迈向和谐的多模态三维全景分割
authors: "Yining Pan, Qiongjie Cui, Xulei Yang, Na Zhao"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=F7BOaYmWl7"
tags: ["query:multi-modal"]
score: 7.0
evidence: 融合LiDAR与相机数据进行三维分割，解决多模态传感器融合挑战
tldr: 该论文针对LiDAR数据稀疏导致远距离和小目标识别困难的问题，提出图像辅助LiDAR的多模态三维全景分割框架IAL，通过模态同步数据增强和特征融合，有效整合图像纹理信息与LiDAR几何信息，在nuScenes等数据集上取得领先性能，为多模态传感器融合提供了新思路。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-f7boaymwl7/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1741, \"height\": 511, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-f7boaymwl7/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 854, \"height\": 456, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-f7boaymwl7/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 851, \"height\": 533, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-f7boaymwl7/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1755, \"height\": 1078, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-f7boaymwl7/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 849, \"height\": 1031, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-f7boaymwl7/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1759, \"height\": 1721, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-f7boaymwl7/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 867, \"height\": 205, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-f7boaymwl7/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1779, \"height\": 579, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-f7boaymwl7/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1779, \"height\": 511, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-f7boaymwl7/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 869, \"height\": 473, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-f7boaymwl7/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 869, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-f7boaymwl7/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 869, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-f7boaymwl7/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 870, \"height\": 242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-f7boaymwl7/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1246, \"height\": 452, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-f7boaymwl7/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 609, \"height\": 232, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-f7boaymwl7/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 980, \"height\": 295, \"label\": \"Table\"}]"
motivation: LiDAR数据稀疏导致远距离和小目标识别困难，现有融合方法存在对齐和依赖后处理问题。
method: 提出IAL框架，引入模态同步数据增强和图像辅助LiDAR的特征融合模块。
result: 在nuScenes数据集上取得优于现有方法的全景分割精度。
conclusion: IAL有效融合图像与LiDAR，提升三维全景分割的鲁棒性和准确性。
---

## Abstract
LiDAR-based 3D panoptic segmentation often struggles with the inherent sparsity of data from LiDAR sensors, which makes it challenging to accurately recognize distant or small objects. Recently, a few studies have sought to overcome this challenge by integrating LiDAR inputs with camera images, leveraging the rich and dense texture information provided by the latter. While these approaches have shown promising results, they still face challenges, such as misalignment during data augmentation and the reliance on post-processing steps. To address these issues, we propose **I**mage-**A**ssists-**L**iDAR (**IAL**), a novel multi-modal 3D panoptic segmentation framework.
In IAL, we first introduce a modality-synchronized data augmentation strategy, PieAug, to ensure alignment between LiDAR and image inputs from the start. Next, we adopt a transformer decoder to directly predict panoptic segmentation results. To effectively fuse LiDAR and image features into tokens for the decoder, we design a Geometric-guided Token Fusion (GTF) module. Additionally, we leverage the complementary strengths of each modality as priors for query initialization through a Prior-based Query Generation (PQG) module, enhancing the decoder’s ability to generate accurate instance masks. Our IAL framework achieves state-of-the-art performance compared to previous multi-modal 3D panoptic segmentation methods on two widely used benchmarks. Code and models are publicly available at https://github.com/IMPL-Lab/IAL.git.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **研究背景：** 3D全景分割同时为点云中的“物体”（thing）和“背景”（stuff）类别分配语义标签并区分实例。LiDAR是获取3D场景信息的主要传感器，但其数据存在**固有稀疏性**，在检测远距离或小尺寸目标时尤为困难。
- **核心问题：** 现有方法尝试融合LiDAR点云与相机图像，利用图像的密集纹理信息弥补LiDAR的稀疏性。然而，这些多模态融合方法在**数据增强中导致两模态失配**，且预测通常依赖**低效的后处理步骤**（如聚类），限制了性能。
- **研究目标：** 设计一个**和谐的多模态3D全景分割框架**，使图像有效地对齐并补充LiDAR信息，消除后处理依赖，提升整体分割质量。

### 2. 论文提出的方法论：IAL框架

IAL（Image-Assists-LiDAR）是一个基于Transformer解码器的多模态3D全景分割框架，由三个核心模块组成：

- **模态同步增强策略（PieAug）**
  - 核心思想：对LiDAR点云和对应相机图像同步施加数据增强，确保两模态始终对齐。
  - 技术细节：
    - 将点云划分为**圆柱体素**（cylindrical voxels），并利用投影关系找到每个体素在图像上对应的像素块（bounding rectangle `gi`）。
    - 定义一个3D二值掩码 `S`，指定哪些体素将被替换。增强时，同时切割并交换LiDAR的“饼状”区域和对应的图像区域。
    - 支持两种增强形式：
      1. **实例粘贴**（Instance Pasting）：从另一场景复制实例并粘贴。
      2. **场景交换**（Scene Swapping）：沿高度或角度轴切割场景，与另一场景的对应切片交换。
    - 该策略可以泛化PolarMix、LaserMix等现有LiDAR增强方法。

- **几何引导的Token融合模块（GTF）**
  - 核心思想：利用LiDAR的精确几何信息指导图像特征与LiDAR特征的融合，形成Transformer解码器的输入令牌（tokens）。
  - 技术细节：
    - **特征对齐**：对每个圆柱体素，将其中所有物理点投影到图像平面，聚合对应图像特征得到 `˜F2D_i`，避免仅用体素中心引起的投影误差。
    - **尺度感知位置编码（SPE）**：针对圆柱体素大小随距离变化的问题，引入体素的8个角点（extreme points）表示尺度，结合中心点位置，生成统一的尺度感知位置编码 `si`，施加于LiDAR特征和图像特征。
    - **融合令牌**：将编码后的LiDAR特征与图像特征拼接得到 `Ffuse_i`。

- **基于先验的查询生成模块（PQG）**
  - 核心思想：利用LiDAR和图像的互补先验知识初始化Transformer解码器的实例查询（instance queries），而非完全依赖可学习参数。
  - 技术细节：设计三组查询
    1. **几何先验查询**：从LiDAR特征预测中心热力图，经非极大值抑制后采样，为检测**近处或大型物体**提供精确的位置提示。
    2. **纹理先验查询**：利用预训练的Grounding-DINO和SAM从图像中提取2D掩膜，提升至3D视锥并聚类（DBSCAN），为检测**远距离或小型物体**提供位置提示。
    3. **无先验查询**：使用一组可学习参数，用于感知前两种先验均未覆盖的实例。
  - 三类查询与语义查询一同输入Transformer解码器，直接预测实例掩膜和类别。

### 3. 实验设计

- **数据集：**
  - **nuScenes**：大型多模态自动驾驶数据集，含32线LiDAR和6个环视相机。训练集/验证集34,149帧，包含10个“物体”类别和6个“背景”类别。
  - **SemanticKITTI**：基于KITTI的数据集，含64线LiDAR和两个前视相机。训练/验证/测试分别有19,130/4,071/20,351帧，包含8个“物体”和11个“背景”类别。
- **评价指标：**
  - 主要指标：**全景质量（PQ）**，进一步分解为识别质量（RQ）和分割质量（SQ），并分别统计“物体”类（PQth）和“背景”类（PQst）的指标，同时报告PQ†（将背景类SQ替换为mIoU）和mIoU。
- **对比方法：**
  - LiDAR-only方法：DS-Net、EfficientLPS、Panoptic-PolarNet、Panoptic-PHNet、CFNet、CenterLPS、P3Former。
  - 多模态方法：LCPS、Panoptic-FusionNet（及其LiDAR分支）、4DFormer。
  - 将IAL分解为LiDAR分支和多模态完整版本进行对比。

### 4. 资源与算力

- 优化器：AdamW，权重衰减0.01。
- 批量大小：2。
- GPU：**4块NVIDIA A40**。
- 训练轮次：nuScenes 80 epoch，SemanticKITTI 36 epoch。
- 学习率：初始0.0008，在指定epoch衰减（nuScenes：60,75；SemanticKITTI：30,32）。
- 推理速度：完整模型约0.9 FPS，若移除2D掩膜预处理（不含Grounding-DINO/SAM）可达4.0 FPS；而LCPS为1.7 FPS。参数量：完整模型859M，轻量版81.8M。

### 5. 实验数量与充分性

- **实验丰富度：**
  - 在nuScenes的验证集和测试集、SemanticKITTI验证集上分别进行**全面的主实验对比**（Table 2-4）。
  - 设计了**多组消融实验**：
    - 模块整体消融（PieAug、GTF、PQG逐步添加，Table 5）。
    - PQG模块内部各查询类型的组合消融（Table 6）。
    - 增强策略对比消融（PolarMix、LaserMix、PieAug有无图像同步，Table 7）。
    - GTF模块内部关于特征选择和位置编码的消融（Table 8，补充材料）。
  - **定性分析**：展示了与LCPS的预测对比、LiDAR分支与完整模型的实例预测对比、以及各模块效果的消融可视化。
  - **鲁棒性分析**：测试了夜间和雨天子集的性能，证明融合模型在恶劣条件下仍有效（Table 10）。
  - **效率分析**：比较了推理速度与参数量（Table 9）。
- **公平性与客观性：** 所有对比方法均使用原论文或官方代码配置，在相同硬件上复测得速。消融实验均采用相同超参数设置，无测试时增强（TTA）。实验覆盖了主流户外多模态全景分割基准，对比方法具有代表性，实验结论可信且充分。

### 6. 论文的主要结论与发现

- **IAL框架实现了和谐的多模态融合**，通过同步增强（PieAug）、几何引导的令牌融合（GTF）和先验查询（PQG），充分发挥了图像的纹理优势与LiDAR的几何优势。
- **性能突破**：在nuScenes验证集上PQ达到**82.3%**，超过前法LCPS **+2.5%**，Panoptic-FusionNet **+5.1%**；在测试集上PQ **82.0%** 位居榜首。在SemanticKITTI上PQ**63.1%**，超LCPS 4.1%。
- **位置编码重要性**：研究表明，为查询提供精确位置先验能带来巨大增益（例如使用地面真值中心可将PQth提升10.7%）。
- **多模态鲁棒性**：即使在夜间和雨天等图像或LiDAR质量均下降的场景下，图像辅助仍带来显著提升（夜间PQ +7.3%，雨天PQ +8.1%）。
- **端到端解码器有效性**：摒弃传统后处理，利用Transformer解码器直接预测全景分割，提升了整体效率和分割质量。

### 7. 优点

- **创新的同步增强策略**：PieAug不仅解决了数据增强导致的多模态失配问题，还统一了多种现有LiDAR增强范式，提升数据多样性和模态对齐程度。
- **精巧的特征融合与查询设计**：
  - GTF通过物理点投影和尺度感知位置编码，解决了圆柱体素化带来的特征对齐与感知域差异问题。
  - PQG通过几何先验、纹理先验和无先验的组合查询，有针对性地强化了对不同难度目标（如远距小目标）的感知能力。
- **端到端的Transformer架构**：移除了繁琐的后处理步骤，使预测过程更直接，同时性能大幅提升。
- **实验全面扎实**：在两大主流基准上验证，与多种前沿方法对比，消融细致，并额外进行了恶劣天气等鲁棒性测试，分析维度全面。
- **开源可复现**：代码和模型已公开。

### 8. 不足与局限

- **计算资源要求较高**：完整模型参数量达859M，且需要4块A40 GPU训练，推理时若不裁剪预处理的Grounding-DINO/SAM，速度仅为0.9 FPS，难以直接部署于对实时性要求极高的车端。
- **纹理先验查询依赖通用模型**：提取2D掩膜使用了Grounding-DINO和SAM等大模型，这些模型并非为自动驾驶场景专门训练，可能在某些情况下产生错误先验，且带来了额外的预处理耗时和外部依赖。
- **数据集覆盖局限**：仅在nuScenes和SemanticKITTI两个自动驾驶场景数据集上验证，对室内或更复杂动态环境的泛化性未经验证。
- **极端恶劣条件下的性能仍有下降**：虽已展示一定鲁棒性，但夜间等场景的PQ（70.5%）仍显著低于正常场景（82.3%），表明极端工况下性能退化明显。
- **先验采样策略较简单**：纹理先验中的DBSCAN聚类和几何先验的NMS采样相对基础，未来可探索更精细的采样方式以进一步提升实例检测质量。

（完）
