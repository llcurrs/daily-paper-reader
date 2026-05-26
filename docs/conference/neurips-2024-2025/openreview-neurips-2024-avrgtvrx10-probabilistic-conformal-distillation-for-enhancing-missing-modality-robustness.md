---
title: Probabilistic Conformal Distillation for Enhancing Missing Modality Robustness
title_zh: 面向缺失模态鲁棒性的概率共形蒸馏
authors: "mengxi Chen, Fei Zhang, Zihua Zhao, Jiangchao Yao, Ya Zhang, Yanfeng Wang"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=AVrGtVrx10"
tags: ["query:multi-modal"]
score: 7.0
evidence: 基于概率共形蒸馏的缺失模态鲁棒学习框架
tldr: 针对多模态模型在测试时模态缺失导致性能下降的问题，提出概率共形蒸馏方法，通过概率分布对齐而非确定性对齐来处理信息不对称。该方法学习缺失模态输入的未知概率密度函数，并利用共形预测区间实现鲁棒对齐。在多个多模态基准上证明能有效提升缺失模态下的鲁棒性，为多模态学习提供了泛用的不确定性建模方案。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-avrgtvrx10/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 779, \"height\": 316, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-avrgtvrx10/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1454, \"height\": 371, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-avrgtvrx10/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 808, \"height\": 341, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-avrgtvrx10/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 800, \"height\": 322, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-avrgtvrx10/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1438, \"height\": 345, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-avrgtvrx10/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 787, \"height\": 572, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-avrgtvrx10/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1438, \"height\": 1445, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-avrgtvrx10/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 940, \"height\": 244, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-avrgtvrx10/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 948, \"height\": 205, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-avrgtvrx10/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 728, \"height\": 273, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-avrgtvrx10/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1368, \"height\": 239, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-avrgtvrx10/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1447, \"height\": 726, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-avrgtvrx10/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1225, \"height\": 600, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-avrgtvrx10/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1413, \"height\": 781, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-avrgtvrx10/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1102, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-avrgtvrx10/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1294, \"height\": 326, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-avrgtvrx10/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1422, \"height\": 826, \"label\": \"Table\"}]"
motivation: 现有知识蒸馏方法在模态缺失情况下强制对齐导致虚假特征学习。
method: 提出概率共形蒸馏，建模缺失模态的不确定性并学习概率密度函数。
result: 在多种模态缺失基准上，方法显著提升模型鲁棒性。
conclusion: 为缺失模态学习提供了有效的不确定性建模思路。
---

## Abstract
Multimodal models trained on modality-complete data are plagued with severe performance degradation when encountering modality-missing data. Prevalent cross-modal knowledge distillation-based methods precisely align the representation of modality-missing data and that of its modality-complete counterpart to enhance robustness. However, due to the irreparable information asymmetry, this determinate alignment is too stringent, easily inducing modality-missing features to capture spurious factors erroneously. In this paper, a novel multimodal Probabilistic Conformal Distillation (PCD) method is proposed, which considers the inherent indeterminacy in this alignment. Given a modality-missing input, our goal is to learn the unknown Probability Density Function (PDF) of the mapped variables in the modality-complete space, rather than relying on the brute-force point alignment. Specifically, PCD models the modality-missing feature as a probabilistic distribution, enabling it to satisfy two characteristics of the PDF. One is the extremes of probabilities of modality-complete feature points on the PDF, and the other is the geometric consistency between the modeled distributions and the peak points of different PDFs. Extensive experiments on a range of benchmark datasets demonstrate the superiority of PCD over state-of-the-art methods. Code is available at: https://github.com/mxchen-mc/PCD.

---

## 论文详细总结（自动生成）

### 论文核心问题与整体含义
本研究聚焦于**多模态学习中的缺失模态鲁棒性**问题。
*   **研究背景**：传统多模态模型假设训练和测试时所有模态数据均完整。然而，在实际应用中因设备限制、成本等因素，经常出现部分模态缺失的情况，导致模型性能急剧下降。
*   **现有方法局限**：主流的统一建模方法（尤其是基于跨模态知识蒸馏KD的方法）通过强制将缺失模态的表示与完整模态的表示进行精确（确定性的）对齐来提升鲁棒性。
*   **核心问题与动机**：由于模态缺失导致的不可修复的**信息不对称**，这种确定性的对齐过于严苛，会错误地迫使缺失模态的特征去拟合一些虚假的、与任务无关的因子，反而损害模型性能。
*   **论文含义**：提出一种新的视角，即缺失模态的表示与其完整模态对应物之间并非确定性关系，而是一种概率性关系。因此，应从概率分布对齐的角度，以更宽容的方式迁移特权信息。

### 论文提出的方法论
论文提出了一种名为**概率共形蒸馏 (Probabilistic Conformal Distillation, PCD)** 的新方法，其核心思想、关键技术细节如下：
*   **核心思想**：不强制缺失模态特征点精确对齐到完整模态特征点，而是学习缺失模态输入在完整模态表示空间中映射变量的**概率密度函数 (PDF)**。该PDF应满足两个特性：1) 在完整模态特征点附近概率高，远离处概率低（极值特性）；2) 不同样本分布的最高点之间的几何关系与它们完整模态特征点之间的几何关系保持一致（共形特性）。
*   **概率建模**：将每个缺失模态输入表示的均值向量和方差向量参数化为一个独立的高斯分布 $\mathcal{N}(\mathbf{z}_i; \mu_i, \sigma^2_i)$。
*   **损失函数**：优化由两部分组成的损失函数来拟合PDF：
    1.  **概率极值损失 $\mathcal{L}_u$**：最大化正样本（同类/同实例完整模态特征）在分布上的对数概率，同时最小化负样本的概率。这鼓励了均值接近正样本，并根据距离自适应地学习方差。
    2.  **几何一致性损失 $\mathcal{L}_g$**：基于对比学习的框架，计算不同样本分布峰值点（即 $\mu_i$）之间的距离向量 $\mathbf{g}_i$，并与完整模态特征点之间的距离向量 $\mathbf{g}^*$ 进行对齐。最大化正样本对 $\mathbf{g}_i$ 和 $\mathbf{g}^*_p$ 的相似度。
*   **训练流程**：采用自知识蒸馏架构。先在热身阶段用完整数据训练一个教师模型，然后固定教师模型参数，指导学生模型（两者结构相同）在所有可能的模态缺失组合下进行训练，总损失为任务损失、$\mathcal{L}_u$ 和 $\mathcal{L}_g$ 的加权和。

### 实验设计
实验设计全面，覆盖了分类和分割两大任务，具体如下：
*   **数据集与场景**：
    *   **分类任务**：在人脸反欺诈数据集上进行，包括 **CASIA-SURF** 和 **CeFA**。这两个数据集均为三模态（RGB, Depth, IR），协议严格，模拟了7种模态缺失/完整组合。
    *   **分割任务**：在语义分割数据集上进行，包括室内的 **NYUv2** 和室外城市场景的 **Cityscapes**。均为双模态（RGB, Depth），模拟了3种组合。
    *   **扩展评测**：在 **SUN RGB-D** 数据集上验证了分割性能，并在训练数据本身也模态缺失的场景下评测了方法的可扩展性。
*   **对比方法**：与多个类别的基线方法进行了比较，包括：
    *   **基线方法**：仅在完整数据上训练的传统模型 (Traditional)、为每种缺失组合单独训练模型 (Separate Model)。
    *   **冗余性方法**：数据增强 (Augmentation)、MMFormer。
    *   **基于蒸馏的KD方法**：MMANET。
    *   **动态融合方法**：MD, ETMC, RAML。
*   **评价指标**：分类任务使用**平均分类错误率 (ACER)**；分割任务使用**平均交并比 (mIOU)**。

### 资源与算力
*   论文中**未明确说明**所使用的具体GPU型号、数量及训练总时长。仅在附录中提及使用SGD或Adam优化器，并设定了批次大小（64或16）和总训练轮数（如450 epochs），可根据此大致推断所需算力，但缺乏精确资源报告。

### 实验数量与充分性
实验数量充足，设计充分且客观公平，能够有力支撑其主张。
*   **主要对比实验**：在4个主流基准数据集上，与至少6种不同的SOTA方法进行了全面比较，覆盖了所有可能的模态缺失组合。
*   **消融实验**：设计了多项消融研究，以验证各模块的有效性，包括：
    *   对损失函数各组件 ($\mathcal{L}_c, \mathcal{L}_u, \mathcal{L}_g$)的分离验证。
    *   对概率蒸馏 vs. 确定性蒸馏的对比。
    *   对自KD策略 vs. 预训练教师KD策略的对比。
*   **参数敏感性分析**：分析了关键超参数 $\lambda$ 和 $\tau$ 在不同取值下的性能稳定性。
*   **泛化性与鲁棒性测试**：
    *   在更大规模的数据集 (SUN RGB-D) 上进行测试。
    *   模拟训练数据部分缺失的 “不完美” 场景进行测试。
    *   对模型进行了稳定性实验（3次重复运行），报告了均值和标准差。
    *   分析了教师和学生模型的分类边界、特征分布可视化（t-SNE）。
    *   对比了不同方法的参数量和FLOPs，论证了其轻量性。

### 论文的主要结论与发现
*   PCD方法在多个模态缺失鲁棒性基准测试中，几乎在所有场景下都取得了**最优性能 (SOTA)**，显著优于现有方法。例如，在CeFA数据集上平均错误率降低了5.31%。
*   概率性对齐相比传统的确定性对齐，是处理模态间信息不对称的更有效、更宽容的方式，能有效防止模型拟合虚假特征。
*   通过自知识蒸馏框架和概率分布建模，PCD能高效地将完整模态的特权信息传递给学生模型，使缺失模态下的特征表示更具判别力。

### 优点
*   **问题视角新颖**：从概率分布对齐的角度切入，抓住了模态缺失问题中信息不对称的核心矛盾，思想深刻。
*   **方法论扎实**：通过建模高斯分布并联合优化概率极值和几何结构，设计精巧，理论动机清晰，实现为简洁的损失函数，易于复现和应用。
*   **实验全面且说服力强**：覆盖了分类和分割、小规模和大规模、室内和室外场景，进行了丰富的消融、对比和可视化分析，论证严谨。
*   **即插即用**：作为轻量化模块，该方法仅增加少量参数即可接入现有的多模态融合框架。

### 不足与局限
*   **训练数据假设较强**：方法的核心依赖于有完整模态的教师模型进行蒸馏，这在训练数据本身也存在模态缺失的场景下，PCD只能应用于有完整对应数据的部分子集，虽展现出一定的可扩展性，但并非其本质设计，性能增益理论上会受限。
*   **PDF建模简化**：假设映射变量的PDF为高斯分布，虽然有效且方便计算，但可能无法完全捕捉真实复杂场景下的分布形态。
*   **缺乏理论证明**：关于概率分布对齐的收敛性和存在性，论文主要基于直觉和实验验证，缺乏严格的理论证明（如论文在检查清单中所述）。
*   **评测模态类型有限**：实验基于视觉模态（RGB、深度、红外），在更稀疏或更异构模态（如文本、音频）组合上的效果有待进一步验证。

（完）
