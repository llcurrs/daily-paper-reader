---
title: "GeoLLaVA-8K: Scaling Remote-Sensing Multimodal Large Language Models to 8K Resolution"
title_zh: "GeoLLaVA-8K: 将遥感多模态大语言模型扩展到8K分辨率"
authors: "Fengxiang Wang, Mingshuo Chen, Yueying Li, Di Wang, Haotian Wang, Zonghao Guo, Zefan Wang, Shan Boqi, Long Lan, Yulin Wang, Hongzhen Wang, Wenjing Yang, Bo Du, Jing Zhang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=LTgUInLTbP"
tags: ["query:multi-modal"]
score: 7.0
evidence: 提出超高分辨率遥感视觉语言数据集和模型，实现多模态遥感图像分类与分析
tldr: GeoLLaVA-8K通过构建超高分辨率遥感视觉问答数据集SuperRS-VQA和HighRS-VQA，并提出基于目标中心token剪枝策略，有效缓解超高分辨率遥感图像带来的token爆炸问题，首次将多模态大模型扩展到8K遥感图像，显著提升了遥感图像理解与分类能力。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-ltguinltbp/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1415, \"height\": 1232, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ltguinltbp/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 697, \"height\": 412, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ltguinltbp/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1422, \"height\": 284, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ltguinltbp/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 794, \"height\": 444, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ltguinltbp/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1310, \"height\": 608, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ltguinltbp/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 935, \"height\": 683, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ltguinltbp/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1415, \"height\": 304, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ltguinltbp/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1438, \"height\": 373, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ltguinltbp/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1410, \"height\": 639, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ltguinltbp/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1185, \"height\": 608, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ltguinltbp/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 688, \"height\": 567, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ltguinltbp/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1233, \"height\": 705, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ltguinltbp/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1305, \"height\": 1363, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-ltguinltbp/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 729, \"height\": 272, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ltguinltbp/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 613, \"height\": 672, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ltguinltbp/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 612, \"height\": 371, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ltguinltbp/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1456, \"height\": 639, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ltguinltbp/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 702, \"height\": 168, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ltguinltbp/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1443, \"height\": 168, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ltguinltbp/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1435, \"height\": 110, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ltguinltbp/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 657, \"height\": 132, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ltguinltbp/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 662, \"height\": 280, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ltguinltbp/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1416, \"height\": 472, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ltguinltbp/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1446, \"height\": 569, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ltguinltbp/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1446, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ltguinltbp/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1448, \"height\": 179, \"label\": \"Table\"}]"
motivation: 超高分辨率遥感图像标注数据稀缺且大尺寸导致token爆炸，现有多模态基础模型难以处理。
method: 构建最高分辨率遥感VQA数据集，并提出目标中心token剪枝策略，保留关键信息剪除背景冗余。
result: 在22种真实对话任务上有效扩展了多模态大模型，实现了8K分辨率遥感图像的高效理解。
conclusion: GeoLLaVA-8K为超高分辨率遥感多模态分析提供了数据和模型基础，推动了遥感大模型发展。
---

## Abstract
Ultra-high-resolution (UHR) remote sensing (RS) imagery offers valuable data for Earth observation but pose challenges for existing multimodal foundation models due to two key bottlenecks: (1) limited availability of UHR training data, and (2) token explosion caused by the large image size. To address data scarcity, we introduce **SuperRS-VQA** (avg. 8,376$\times$8,376) and **HighRS-VQA** (avg. 2,000$\times$1,912), the highest-resolution vision-language datasets in RS to date, covering 22 real-world dialogue tasks. To mitigate token explosion, our pilot studies reveal significant redundancy in RS images: crucial information is concentrated in a small subset of object-centric tokens, while pruning background tokens (e.g., ocean or forest) can even improve performance. Motivated by these findings, we propose two strategies: *Background Token Pruning* and *Anchored Token Selection*, to reduce the memory footprint while preserving key semantics. Integrating these techniques, we introduce **GeoLLaVA-8K**, the first RS-focused multimodal large language model capable of handling inputs up to 8K$\times$8K resolution, built on the LLaVA framework. Trained on SuperRS-VQA and HighRS-VQA, GeoLLaVA-8K sets a new state-of-the-art on the XLRS-Bench. Datasets and code were released at https://github.com/MiliLab/GeoLLaVA-8K.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
*   **核心问题**：现有多模态大模型（MLLMs）难以有效处理超高分（Ultra-High-Resolution, UHR，例如 8K×8K）遥感图像，主要面临两项瓶颈：（1）可供训练的 UHR 图文数据极度匮乏；（2）大尺寸图像导致视觉标记（token）数量爆炸，引发计算溢出与语义密度低下。
*   **整体含义**：本研究旨在突破遥感 MLLM 的分辨率上限，通过构建迄今最高分辨率的遥感视觉问答数据集，并提出一种针对背景冗余和关键目标稀疏性问题的标记压缩策略，首次实现能直接处理 8K 分辨率输入的遥感专用多模态大语言模型 GeoLLaVA‑8K。

### 2. 论文提出的方法论
*   **核心思想**：遥感图像中存在严重的信息冗余——大部分像素为低信息密度的背景（如海洋、森林），而关键语义集中在稀疏的物体标记上。基于此，提出“背景标记剪枝+锚定标记选择”的两阶段标记压缩框架，仅在微调阶段作用于视觉编码器和投影层之间，以减小序列长度并保留关键目标信息。
*   **关键技术细节与算法流程**：
    *   **数据集构建**：
        *   **SuperRS‑VQA**（平均分辨率约 8,376×8,376）：纯手动标注 12K 个超高分辨率图文对话样本，覆盖 22 种任务。
        *   **HighRS‑VQA**（平均分辨率约 2,000×1,912）：利用 GPT‑4o 结合已有检测分割标注进行半自动生成，再通过基于梯度影响的 LESS 框架筛选出对下游最有价值的 70% 样本，最终得到 69K 个中等高分辨率样本。筛选时使用简化的影响函数：Inf_SGD(z_i, X) = max_{x∈X} cos⟨∇ℓ_θ(z_i), ∇ℓ_θ(x)⟩，并利用随机投影降维存储 LoRA 梯度。
    *   **背景标记剪枝（Background Token Pruning）**：
        *   基于语义亲和力的自适应聚类：对每个标记 p，在其局部邻域 N_p 内依概率 q_s(p) 指定最相似的邻近标记 s。该过程迭代 N 步，逐渐形成代表相同背景成分的不规则聚类，合并重叠簇后，用少数标记替代整个聚类，从而大幅压缩冗余背景标记。
    *   **锚定标记选择（Anchored Token Selection, ATS）**：
        *   利用预训练 ViT 中 [CLS] 标记与其余图像块标记之间的注意力图来保留关键目标。具体公式为：a_[CLS] = Softmax( (z_[CLS]W^Q (Z_v W^V)^T) / √d )。选择倒数第二层中注意力分数最高的前 R = n × r 个标记（r 为压缩比），确保不易丢失小物体等关键语义。
*   **模型集成**：以 LLaVA‑Next‑2K 为骨架，将其输入分辨率扩展到 24×24 网格（约 8K），训练时在两阶段 token 压缩后，将保留的视觉标记经投影器与语言指令一同送入 LLM 生成回答。

### 3. 实验设计
*   **评估基准**：XLRS‑Bench，这是一个专为超大尺寸（平均 8,500×8,500）遥感图像设计的多任务 VQA 基准，涵盖感知（计数、场景分类、目标属性、空间关系）和推理（路径规划、异常检测、复杂推理、时空推理）两大类共 13 个三级子任务。
*   **对比方法**（共 16 个）：
    *   **遥感专用模型**：GeoChat。
    *   **闭源 MLLMs**：GPT‑4o、GPT‑4o‑mini、Claude 3.7 Sonnet、Gemini 2.0 Flash。
    *   **开源 MLLMs**：InternLM‑XComposer‑2.5、LLaVA‑Next、LLaVA‑OneVision（7B/72B）、InternVL2.5‑8B、InternVL3（8B/78B）、Qwen2‑VL‑7B、Qwen2.5‑VL（7B/72B）等。
*   **实验场景**：
    *   零样本设定，统一提示词。
    *   消融实验：高分辨率数据集 v.s. VRSBench；不同标记压缩比（16×/24×/32×）；数据集与标记优化策略的组合贡献。
    *   计算效率：不同压缩比下的 FLOPs 与推理延迟。
    *   小物体专项：基于 COCO 面积标准划分的极小/很小/一般小物体子集上的性能。
    *   泛化测试：在外部超高分基准 LRS‑VQA 上进行验证。

### 4. 资源与算力
*   **GPU 型号与数量**：使用 16 至 24 块 NVIDIA A100 GPU。
*   **训练设置**：单轮（1 epoch）全参数监督微调，解冻视觉编码器、投影器和语言模型。学习率：vision 部分 1e‑6，proj 与 LLM 部分 5e‑6；批次大小 16；采用 ZeRO‑2 并行；输入分辨率 8,064×8,064。论文未明确说明总训练时长（单位小时），但给出了上述配置细节。

### 5. 实验数量与充分性
*   **实验组数概览**：
    *   基准对比：1 个主表（Table 4）和 1 个二级能力表，对比 16 个模型。
    *   数据集消融：3 组（Table 13），验证 SuperRS‑VQA 与 HighRS‑VQA 的叠加增益。
    *   方法消融：3 组（Table 6），分别验证高分辨率数据、BTP 及 ATS 的作用。
    *   压缩比消融：3 种配置（Table 5），并考察对应的 FLOPs 和延迟。
    *   专项分析：小物体场景（Table 7）和外部泛化实验（Table 8）。
    *   先导实验：背景占比统计、背景裁剪对比、目标标记剔除实验（Table 3）等。
*   **充分性与公平性评价**：实验设计比较系统，消融维度较多，且对比了当时最新的强基线模型，采用统一基准和零样本测评，整体客观、公平。各类实验能有效支撑所提方法中各个组件有效性的论断。

### 6. 论文的主要结论与发现
*   GeoLLaVA‑8K 以 7B 参数在 XLRS‑Bench 上取得了 51.5% 的平均准确率，不仅远超同量级开源模型，甚至超越了 72B 的 Qwen2.5‑VL‑72B（50.2%）等更大模型，验证了领域适配和高效标记管理的重要性。
*   单纯提升分辨率（如 LLaVA‑Next‑9K）反而会因训练数据缺失而性能下降；但若配合背景剪枝，即使仅保留一半背景标记，性能还能提升（43.2% → 44.3%），证明背景冗余对建模有害。
*   目标物体相关的视觉标记具有高度局部性，少量剪除即会导致大幅性能下降，而 [CLS] 注意力能够有效定位这些关键标记。
*   高分辨率数据集带来的提升（从 44.7% 到 49.1%）不及叠加标记优化后明显（到 51.5%），说明标记管理是实现 UHR 遥感理解的核心驱动力。
*   模型在路径规划（66.0%）、时空推理（50.0%）等需要长程依赖的任务上表现尤为突出，展现了深层推理潜力。

### 7. 优点
*   **填补数据空白**：推出了目前分辨率最高的遥感视觉语言训练数据集，并设计了有效的半自动+影响函数筛选管线，兼顾质量与规模。
*   **问题认知深刻**：通过先导实验精确量化了遥感图像的“低语义密度”特征，并据此针对性设计了标记剪枝策略，逻辑链条清晰。
*   **方法简洁高效**：仅通过背景聚类和 [CLS] 注意力选择，即实现 24 倍标记压缩，极大降低算力需求，同时保证性能。
*   **实验说服力强**：与大量最新 SOTA 模型公平对比，并提供了多维度的消融、效率分析和跨基准泛化测试。

### 8. 不足与局限
*   **传感器模态单一**：仅针对光学卫星图像训练和评估，对合成孔径雷达（SAR）、多光谱等其他遥感数据模态的适用性尚未验证。
*   **模型规模偏小**：当前仅基于 7B 模型，未探索更大参数量（如 13B、34B 或 72B）下该标记压缩策略的 scaling 表现。
*   **数据集偏差风险**：半自动标注部分仍依赖 GPT‑4o，可能引入语言模型固有的幻觉或分布偏移；人工标注部分由硕士研究生等众包完成，可能存在标注噪声。
*   **隐私与安全**：超高分辨率图像可能带来新的隐私风险（如顶视识别敏感设施细节），且高精度目标定位能力具备潜在的“双重用途”风险。
*   **未对比最新遥感专用方法**：基准表中的遥感专用模型仅 GeoChat，缺乏与其他较新 RS‑MLLM（如 EarthGPT、LHRS‑Bot）的直接对比。

（完）
