---
title: Revisiting Generative Infrared and Visible Image Fusion Based on Human Cognitive Laws
title_zh: 基于人类认知规律的生成式红外与可见光图像融合再思考
authors: "Lin Guo, Xiaoqing Luo, Wei Xie, Zhancheng Zhang, Hui Li, Rui Wang, Zhenhua Feng, Xiaoning Song"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=wvcYIEaD5X"
tags: ["query:multi-modal"]
score: 4.0
evidence: 提出生成式红外与可见光图像融合方法
tldr: 现有红外与可见光图像融合方法面临模态信息平衡困境且缺乏可解释性。HCLFuse受人类认知规律启发，提出多尺度掩码与信息映射量化理论，增强生成能力，在通用数据集上提升了融合质量与一致性，但未在遥感图像上验证，对遥感多传感器融合有一定借鉴意义。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-wvcyiead5x/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1433, \"height\": 406, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wvcyiead5x/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1449, \"height\": 591, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wvcyiead5x/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1453, \"height\": 1003, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wvcyiead5x/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1452, \"height\": 1001, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wvcyiead5x/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1446, \"height\": 207, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wvcyiead5x/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1452, \"height\": 990, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wvcyiead5x/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1452, \"height\": 1038, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wvcyiead5x/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1452, \"height\": 1003, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wvcyiead5x/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1452, \"height\": 1002, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wvcyiead5x/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1452, \"height\": 1002, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wvcyiead5x/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1451, \"height\": 1002, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wvcyiead5x/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1440, \"height\": 561, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-wvcyiead5x/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1457, \"height\": 716, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wvcyiead5x/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1451, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wvcyiead5x/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1458, \"height\": 717, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wvcyiead5x/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1458, \"height\": 714, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wvcyiead5x/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1458, \"height\": 716, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wvcyiead5x/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1454, \"height\": 849, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wvcyiead5x/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1455, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wvcyiead5x/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1454, \"height\": 181, \"label\": \"Table\"}]"
motivation: 现有融合方法难以平衡模态信息，生成能力有限且缺乏可解释性。
method: 提出HCLFuse，引入多尺度掩码和信息映射量化理论，模仿人类认知选择模态信息。
result: 在公开数据集上，HCLFuse融合结果更自然、信息保留更完整，但未在遥感数据上测试。
conclusion: 为多模态图像融合提供了可解释的生成范式，可潜在应用于遥感多传感器融合任务。
---

## Abstract
Existing infrared and visible image fusion methods often face the dilemma of balancing modal information. Generative fusion methods reconstruct fused images by learning from data distributions, but their generative capabilities remain limited. Moreover, the lack of interpretability in modal information selection further affects the reliability and consistency of fusion results in complex scenarios. This manuscript revisits the essence of generative image fusion under the inspiration of human cognitive laws and proposes a novel infrared and visible image fusion method, termed HCLFuse. First, HCLFuse investigates the quantification theory of information mapping in unsupervised fusion networks, which leads to the design of a multi-scale mask-regulated variational bottleneck encoder. This encoder applies posterior probability modeling and information decomposition to extract accurate and concise low-level modal information, thereby supporting the generation of high-fidelity structural details. Furthermore, the probabilistic generative capability of the diffusion model is integrated with physical laws, forming a time-varying physical guidance mechanism that adaptively regulates the generation process at different stages, thereby enhancing the ability of the model to perceive the intrinsic structure of data and reducing dependence on data quality. Experimental results show that the proposed method achieves state-of-the-art fusion performance in qualitative and quantitative evaluations across multiple datasets and significantly improves semantic segmentation metrics. This fully demonstrates the advantages of this generative image fusion method, drawing inspiration from human cognition, in enhancing structural consistency and detail quality.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：现有红外与可见光图像融合方法存在三大痛点——生成能力有限（难以充分挖掘数据分布）、模态信息选择缺乏可解释性（导致复杂场景下融合结果不可靠）、对数据质量强依赖（分布偏移或噪声干扰下鲁棒性差）。
- **整体含义**：本文受人类认知规律（选择性注意、物理定律）启发，重新审视生成式图像融合的本质。通过模仿人类将经验数据与抽象推理、领域知识相结合的方式，提出一种可解释、鲁棒的生成融合框架 HCLFuse，力图突破现有方法的局限性，并为多模态融合提供新的建模范式。

### 2. 论文提出的方法论
- **核心思想**：将无监督信息融合建模为信息压缩与保留的权衡问题。设计“多尺度掩码变分瓶颈编码器（VBE）”提取紧凑的低层模态信息，再将物理定律注入扩散生成过程，形成“时间变化物理引导机制（TPG）”，实现经验学习与物理规则协同的生成。
- **关键技术细节**：
  - **最优传输模态对齐（OT）**：通过最优传输映射 \(T^*\) 将红外图像分布向可见光图像对齐，降低模态间分布差异，为后续编码提供更紧密的联合表示。
  - **多尺度掩码变分瓶颈编码器（VBE）**：
    - 基于信息瓶颈理论，最大化融合隐变量 \(Z\) 与任务相关的互信息，同时压缩冗余。
    - 利用可学习的多尺度掩码 \(M_s\) 自适应过滤特征，对后验分布 \(q(Z|X',Y)\) 建模为高斯分布，并将隐变量分解为确定性分量 \(\mu\) 和随机扰动 \(R\)，以分离任务相关结构与不确定性。
  - **物理引导条件扩散模型**：
    - 在扩散逆向采样过程中引入物理校正项 \(\Delta \mu_{\text{phys}}\)，使生成过程遵循物理定律。
    - 三种物理约束：**热传导约束**（Laplacian 平滑抑制伪影）、**结构保持约束**（基于可见光梯度保持边缘）、**物理一致性约束**（融合热掩码与结构掩码确保跨模态物理一致）。
    - 时间变化权重 \(\lambda_i(t) = \lambda_i^0 e^{-\gamma t}\)：早期多物理引导，后期多依赖数据驱动细节恢复，模仿“粗感知到细推理”的认知过程。
- **算法流程**：输入图像经 OT 对齐后由 VBE 编码得隐变量 \(z\)，以此为条件，扩散模型从噪声 \(z_T\) 开始逐步去噪，每步先估计干净隐变量 \(z_0\)，再依次施加三类物理约束，最后采样下一步隐变量，直至生成融合图像。

### 3. 实验设计
- **数据集**：
  - MSRS（城市驾驶，昼夜，361 对用于测试）
  - TNO（夜视军事，42 对）
  - FMB（多天气、多光照，280 对）
  - MFNet（城市驾驶，昼夜，393 对）
- **基准方法**：共 17 种，涵盖非端到端（NestFuse， LRRNet， MMAE）、端到端学习型（SwinFusion， SegMiF， SOSMaskFuse， STFNet， CrossFuse， Text\-IF， GIFNet）、生成式（FusionGAN， TarDAL， DDFM， Diff\-IF， CCF， Text\-DiFuse， LFDT\-Fusion）。
- **评估指标**：
  - 7 个无参考：SD， AG， EN， SF， DF， PIQE， BRISQUE
  - 5 个有参考：CC， SCD， Nabf， QSF， VIF
  - 下游任务：语义分割（Mask2Former），以 mIoU 评价。
- **比较方式**：定性视觉对比（局部放大、高曲率可视化）、定量指标对比（表格，最优粗体、次优下划线）。

### 4. 资源与算力
- **硬件**：1 张 NVIDIA RTX 3090 GPU，搭配 Intel Core i7\-6850K CPU @3.60GHz。
- **训练细节**：优化器 Adam，学习率 \(2\times 10^{-5}\)，文中未明确给出训练总时长或总迭代次数。

### 5. 实验数量与充分性
- **实验组数**：
  - 在 4 个公开数据集上分别进行定性、定量比较，每个数据集对比 17 种方法，共生成大量结果图与多个指标表格。
  - 消融实验：对扩散采样模块（DDIM）、最优传输（OT）、变分瓶颈编码器（VBE）、时间物理引导（TPG）进行模块有效性消融（共 5 个变体）；对物理约束组合（\(\Phi_{\text{heat}}\)， \(\Phi_{\text{stru}}\)， \(\Phi_{\text{con}}\)）进行消融（4 种组合）；对掩码组件（\(M_s\)， \(M_{\text{heat}} \& M_{\text{stru}}\)）进行消融（3 种设置）。
  - 下游任务：语义分割对比实验。
- **充分性与公平性**：实验覆盖多种场景、光照、天气，对比方法广泛，指标多维，消融层层递进，实验设计比较充分、客观。所有对比方法均引用自已有工作，评估指标统一，具备公平性。

### 6. 论文的主要结论与发现
- HCLFuse 在融合纹理清晰度（AG 提升约 70%）、空间频率（SF 提升约 39%）、视觉清晰度（DF 提升约 66%）等关键指标上显著超越已有方法，同时具有更完整的高斯曲率结构和更自然的视觉效果。
- 物理引导机制显著增强了扩散模型的生成能力与稳定性，减少了对高质量数据的依赖。
- 所融合的图像在下游语义分割任务中取得了最佳 mIoU，证明其有效保留了任务相关的语义线索。
- 整体上，将认知科学原则引入生成式融合是可行且有效的，为可解释多模态融合提供了新思路。

### 7. 优点
- **创新性强**：首次将人类认知规律（选择性注意、物理知识）与扩散模型系统结合，提出具有理论支撑的生成融合范式。
- **理论严谨**：给出信息下界定理和冗余互信息上界定理，为无监督融合提供了量化优化目标。
- **可解释性提升**：通过变分瓶颈的信息分解和物理约束的可视化，显式展示了模型如何进行信息选择与生成。
- **实验扎实**：多数据集、多指标、多方法对比，消融实验细致，定性与定量分析全面，且验证了下游任务收益。

### 8. 不足与局限
- **输入假设严格**：依赖精确配准的红外与可见光图像对，在未对齐或视角差异大的场景下性能可能下降。
- **计算开销大**：扩散模型迭代推理加上物理约束计算，可能导致推理时间长，难以部署于实时系统或资源受限设备。
- **实验覆盖局限**：仅在4个常见红外\-可见光数据集上测试，未涉及遥感、医学等多光谱融合场景，泛化性未充分验证。
- **物理先验可移植性**：所使用的热、结构等物理约束可能对特定场景敏感，极端噪声或特殊材质条件下有效性有待考证。
- **超参敏感性**：物理引导的衰减系数、初始权重等对生成质量可能有较大影响，文中未详细讨论其调参敏感度。

（完）
