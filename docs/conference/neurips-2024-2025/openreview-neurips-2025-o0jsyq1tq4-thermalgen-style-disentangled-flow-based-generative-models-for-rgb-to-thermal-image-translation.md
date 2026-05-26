---
title: "ThermalGen: Style-Disentangled Flow-Based Generative Models for RGB-to-Thermal Image Translation"
title_zh: "ThermalGen: 基于风格解耦流生成模型的RGB到热红外图像转换"
authors: "Jiuhong Xiao, Roshan Nayak, Ning Zhang, Daniel Toertei, Giuseppe Loianno"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=o0JSYq1TQ4"
tags: ["query:multi-modal"]
score: 5.0
evidence: 从RGB生成热红外图像以实现多模态传感器融合，可应用于遥感
tldr: ThermalGen提出基于风格解耦流生成模型的RGB到热红外图像转换方法，通过自适应流模型和条件架构生成高质量热红外图像，解决了配对数据稀缺问题，为多模态传感器融合（包括遥感）提供数据增强手段。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-o0jsyq1tq4/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1418, \"height\": 850, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-o0jsyq1tq4/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1367, \"height\": 704, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-o0jsyq1tq4/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1346, \"height\": 545, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-o0jsyq1tq4/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1453, \"height\": 772, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-o0jsyq1tq4/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 687, \"height\": 496, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-o0jsyq1tq4/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1376, \"height\": 1193, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-o0jsyq1tq4/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1356, \"height\": 180, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-o0jsyq1tq4/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1407, \"height\": 404, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-o0jsyq1tq4/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1449, \"height\": 678, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-o0jsyq1tq4/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1453, \"height\": 338, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-o0jsyq1tq4/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1453, \"height\": 342, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-o0jsyq1tq4/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 578, \"height\": 304, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-o0jsyq1tq4/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1450, \"height\": 234, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-o0jsyq1tq4/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1452, \"height\": 290, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-o0jsyq1tq4/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1295, \"height\": 181, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-o0jsyq1tq4/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1453, \"height\": 387, \"label\": \"Table\"}]"
motivation: 同步校准的RGB-热红外图像对稀缺，限制了视觉-热传感器融合和多模态任务的发展。
method: 设计自适应流生成模型，结合RGB条件架构和风格解耦机制，实现RGB到热红外的图像转换。
result: 该方法生成的热红外图像逼真，有效支持大规模训练，提升了多模态对齐和检索等任务性能。
conclusion: ThermalGen为跨模态图像转换提供了高效框架，缓解了配对数据不足瓶颈，推动多模态融合应用。
---

## Abstract
Paired RGB-thermal data is crucial for visual-thermal sensor fusion and cross-modality tasks, including important applications such as multi-modal image alignment and retrieval. However, the scarcity of synchronized and calibrated RGB-thermal image pairs presents a major obstacle to progress in these areas. To overcome this challenge, RGB-to-Thermal (RGB-T) image translation has emerged as a promising solution, enabling the synthesis of thermal images from abundant RGB datasets for training purposes. In this study, we propose ThermalGen, an adaptive flow-based generative model for RGB-T image translation, incorporating an RGB image conditioning architecture and a style-disentangled mechanism. To support large-scale training, we curated eight public satellite-aerial, aerial, and ground RGB-T paired datasets, and introduced three new large-scale satellite-aerial RGB-T datasets--DJI-day, Bosonplus-day, and Bosonplus-night--captured across diverse times, sensor types, and geographic regions. Extensive evaluations across multiple RGB-T benchmarks demonstrate that ThermalGen achieves comparable or superior translation performance compared to existing GAN-based and diffusion-based methods. To our knowledge, ThermalGen is the first RGB-T image translation model capable of synthesizing thermal images that reflect significant variations in viewpoints, sensor characteristics, and environmental conditions. Project page: http://xjh19971.github.io/ThermalGen

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **核心问题**：同步且校准的 RGB‑热红外（RGB‑T）图像对极度稀缺，严重阻碍了视觉‑热红外传感器融合、多模态图像对齐与检索等下游任务的发展。直接从 RGB 图像合成热红外图像，能够利用海量 RGB 数据缓解配对数据不足的瓶颈。
- **整体含义**：本文提出一种 **自适应、风格解耦的流匹配生成模型 ThermalGen**，旨在实现高保真、跨域泛化能力强的 RGB 到热红外图像转换，使合成图像能够反映视角、传感器类型、昼夜变化和环境差异等多种真实条件下的热红外特征，从而为下游多模态任务提供灵活、高质量的训练数据。

## 2. 方法论

### 2.1 生成范式与潜在空间
- 采用 **流匹配（Flow Matching）** 生成框架，基于可扩展插值 Transformer（SiT）架构。
- 遵循潜在扩散模型范式：热红外图像通过 **热红外编码器 \(E_T\)** 压缩为潜在变量 \(z_T\)，生成过程反向去噪得到 \( \hat{z}_{0,T} \)，再由解码器 \(D_T\) 重建图像 \( \hat{x}_T \)。
- 扩散过程定义为连续时间 \( t \in [0,1] \) 下的插值：\( z_t = \alpha_t z_0 + \sigma_t \epsilon \)，其中 \( \epsilon \sim \mathcal{N}(0,I) \)。模型学习速度场 \( v_\theta(\hat{z}_{t,T}, t, z_{RGB}, y) \)，通过 ODE 求解器迭代去噪。

### 2.2 风格解耦机制
- 为应对不同数据集的 RGB‑T 映射风格（由传感器、视角、环境等因素决定），定义一组 **可学习的数据集特定风格嵌入** \( Y = \{y_0, y_1, \dots, y_n, y_{un}\} \)，其中 \( y_{un} \) 为无条件风格嵌入。
- 在 SiT 块中采用 **adaLN‑Zero 条件注入**，将风格嵌入与时间步 \( t \) 结合生成条件嵌入 \( c_{y_i, t} \)，通过自适应层归一化的缩放与偏移参数影响生成特征，类似 AdaIN 的风格迁移思想。
- 训练时随机切换条件与无条件嵌入，支持训练后使用 **无分类器引导（CFG）** 调节风格强度。

### 2.3 RGB 图像条件架构
- 使用预训练的 KL‑VAE 编码器 \(E_{RGB}\) 提取 RGB 潜在表征 \(z_{RGB}\)，设计两种条件注入方式：
  1. **多头交叉注意力（Cross‑Attn）**：在 SiT 块的自注意力与逐点前馈网络之间插入交叉注意力层，以 \(z_{RGB}\) 为查询，\( \hat{z}_{t,T} \) 为键和值。
  2. **拼接（Concatenation）**：将 \(z_{RGB}\) 与 \( \hat{z}_{t,T} \) 沿通道拼接后输入 SiT 块，便于从预训练 SiT 权重微调。
- 最终损失函数为流场预测的均方误差：\( \mathcal{L}_{flow} = \mathbb{E}_{z_t, t} \| v_\theta(z_t, t) - v(z_t, t) \|^2 \)。

## 3. 实验设计

### 3.1 数据集与场景
- **整理与收集**：涵盖卫星‑航拍、航拍（无人机/监控）、地面（手持/车载）三大类，共十余个公开数据集，并全新贡献三个大规模卫星‑航拍数据集：
  - **卫星‑航拍**：Boson‑night、DJI‑day、Bosonplus‑day、Bosonplus‑night（覆盖昼夜、多种热传感器、不同地理区域）
  - **航拍**：LLVIP、NII‑CU、AVIID、CalTech
  - **地面**：M³FD、MSRS、FLIR、Freiburg‑day/night、SMOD‑day/night、KAIST 等
- 数据预处理：统一标准化为 8 位热红外图像，对齐 RGB 与热红外，去除无效区域；卫星‑航拍数据采用 35 m 采样步长裁剪为 512×512 图像块。

### 3.2 评估基准与指标
- **基准方法**：对比了 GAN 类（pix2pix、CycleGAN、pix2pixHD、VQGAN）和扩散类（DDIM、BBDM、DiffV2IR 及其微调版本）。DiffV2IR 使用预训练模型。
- **评价指标**：PSNR（峰值信噪比）、SSIM（结构相似性）、FID（Fréchet Inception 距离）和 LPIPS（学习感知图像块相似度），从像素保真度、结构相似性、分布距离与感知质量多维度评估。

### 3.3 消融与超参数分析
- **模型架构**：测试不同 Transformer 大小（SiT‑B/L/XL）及补丁大小（2/4/8），评估对 FID 的影响。
- **RGB 条件设计**：比较交叉注意力与拼接两种注入方案的 FID 表现。
- **风格嵌入设置**：对比无条件、条件（指定风格嵌入）和 CFG（scale=2.0）在多个数据集上的效果。
- **CFG 尺度调优**：在 Boson‑night 和 FLIR 上实验不同 CFG 因子（1.0、2.0、4.0、8.0、16.0）对 FID 的优化。

## 4. 资源与算力

- **硬件平台**：所有训练与评估均在 **单张 NVIDIA A100 或 H100 GPU** 上完成。
- **训练配置**：
  - 热红外编码器/解码器：batch size 16，AdamW 优化器（学习率 \(6\times10^{-5}\)、权重衰减 \(1\times10^{-3}\)），训练 200k 步。
  - 流匹配生成模型：batch size 64，AdamW（学习率 \(1\times10^{-4}\)、无权重衰减），训练 200k 步。
  - 图像随机缩放并裁剪至 256×256，推理时使用 50 步 ODE 去噪。
- 论文未明确报告总训练时长，但训练步数与批次大小足以估算所需计算量。

## 5. 实验数量与充分性

- **跨数据集对比实验**：在 **6 个代表性数据集**（卫星‑航拍：Boson‑night、Bosonplus‑day/night；航拍：LLVIP、NII‑CU、AVIID；地面：M³FD、MSRS、FLIR）上与 8 种基线方法进行定量对比，表格数据翔实。
- **消融实验**：
  - 7 个数据集上的模型架构对比（不同规模 Transformer 与补丁大小）
  - 5 个数据集上的 RGB 条件设计对比
  - 4 个数据集上的风格嵌入策略对比
- **CFG 调优实验**：在 2 个数据集上测试不同引导尺度。
- **定性分析**：通过大量生成样本可视化与 t‑SNE 特征分布分析予以辅证。
- 整体实验设计覆盖多种模态、视角、环境和传感器变化，对比基准广泛，消融维度全面，具备较好的客观性与公平性。但未报告多随机种子下的误差棒，统计显著性未量化。

## 6. 主要结论与发现

- ThermalGen 在绝大多数评测数据集上取得了 **优于或持平于现有 GAN 与扩散基线** 的表现，尤其是在 FID 和 LPIPS 等感知质量指标上优势明显。
- **风格解耦机制** 对跨数据集泛化至关重要：指定风格嵌入并结合 CFG 可显著提升生成真实感，尤其在风格差异大的数据集上（如 Bosonplus‑day/night、NII‑CU）。
- 消融实验表明：更深的 Transformer（SiT‑L/XL）和更小的补丁尺寸能进一步提升性能；RGB 潜变量以拼接方式注入略优于交叉注意力；CFG 尺度调节可针对性缓解某些数据集上的退化问题。
- ThermalGen 是首个能够 **同时处理卫星‑航拍、航拍和地面场景，并平滑适应视角、传感器、昼夜及环境变化** 的 RGB‑T 转换模型。

## 7. 优点

- **方法论创新**：将流匹配与潜在扩散结合，并引入可解耦的数据集特定风格嵌入，无需为每个新域重新训练模型，即可生成与目标风格一致的热红外图像。
- **数据贡献**：提供了三个新的大规模卫星‑航拍 RGB‑T 数据集（DJI‑day， Bosonplus‑day/night），扩充了社区在远距离、不同传感器和光照条件下的配对数据资源。
- **实验广度**：覆盖卫星‑航拍、航拍、地面三类平台，对比 GAN 与扩散两大类基线，消融研究深入，有说服力。
- **实用性强**：合成的热红外图像在视觉上高度逼真，能够为多模态特征匹配、目标检测等下游任务提供高质量、无限量的训练数据，具有显著的工程价值。

## 8. 不足与局限

- **特定数据集性能退化**：在 **Boson‑night**（极低对比度）、**FLIR**（远距离模糊、过曝/欠曝）和 **LLVIP**（训练‑测试域差异显著）等特殊数据上，原始模型表现欠佳。论文通过调大 CFG 尺度或扩充训练数据得以缓解，但仍未在所有指标上超越最优基线。
- **算力与可复现性**：虽指明单卡 A100/H100 训练，但未提供总训练时长，且未进行多随机种子误差分析，可能影响统计可靠性。
- **应用限制与伦理**：模型在安全关键场景下合成输出可能被误用为真实热红外数据，存在被用于欺骗或隐私侵犯的风险。此外，对极端视角、低分辨率或严重遮挡的情况未做专项评测。
- **模态假设**：方法依赖 RGB 与热红外之间的统计映射，而热红外辐射本质上无法仅从可见光完全推断，当场景中存在非视觉热源时，合成图像的真实性可能下降。

（完）
