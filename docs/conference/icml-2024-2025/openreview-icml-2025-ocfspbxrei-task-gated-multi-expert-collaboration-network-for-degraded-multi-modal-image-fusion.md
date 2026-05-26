---
title: Task-Gated Multi-Expert Collaboration Network for Degraded Multi-Modal Image Fusion
title_zh: 任务门控多专家协作网络用于退化多模态图像融合
authors: "Yiming Sun, Xin Li, Pengfei Zhu, Qinghua Hu, Dongwei Ren, Huiying Xu, Xinzhong Zhu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=OcFsPBXREI"
tags: ["query:multi-modal"]
score: 6.0
evidence: 基于任务门控多专家协作的退化多模态图像融合
tldr: 针对现实成像中可见光和红外图像的噪声、模糊、雾霾及条纹噪声等退化问题，提出任务门控多专家协作网络TG-ECNet。通过退化感知门控动态分配专家组进行复原，并融合多模态特征。实验表明方法在退化条件下的融合质量优于现有方案。虽然应用场景为搜救与安防而非遥感，但退化处理和多模态融合策略对遥感图像在恶劣天气或传感器故障下的融合具有借鉴意义。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 860, \"height\": 583, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1765, \"height\": 724, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 851, \"height\": 597, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1737, \"height\": 721, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1776, \"height\": 1029, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1772, \"height\": 379, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1774, \"height\": 483, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 893, \"height\": 610, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1782, \"height\": 611, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ocfspbxrei/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1775, \"height\": 487, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1767, \"height\": 458, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1765, \"height\": 455, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1771, \"height\": 293, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1521, \"height\": 119, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 856, \"height\": 447, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 859, \"height\": 349, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1767, \"height\": 495, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1767, \"height\": 494, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1769, \"height\": 494, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1765, \"height\": 494, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1768, \"height\": 492, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1767, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1766, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1768, \"height\": 221, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1767, \"height\": 221, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1327, \"height\": 325, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ocfspbxrei/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1327, \"height\": 431, \"label\": \"Table\"}]"
motivation: 真实多模态图像融合面临噪声、模糊等退化问题，模型性能下降。
method: 提出任务感知门控与多专家协作框架，动态分配专家进行复原与融合。
result: 在退化可见光与红外图像融合中表现优异，鲁棒性强。
conclusion: 退化感知的多模态融合方法可推广至遥感图像复杂成像条件。
---

## Abstract
Multi-modal image fusion aims to integrate complementary information from different modalities to enhance perceptual capabilities in applications such as rescue and security. However, real-world imaging often suffers from degradation issues, such as noise, blur, and haze in visible imaging, as well as stripe noise in infrared imaging, which significantly degrades model performance. To address these challenges, we propose a task-gated multi-expert collaboration network (TG-ECNet) for degraded multi-modal image fusion. The core of our model lies in the task-aware gating and multi-expert collaborative framework, where the task-aware gating operates in two stages: degradation-aware gating dynamically allocates expert groups for restoration based on degradation types, and fusion-aware gating guides feature integration across modalities to balance information retention between fusion and restoration tasks. To achieve this, we design a two-stage training strategy that unifies the learning of restoration and fusion tasks. This strategy resolves the inherent conflict in information processing between the two tasks, enabling all-in-one multi-modal image restoration and fusion. Experimental results demonstrate that TG-ECNet significantly enhances fusion performance under diverse complex degradation conditions and improves robustness in downstream applications. The code is available at https://github.com/LeeX54946/TG-ECNet.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：真实世界多模态成像（可见光 + 红外）常伴随严重退化，如可见光图像的噪声、模糊、雾霾，以及红外图像的条纹噪声。这些退化显著降低多模态图像融合的质量，并影响下游任务（如检测、分割）的鲁棒性。
- **研究动机**：现有级联式方法（先复原再融合）需要预存多个专用模型且任务割裂，容易丢失对融合有益的信息；最近的统一框架（如扩散模型、文本引导方法）在复杂多退化场景下表现依然有限。因此，亟需一种能够统一处理多种退化、同时兼顾复原与融合功能的全能型方法。
- **整体含义**：提出一种**任务门控多专家协作网络（TG-ECNet）**，将多模态图像复原与融合整合为单一模型，通过动态分配专家和两阶段训练，实现“all-in-one”的退化多模态图像融合。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程
- **整体框架**：基于U型Transformer，包含退化感知编码器、图像复原解码器和融合分支。红外与可见光分支共享编码器和解码器权重。
- **任务感知门控与多专家协作**：
  - **退化感知门控（Degradation‑Aware Gating）**：在编码器中，根据输入图像的退化类型（噪声、模糊、雾霾、条纹噪声）动态选择最合适的“专家组”进行逐像素复原。输出为：
    \[
    \text{Output} = \sum_{i=1}^{N} G_{\text{Degrad}}(I_d)_i \cdot E_{\text{Degrad}_i}(I_d)
    \]
  - **融合感知门控（Fusion‑Aware Gating）**：在融合阶段，通过可学习权重 \(\alpha, \beta\) 整合复原后的可见光特征 \(F_V\) 和红外特征 \(F_I\) 得到 \(F_M = \alpha F_V + \beta F_I\)，然后利用门控从多模态中筛选最有价值的互补信息：
    \[
    \text{Output}_{\text{Fus}} = \sum_{i=1}^{N} G_{\text{Fus}}(F_M)_i \cdot E_{\text{Fus}_i}(F_M)
    \]
- **两阶段训练策略**：
  - **阶段1（复原训练）**：仅优化复原任务，损失函数 \(L_{\text{stage1}} = L_{\text{res}} + L_{\text{Degrad\_grad}} + L_{\text{Degrad\_load}}\)，其中 \(L_{\text{res}} = \|I_V - I_V^c\| + \|I_I - I_I^c\|\)。
  - **阶段2（融合训练）**：在阶段1的基础上细调，加入融合损失 \(L_{\text{stage2}} = L_{\text{pixel}} + L_{\text{grad}} + L_{\text{Fus\_load}}\)，同时保留复原损失，实现联合优化。
- **核心思想**：通过解耦任务的学习过程，避免复原与融合之间的信息冲突，从而实现端到端的“全能”退化多模态图像融合。

### 3. 实验设计：使用了哪些数据集/场景，它的benchmark是什么，对比了哪些方法
- **数据集**：
  - **自建数据集 DeMMI-RF**：包含城市街景和低空无人机视角，共6种退化（高/中/低高斯噪声、雾霾、散焦模糊、条纹噪声），训练集26631对，测试集9895对。
  - **公开数据集 EMS**（Yi et al., 2024）：用于进一步验证。
- **对比方法**：
  - **级联式（先用AdaIR复原，再融合）**：DenseFuse, SwinFuse, CDDFuse, SeAFusion, MGDN, EMMA。
  - **联合式（端到端复原‑融合）**：AWFusion, DRMF, Text‑IF。
- **评价指标**：融合质量（CC, MSE, PSNR, \(N_{\text{abf}}\), MS‑SSIM），下游任务（YOLOv5目标检测 mAP、Grounded‑SAM 分割）。

### 4. 资源与算力
- **硬件**：6块NVIDIA GeForce RTX 4090 GPU。
- **软件**：PyTorch 1.12.0，Adam优化器，初始学习率 \(1\times10^{-4}\)，余弦退火调整。
- **训练细节**：图像随机裁剪至 \(128\times128\)，数据增强（水平/垂直翻转）。第一阶段训练30 epoch，第二阶段训练30 epoch，直接在多个任务上测试。**未明确说明总训练时长**。

### 5. 实验数量与充分性
- **实验组数**：约**9组以上主要实验**，覆盖单个退化（噪声、雾霾、模糊、条纹）、多退化组合（9种混合退化）、无退化场景、真实世界数据（AWMM）、下游任务（检测、分割）以及消融实验（移除任务感知门控、移除不同多专家模块、单阶段训练对比）。
- **充分性与公平性**：实验设置全面，不仅比较了多个SOTA方法，还统一采用相同的预处理流水线（级联式对比时用同一复原网络AdaIR）。指标覆盖像素级、结构级和语义级，消融实验验证各组件作用。自建数据集规模充足，结论具有说服力。实验设计客观、公平。

### 6. 论文的主要结论与发现
- TG-ECNet在多种单一和混合退化条件下，均能有效抑制退化并生成高质量融合图像，在PSNR、CC、MS‑SSIM等指标上显著优于现有级联式和联合方法。
- 通过两阶段训练策略成功解耦复原与融合任务，避免了信息处理冲突，实现了真正的“all‑in‑one”处理。
- 复原后的融合结果能有效提升下游目标检测（mAP50达0.969）和分割精度，鲁棒性更强。

### 7. 优点：方法或实验设计上的亮点
- **创新架构**：任务感知门控 + 多专家协作，动态路由不同退化与融合任务，灵活性高。
- **两阶段训练**：明确分离复原与融合任务训练，避免梯度冲突，是处理多任务学习的有效策略。
- **统一框架**：单一模型完成多种退化下的复原与融合，降低部署成本。
- **大规模基准**：建立了包含无人机和驾驶场景的多退化多模态数据集 DeMMI‑RF，有助于社区发展。
- **全面评估**：涵盖多种退化、多项指标、多个下游任务，实验丰富，验证维度多元。

### 8. 不足与局限
- **退化类型有限**：目前仅包含预设的噪声、雾霾、模糊、条纹噪声，对更复杂或未知的真实退化（如雨雪、低光等）泛化性未验证。
- **专家数目敏感**：专家数量 \(N=11\)、选择个数 \(K=6\) 是经验设定，需手动调参，未探索自适应或动态稀疏激活。
- **计算开销与效率**：虽给出了参数和FPS对比，但与轻量级模型相比仍较重，未深入讨论实时性部署限制。
- **数据集场景偏窄**：以城市街景和无人机为主，其他场景（如医疗、遥感）的适用性未知。
- **两阶段训练耗时**：训练需先后执行两个阶段，流程略为繁琐；第一阶段参数冻结策略对最终融合性能的影响未充分剖析。

（完）
