---
title: Deep Correlated Prompting for Visual Recognition with Missing Modalities
title_zh: 面向缺失模态的深度相关提示学习视觉识别
authors: "Lianyu Hu, Tongkai Shi, Wei Feng, Fanhua Shang, Liang Wan"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=zO55ovdLJw"
tags: ["query:multi-modal"]
score: 8.0
evidence: 使用提示学习处理视觉识别中的缺失模态
tldr: 大规模多模态模型在模态缺失时性能显著下降。本文提出深度相关提示学习方法，通过构建跨模态相关的提示嵌入，动态适应不同缺失模态输入模式，从而无需重新训练即可提升模型在缺失模态下的视觉识别能力。实验表明，该方法在多种缺失设置下均取得领先结果，为高效处理缺失模态问题提供了新的范式。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-zo55ovdljw/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1298, \"height\": 824, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-zo55ovdljw/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1452, \"height\": 896, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-zo55ovdljw/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1429, \"height\": 431, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-zo55ovdljw/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1445, \"height\": 413, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-zo55ovdljw/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 665, \"height\": 474, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-zo55ovdljw/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 462, \"height\": 381, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-zo55ovdljw/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 956, \"height\": 381, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-zo55ovdljw/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1440, \"height\": 1072, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-zo55ovdljw/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 782, \"height\": 426, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-zo55ovdljw/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 809, \"height\": 426, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-zo55ovdljw/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 804, \"height\": 107, \"label\": \"Table\"}]"
motivation: 预训练多模态模型假设模态完整，但实际中模态缺失导致性能严重退化。
method: 提出深度相关提示学习，利用跨模态相关性生成自适应提示，根据缺失情况动态调整。
result: 在多个视觉识别任务上，本方法在模态缺失设置下大幅超越基线，展现了鲁棒性和灵活性。
conclusion: 为多模态模型在真实缺失模态场景下的高效适应提供了一种无需重新训练的解决方案。
---

## Abstract
Large-scale multimodal models have shown excellent performance over a series of tasks powered by the large corpus of paired multimodal training data. Generally, they are always assumed to receive modality-complete inputs. However, this simple assumption may not always hold in the real world due to privacy constraints or collection difficulty, where models pretrained on modality-complete data easily demonstrate degraded performance on missing-modality cases. To handle this issue, we refer to prompt learning to adapt large pretrained multimodal models to handle missing-modality scenarios by regarding different missing cases as different types of input. Instead of only prepending independent prompts to the intermediate layers, we present to leverage the correlations between prompts and input features and excavate the relationships between different layers of prompts to carefully design the instructions. We also incorporate the complementary semantics of different modalities to guide the prompting design for each modality. Extensive experiments on three commonly-used datasets consistently demonstrate the superiority of our method compared to the previous approaches upon different missing scenarios. Plentiful ablations are further given to show the generalizability and reliability of our method upon different modality-missing ratios and types.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **背景**：大规模多模态预训练模型（如 CLIP）依赖成对的模态完整数据（图文对）取得优异性能，但现实中因隐私、采集难度等原因常出现模态缺失（纯文本、纯图像或二者皆缺），导致模型性能严重下降。
- **核心挑战**：
  - 任何模态在训练或测试阶段均可能缺失，且缺失类型、缺失比例不固定。
  - 现有缺失模态处理方法多需更新大量模型参数，计算开销大，且多假设缺失类型已知。
- **研究目标**：提出一种参数高效的方法，通过可学习的提示（prompt）自适应地调整预训练多模态模型，使其对缺失模态具有鲁棒性，同时保持骨干网络冻结，仅微调少量额外参数。

## 2. 提出的方法论

### 2.1 整体思路
- 将不同缺失情况（完整、缺文本、缺图像）视为不同输入类型，为每种类型设计一组可学习的提示。
- 提示插入到图像编码器和文本编码器的输入嵌入及中间层特征前，引导模型处理缺失。
- 骨干网络冻结，仅更新提示参数和最终分类层，实现高效微调。

### 2.2 核心技术细节：三种提示设计

1. **相关提示（Correlated Prompts）**
   - 不同层的提示不应独立，需利用层间相关性。
   - 当前层提示由前一层提示经瓶颈 MLP（GELU + LayerNorm）生成，提升信息继承。
   - 同时融合另一模态对应层的提示，使跨模态信息互补：
     - 以图像编码器为例，第 $i$ 层提示 $P_{m,i}^{I,R} = \mathcal{F}_{i-1}^{I}(\text{Concat}(P_{m,i-1}^{I,R}, P_{m,i-1}^{T,R}))$，其中 $\mathcal{F}$ 为残差 MLP。

2. **动态提示（Dynamic Prompts）**
   - 固定提示无法适应不同样本特征，因此根据输入特征动态生成。
   - 使用单头自注意力层处理输入嵌入后得到动态提示，长度与原始提示相同。
   - 动态提示仅插入输入层，后续层保留并通过网络传播。

3. **模态共有提示（Modal-Common Prompts）**
   - 多模态输入包含共有语义和模态特有语义，将提示分解为模态共有部分和模态特有部分。
   - 引入一个共享的模态共有提示 $P_m^C$，通过线性投影 $\mathcal{G}^T$、$\mathcal{G}^I$ 映射到文本、图像空间，分别得到 $P_m^{T,C}$、$P_m^{I,C}$。
   - 模态共有提示仅插入输入层，使每个编码器在保留特有信息的同时吸收共有知识。

### 2.3 算法流程
- 给定样本 $(x_{m1}, x_{m2})$ 和缺失类型 $m \in \{c, m1, m2\}$，选择对应提示。
- 提示由相关提示（$P^{R}$）、动态提示（$P^{D}$）和模态共有提示（$P^{C}$）拼接而成，预置在输入 token 序列前。
- 经过冻结的编码器前向传播，最终取任务相关 token（如 [CLS]）拼接后送入分类头。
- 训练时仅优化提示参数和分类头。

## 3. 实验设计

- **数据集**：
  - MM-IMDb：电影类型多标签分类，F1-Macro 评价。
  - UPMC Food-101：食物分类，Top-1 准确率。
  - Hateful Memes：仇恨表情检测，AUROC 评价。
- **缺失模态设定**：
  - 缺失率 $\eta$ 表示模态不完整数据的比例，默认 $\eta=70\%$。
  - 三种缺失情形：缺文本、缺图像、两者皆缺（missing-both）。
- **对比方法**：
  - Baseline：缺失模态特征直接置零。
  - CoOp：仅输入级提示。
  - MMP：逐层独立提示。
  - MaPLe：跨层跨模态提示生成。
  - DePT：解耦提示。
- **骨干网络**：CLIP (ViT-B/16)，保持冻结。

## 4. 资源与算力

- 实验均在单块 NVIDIA 3090 GPU 上进行。
- Batch size = 4，优化器为 Adam（学习率 1e-2，权重衰减 2e-2），学习率预热后线性衰减。
- 额外参数量约 4.0M，占冻结骨干（151M）的 2.4%，训练高效。

## 5. 实验数量与充分性

- **主要实验**：
  - 不同缺失率（0%~100%）下的性能曲线，三种缺失情形各含多组实验。
  - 三个数据集、三种缺失率（50%、70%、90%）与多种方法的全面对比。
- **消融实验**：
  - 三种提示组件的有效性逐一验证。
  - 相关提示的层数、生成函数、跨模态融合方式。
  - 动态提示的插入深度、生成函数（注意力、池化等）。
  - 模态共有提示的投影方式、深度、缩减因子。
  - 提示长度的影响。
  - 与 MMP 在等参数量下的对比。
- **泛化性实验**：
  - 训练与测试缺失类型不匹配（如训练 missing-both，测试 missing-image）。
- **模型兼容性实验**：方法迁移至 CoCa、ViLT 等其他多模态框架。
- **完备性实验**：训练集为完整数据但在训练时随机模拟缺失。

总体实验设计全面，覆盖多种缺失比例、类型、数据集和变量，与最新方法公平比较，消融充分，结论客观可靠。

## 6. 主要结论与发现

- 提出的深度相关提示学习方法在所有缺失场景和缺失比例下均显著优于基线和其他提示方法，验证了利用相关性、动态性和模态共有分解的有效性。
- 相关提示带来的提升最大，动态提示和模态共有提示可进一步叠加增益。
- 模型对训练时见过的缺失类型更鲁棒，但在 missing-both 训练后泛化性最强。
- 文本缺失对 MM-IMDb 和 Food101 影响更大，而 Hateful Memes 对图像缺失更敏感。
- 方法参数高效，仅增加极少计算量即可大幅提升鲁棒性。

## 7. 优点

- 创新性：首次系统地设计了层内相关、动态生成和模态分解的提示机制，充分挖掘提示潜能。
- 高效性：冻结骨干，仅微调少量参数，训练开销小。
- 鲁棒性：在多种缺失类型、缺失比例和数据集上均取得领先，且泛化能力强。
- 可扩展性：可适配不同多模态架构（CLIP、CoCa、ViLT），且理论上可扩展至更多模态。

## 8. 不足与局限

- 仅在双模态（图文）和双流编码器上进行验证，未涉及更多模态或单流架构的深入测试（但附录有 ViLT 实验做部分补充）。
- 有些消融实验的指标差异较小，未报告误差棒或多次运行的统计显著性。
- 模态共有提示的分解依赖于人工划分，可能未最优地捕获跨模态共有语义。
- 未讨论大规模部署时的实际推理效率或压缩方案。
- 动态提示引入了额外注意力计算，虽在实验中影响不大，但可能影响极高吞吐场景的延迟。

（完）
