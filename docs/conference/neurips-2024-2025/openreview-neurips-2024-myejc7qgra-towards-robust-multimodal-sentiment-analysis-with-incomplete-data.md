---
title: Towards Robust Multimodal Sentiment Analysis with Incomplete Data
title_zh: 面向不完整数据的鲁棒多模态情感分析
authors: "Haoyu Zhang, Wenbin Wang, Tianshu Yu"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=mYEjc7qGRA"
tags: ["query:multi-modal"]
score: 6.0
evidence: 处理多模态学习中的不完整数据
tldr: 该文针对多模态情感分析中的数据缺失问题，提出语言主导的噪声抵抗学习网络LNLN，利用主导模态校正和基于主导模态的多模态学习模块，增强模型在缺失模态下的鲁棒性。实验验证了在不同缺失率下的有效性。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-myejc7qgra/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1442, \"height\": 742, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-myejc7qgra/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1459, \"height\": 742, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-myejc7qgra/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1311, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-myejc7qgra/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1453, \"height\": 445, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-myejc7qgra/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1456, \"height\": 550, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-myejc7qgra/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1437, \"height\": 563, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-myejc7qgra/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1447, \"height\": 2200, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-myejc7qgra/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1451, \"height\": 2200, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-myejc7qgra/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1457, \"height\": 2222, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-myejc7qgra/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1448, \"height\": 837, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1452, \"height\": 494, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1454, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1453, \"height\": 435, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1443, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1452, \"height\": 294, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1435, \"height\": 371, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1447, \"height\": 1125, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1456, \"height\": 278, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1311, \"height\": 443, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1456, \"height\": 2243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1442, \"height\": 1525, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1453, \"height\": 331, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1457, \"height\": 436, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1444, \"height\": 1658, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-myejc7qgra/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1444, \"height\": 941, \"label\": \"Table\"}]"
motivation: 多模态情感分析中模态缺失影响模型性能。
method: 提出LNLN网络，包含主导模态校正和多模态学习模块。
result: 随机缺失场景下鲁棒性显著提升。
conclusion: 语言主导方法有效应对数据不完整性。
---

## Abstract
The field of Multimodal Sentiment Analysis (MSA) has recently witnessed an emerging direction seeking to tackle the issue of data incompleteness. Recognizing that the language modality typically contains dense sentiment information, we consider it as the dominant modality and present an innovative Language-dominated Noise-resistant Learning Network (LNLN) to achieve robust MSA. The proposed LNLN features a dominant modality correction (DMC) module and dominant modality based multimodal learning (DMML) module, which enhances the model's robustness across various noise scenarios by ensuring the quality of dominant modality representations. Aside from the methodical design, we perform comprehensive experiments under random data missing scenarios, utilizing diverse and meaningful settings on several popular datasets (e.g., MOSI, MOSEI, and SIMS), providing additional uniformity, transparency, and fairness compared to existing evaluations in the literature. Empirically, LNLN consistently outperforms existing baselines, demonstrating superior performance across these challenging and extensive evaluation metrics.

---

## 论文详细总结（自动生成）

### 论文核心问题与整体含义
这篇论文聚焦于**多模态情感分析**领域中一个突出但研究不充分的难题：**数据不完整**情况下的鲁棒性。在真实应用场景中，由于传感器故障、自动语音识别错误等问题，视觉、音频或文本模态的数据经常会发生随机缺失，导致现有模型的性能大幅下降。

- **研究动机**：现有针对缺失数据的鲁棒MSA方法虽然存在，但它们的评估标准不统一、实验设定不够全面，阻碍了有效的比较与进展。
- **核心假设**：论文认为语言模态包含最密集的情感信息，因此将其视为**主导模态**。核心假设是：**如果能保证主导模态表征的完整性和高质量，模型的整体鲁棒性将得到显著提升**。

### 论文提出的方法论
该论文提出了一种名为**语言主导的噪声抵抗学习网络**的新模型。其核心思想是：在数据随机缺失时，利用音频和视觉模态的信息来**修正和增强**受损的语言模态特征，从而确保主导模态的质量。

模型主要由三个关键模块构成：

- **主导模态修正模块**：
  - **完整性检查**：使用一个编码器预测语言模态当前的信息完整度 `w`，并通过 L2 损失进行优化。
  - **代理主导特征生成**：一个生成器 `E_DFG` 以视觉和音频特征为输入，生成一个“代理”语言特征 `H¹ₚ`。同时，一个带有梯度反转层的判别器 `D` 试图区分真实的语言特征和生成的代理特征，两者进行**对抗学习**。这种机制迫使生成器创造出与视觉/音频模态不同、但又能有效补充语言信息的特征。
  - **特征修正**：最终，将原始语言特征 `H¹ₗ` 和代理特征 `H¹ₚ` 按照预测的完整度 `w` 进行加权融合，得到**修正后的主导特征** `H¹_d`。
  - **公式表示**：`H¹_d = (1 - w) * H¹ₚ + w * H¹ₗ`
- **基于主导模态的多模态学习模块**：
  - **自适应超模态学习**：在原有的ALMT架构基础上进行改进。该模块利用修正后的主导特征 `H¹_d` 计算查询向量，通过多头注意力机制从视觉和音频特征中查询有用的情感线索，形成“超模态”表征，从而避免引入与情感无关的噪声。
  - **融合与预测**：使用一个交叉Transformer对修正后的主导特征和超模态特征进行深度融合，并完成最终的情感预测。
- **重建器**：
  - 一个基于两层Transformer的重建器 `E_rec`。
  - 其任务是根据带噪声的输入 `U¹_m` 尝试重建出原始的完整特征 `U⁰_m`，并通过 L2 重建损失进行优化。这作为一个辅助任务，增强了模型对缺失信息的理解能力。

整个网络的训练由四个损失函数加权联合驱动：完整性检查损失 `L_cc`、对抗学习损失 `L_adv`、重建损失 `L_rec` 和情感预测损失 `L_sp`。

### 实验设计
- **数据集**：在三个广泛使用的多模态情感分析基准数据集上进行了验证：**MOSI**、**MOSEI** 和 **SIMS**。SIMS是一个中文数据集，有助于检验模型的跨语言能力。
- **模拟场景**：为了模拟数据不完整，实验随机擦除每个模态中**0% 到 90%**（以10%为步长）的信息。视觉和音频用零填充，文本用 `[UNK]` 标记填充。实验在不同缺失率下重复10次，并计算平均性能以评估模型的整体鲁棒性。
- **评估指标**：全面而严苛，涵盖了回归和分类两大方面，包括七分类准确率（Acc-7）、五分类准确率（Acc-5）、二分类准确率（Acc-2）和F1分数、平均绝对误差（MAE）以及相关系数（Corr）。
- **对比方法**：与多类代表性基线方法进行了比较：
  - **上下文建模方法**：MISA、Self-MM、MMIM、CENET、TETFN、ALMT。
  - **噪声感知方法**：TFR-Net。

### 资源与算力
论文明确说明了实验的计算资源：
- **框架**：PyTorch 2.2.1。
- **硬件**：一台配备 **AMD EPYC 7513 CPU** 和单张 **NVIDIA Tesla A40 GPU** 的个人电脑。
- **复现性**：为公平比较，所有方法的实验均使用固定的随机种子（1111, 1112, 1113）各跑三次。作者公开了代码。

### 实验数量与充分性
这项工作的实验设计非常全面和充分，力求客观公平：

1.  **主实验**：在3个数据集上，对比了8种方法，每种方法在10个不同缺失等级下测试，并根据回归和分类指标分别挑选最优模型，统计了均值和标准差，提供了详尽的鲁棒性对比。
2.  **消融实验**：
    - **组件消融**：在MOSI和SIMS上，依次移除DMC模块、重建器和DMML模块（替换为简单拼接），并测试了不使用带噪数据训练的情况。
    - **正则化项消融**：在MOSI和SIMS上，依次移除 `L_cc`、`L_adv`、`L_rec` 三个损失项。
3.  **模态消融**：在MOSI上，分别移除语言、音频、视觉模态，验证了语言模态的主导作用。
4.  **泛化性分析**：进一步在“模态完全缺失”这个特殊但更苛刻的场景下评估了模型的泛化能力。
5.  **深入分析**：提供了数据分布可视化、混淆矩阵、特征可视化、稳定性分析及案例研究，从多个维度剖析了模型行为。

### 论文的主要结论与发现
- **LNLN性能优越**：在绝大多数评估指标和缺失率下，LNLN均优于现有基线模型，尤其在高缺失率场景中，其优势更为明显。
- **现有模型存在“懒惰”行为**：论文揭示了一个重要发现：在高噪声（如缺失率>=0.9）下，许多现有方法（如Self-MM, MISA等）会表现出严重的“懒惰”行为，即无视输入，将所有预测偏向训练集中样本数最多的某一类别，从而获得虚高的准确率。LNLN这种行为相对较轻，表明它仍在尝试从受损数据中提取信息。
- **各组件不可或缺**：消融实验证明，LNLN的三个核心模块（DMC, DMML, 重建器）及各个正则化损失项都对模型的鲁棒性有积极贡献，且带噪数据的训练至关重要。
- **语言模态至关重要**：移除语言模态会导致性能断崖式下跌，进一步验证了语言作为主导模态的假设。但视觉和音频信息作为补充也同样重要。

### 优点
- **方法创新性强**：明确地以保护和增强“主导模态”为核心思想，设计了精巧的完整性检查和对抗性特征生成机制，为噪声鲁棒MSA提供了新的有效范式。
- **评估体系全面、公平、深刻**：这是论文的一大亮点。它不仅设置了多维度、多缺失率的系统性评估，还通过混淆矩阵等方式深度揭示了现有方法的“懒惰”预测问题，对领域发展具有重要参考价值。
- **分析与可视化丰富**：通过特征分布可视化、混淆矩阵和案例研究，对模型行为进行了直观且深入的解释，增强了论文的可信度和洞察力。

### 不足与局限
- **多场景泛化能力有限**：作者承认，LNLN在“模态完全缺失”这一特殊场景下并非总是最优，表明其在不同类型噪声场景间的泛化能力有待提升。
- **现实世界复杂性考量不足**：实验基于随机缺失的模拟，而真实世界的数据不完整可能更复杂，伴随多种噪声、文化差异和行为模式影响，模型的适用性有待验证。
- **超参数敏感**：损失函数的权重 `α, β, γ, δ` 是根据经验设定的，且在不同数据集上有所不同，调参可能具有挑战性。
- **未在所有指标上全面领先**：在类别极度不均衡的数据集（如MOSEI）上，部分指标略逊于其他方法，模型在对抗数据不平衡方面仍有改进空间。

（完）
