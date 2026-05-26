---
title: "OSKAR: Omnimodal Self-supervised Knowledge Abstraction and Representation"
title_zh: 全模态自监督知识抽象与表示
authors: "Mohamed O Abdelfattah, Kaouther Messaoud, Alexandre Alahi"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=LWuhOoHpo5"
tags: ["query:multi-modal"]
score: 4.0
evidence: 自监督多模态学习预测缺失token，可用于融合与不完整模态处理
tldr: OSKAR提出首个基于自举潜在特征预测的多模态基础模型，通过掩码token预测学习多模态表示，以自监督方式高效处理缺失模态并实现多模态融合，为通用的不完整多模态数据建模提供了可扩展方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-lwuhoohpo5/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1434, \"height\": 639, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-lwuhoohpo5/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1445, \"height\": 832, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-lwuhoohpo5/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1451, \"height\": 462, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-lwuhoohpo5/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1449, \"height\": 577, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-lwuhoohpo5/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1451, \"height\": 395, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-lwuhoohpo5/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 722, \"height\": 636, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-lwuhoohpo5/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 724, \"height\": 674, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-lwuhoohpo5/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 721, \"height\": 606, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-lwuhoohpo5/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 720, \"height\": 313, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-lwuhoohpo5/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 721, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-lwuhoohpo5/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 724, \"height\": 305, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-lwuhoohpo5/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 724, \"height\": 303, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-lwuhoohpo5/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 719, \"height\": 331, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-lwuhoohpo5/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 722, \"height\": 279, \"label\": \"Table\"}]"
motivation: 现有多模态预训练方法需大量负样本或人工增强，且难以处理缺失模态，计算成本随模态数增加。
method: 提出自举潜在特征预测策略，对多模态掩码token预测缺失部分，由动量更新的单模态编码器监督，实现计算与模态数解耦。
result: 该方法在学习高层表示的同时保留模态特定信息，并在多模态任务上展现出高效性和可扩展性。
conclusion: OSKAR为缺失模态下的多模态表示学习提供了新的有效范式，避免了生成或对比方法的局限性。
---

## Abstract
We present OSKAR, the first multimodal foundation model based on bootstrapped latent feature prediction. Unlike generative or contrastive methods, it avoids memorizing unnecessary details (e.g., pixels), and does not require negative pairs, large memory banks, or hand-crafted augmentations. We propose a novel pretraining strategy: given masked tokens from multiple modalities, predict a subset of missing tokens per modality, supervised by momentum-updated uni-modal target encoders. This design efficiently utilizes the model capacity in learning high-level representations while retaining modality-specific information. Further, we propose a scalable design which decouples the compute cost from the number of modalities using a fixed representative token budget—in both input and target tokens—and introduces a parameter-efficient cross-attention predictor that grounds each prediction in the full multimodal context. We instantiate OSKAR on video, skeleton, and text modalities. Extensive experimental results show that OSKAR's unified pretrained encoder outperforms models with specialized architectures  of similar size in action recognition (rgb, skeleton, frozen, low-shot) and localization, video-text retrieval, and video question answering. Project website: https://multimodal-oskar.github.io

---

## 论文详细总结（自动生成）

## 一、论文核心问题与整体含义

- **研究背景**：人类感知本质上是多模态的（视觉、运动、语言等）。当前多模态自监督学习主要分为两大类——生成式方法（如 MAE、VideoMAE）和对比式方法（如 CLIP、ImageBind）。前者在像素空间重建低层细节，浪费模型容量；后者依赖负样本、人工增强，且缺乏跨模态预测能力，难以学到丰富的交叉模态表征。
- **核心问题**：能否设计一种新的预训练策略，避免无效的像素重建和苛刻的对比学习约束，从而高效地学习高层、语义丰富的跨模态表示？
- **整体含义**：论文提出 OSKAR，首个基于自举式潜在特征预测（bootstrapped latent feature prediction）的多模态基础模型。它采用“先融合，再预测”的代理任务，仅在特征空间进行学习，无需负样本、大内存库或手工增强，同时显式保留模态特有的结构信息。

## 二、方法论

- **核心思想（Fuse-then-Predict）**：给定多个模态的部分可见 token，先用一个跨模态融合编码器融合可见信息，再为每个模态预测其缺失 token 的潜在表示。预测目标由动量更新的模态特有目标编码器提供，从而实现稳定且跨模态的监督。
- **关键技术细节**：
  - **模态特定目标编码器**：每种模态拥有独立的目标编码器，通过 EMA 从融合编码器更新权重。这既可以采用共享动量系数得到统一编码器，也可为不同模态分配不同动量系数，使各模态按自身学习节奏演化。
  - **跨模态掩码策略**：为保证计算量不随模态数线性增长，模型固定输入和目标 token 的总预算（如均设为 128）。通过 Dirichlet 分布采样控制各模态占比，且使用跨模态时空互斥约束，防止模型利用简单捷径（如同一视频块同时出现在输入和目标中）。
  - **统一的跨注意力预测器**：预测器为单网络、权重共享，通过自注意力捕捉模态内结构，并通过交叉注意力从融合特征中获得跨模态上下文，以预测每个模态的缺失表示。
  - **训练目标**：在潜在空间最小化预测特征与目标特征的均方误差（MSE），避免模态特定的损失函数。
- **算法流程**：
  1. 输入视频、骨架、文本分别 tokenized 并投影至共享嵌入空间。
  2. 应用掩码策略选取少量 token 送入融合编码器（交叉注意力）得到融合表示 H。
  3. 预测器接收目标位置的掩码查询，经自注意力和与 H 的交叉注意力生成预测特征 Yp。
  4. 目标编码器独立生成目标特征 Yt（与融合编码器共享结构，但用 EMA 更新）。
  5. 计算 MSE 损失 L = 1/Nt ∑ ||Yp_i - Yt_i||²。
  6. 微调时直接使用目标编码器适配下游任务。

## 三、实验设计

- **预训练数据**：OpenHumanVid 数据集（1000 万视频，16.7K 小时），使用 YOLO11 伪标记人体姿态与检测框，MiniCPM/CogVLM 生成字幕。视频、骨架、文本分别用 V‑JEPA、MotionBERT、WordPiece 预 tokenize。
- **下游任务与 Benchmark**：
  - RGB 动作识别：Kinetics-400 (K400)、Something-Something V2 (SSv2)。
  - 骨架动作识别：NTU60、NTU120。
  - 时空动作定位：AVA v2.2。
  - 文本‑视频检索：MSRVTT、MSVD、VATEX。
  - 视频问答：MSRVTT-QA、MSVD-QA、TGIF-FrameQA。
- **对比方法**：生成式模型（VideoMAE、OmniMAE、ST-MAE）、对比式/联合嵌入模型（V‑JEPA、MotionBERT、CLIP4CLIP 等），以及相关多模态模型（OmniVL、InternVideo 等）。

## 四、资源与算力

- **训练硬件**：预训练使用 256 块 GH200 GPU。
- **训练规模**：处理约 5000 亿 token，包含 10 亿 token 的 warmup。总批次大小 8192，使用 AdamW 优化器（β1=0.9, β2=0.95），基本学习率 1e‑4，余弦衰减，权重衰减 0.05。
- **推理与微调**：下游微调时，所用计算量与常规 ViT 微调相当，论文未单独列出微调的具体 GPU 数量。

## 五、实验数量与充分性

- **实验组数量**：论文报告了多个模型尺寸（ViT‑S/B/L）在 5 个主要任务（动作识别/定位/检索/问答）共 10+ 个基准上的结果，并展示了样本效率、参数效率、标签效率曲线（图 3），以及定性预测可视化。
- **消融实验**：使用 ViT‑S 在 100K 样本上预训练后，围绕多个关键设计进行消融：
  - 逐步添加模态（视频、骨架、文本）对性能的影响（表 6）。
  - 注意力路由策略（融合编码器、目标编码器、预测器中交叉/自注意力的组合，表 8）。
  - 共享与定制目标编码器及 EMA 系数（表 7、图 5b）。
  - 输入与目标 token 数量（表 9）。
  - Dirichlet 分布浓度参数 α 的影响（图 5c）。
  - 任务空间（输入空间重建 vs. 特征空间预测）的比较（图 5a）。
  - 边界框嵌入的作用（图 5a）。
- **充分性与客观性**：实验覆盖多个数据集、不同模型规模、低样本/低标签设定，且与同期主流模型公平对比（相同分辨率、类似参数量）。消融实验系统且维度全面，能有效支撑论文主张。但所有实验基于固定随机种子，未报告多次运行的误差棒，统计显著性未能完全展示。

## 六、论文的主要结论与发现

- OSKAR 的统一预训练编码器在多个视频、骨架和文本任务上，一致地超越同等规模的特化模型，证明跨模态潜在预测能够学习到通用的高层表示。
- 该方法在低样本、低参数、低标签场景下表现突出，显示出良好的数据效率和泛化能力。
- 特征空间预测比像素重建更有利于捕捉语义，且动量更新的目标编码器提供了稳定且可调整的监督信号。
- 跨模态融合与预测的设计在保留模态特有结构的同时，显著提升了跨模态对齐性能。

## 七、优点

- **新颖的预训练范式**：首次将自举潜在预测扩展到多模态，避免生成式模型的低效和对比式模型的限制。
- **计算高效且可扩展**：通过固定 token 预算、Dirichlet 采样解耦计算成本与模态数量，支持即插即用扩展新模态。
- **灵活的编码器策略**：支持共享或定制目标编码器，可在统一表征与模态特有性能之间权衡。
- **全面的实验验证**：覆盖多种下游任务和消融分析，实证支撑强。
- **无需外部教师或标注**：完全基于伪标签训练，易于规模化。

## 八、不足与局限

- **模态覆盖有限**：当前仅整合视频、骨架和文本，未探索音频、深度等额外模态，限制了对更丰富多模态场景的验证。
- **数据规模依赖**：预训练数据量较大（10M 视频），对计算资源要求高，可能制约资源有限环境下的复现与普及。
- **EMA 敏感性**：目标编码器的动量系数对性能影响显著，需人工调节，缺乏自适应调整机制，可能增加调参负担。
- **缺少统计重复**：受限于计算成本，未报告多次运行的均值和方差，实验结果稳定性无法量化。
- **词汇/文本限制**：仅使用英文文本，未考虑多语言场景，且生成式文本任务（如 captioning）的迁移能力未验证。
- **应用风险**：模型可能继承伪标签数据中的偏差（如人体检测偏差），在隐私敏感的监控等应用中需谨慎。

（完）
