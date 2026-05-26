---
title: Incomplete Multi-view Deep Clustering with Data Imputation and Alignment
title_zh: 不完全多视图深度聚类中的数据填补与对齐
authors: "Jiyuan Liu, Xinwang Liu, Xinhang Wan, KE LIANG, Weixuan Liang, Sihang Zhou, Huijun Wu, Kehua Guo"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=qUnjCEcN6S"
tags: ["query:multi-modal"]
score: 7.0
evidence: 使用数据填补的不完全多视图深度聚类方法处理缺失模态
tldr: 针对不完全多视图数据中缺失观测和相似度利用不足的问题，提出一种带数据填补和对齐的深度聚类方法。该方法同时进行缺失数据插补和潜表示对齐，更好地利用成对相似度。在多个多视图数据集上实现了优于现有方法的聚类性能，为解决缺失模态下的多源数据聚类提供了新思路。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-qunjcecn6s/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1425, \"height\": 676, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qunjcecn6s/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1452, \"height\": 389, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qunjcecn6s/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1458, \"height\": 363, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-qunjcecn6s/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1446, \"height\": 1156, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qunjcecn6s/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1432, \"height\": 1158, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qunjcecn6s/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 928, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qunjcecn6s/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1168, \"height\": 371, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qunjcecn6s/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1445, \"height\": 1155, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qunjcecn6s/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1430, \"height\": 1157, \"label\": \"Table\"}]"
motivation: 现有多视图聚类未有效利用缺失数据的成对相似度，影响性能。
method: 结合数据插补与表示对齐，同时恢复缺失观测并优化聚类表示。
result: 在多个基准上，聚类精度显著超过现有不完全多视图方法。
conclusion: 为处理缺失模态的多源数据聚类提供了有效方案。
---

## Abstract
Incomplete multi-view deep clustering is an emerging research hot-pot to incorporate data information of multiple sources or modalities when parts of them are missing. Most of existing approaches encode the available data observations into multiple view-specific latent representations and subsequently integrate them for the next clustering task. However, they ignore that the latent representations are unique to a fixed set of data samples in all views. Meanwhile, the pair-wise similarities of missing data observations are also failed to utilize in latent representation learning sufficiently, leading to unsatisfactory clustering performance. To address these issues, we propose an incomplete multi-view deep clustering method with data imputation and alignment. Assuming that each data sample corresponds to a same latent representation among all views, it projects the latent representations into feature spaces with neural networks. As a result, not only the available data observations are reconstructed, but also the missing ones can be imputed accordingly. Moreover, a linear alignment measurement of linear complexity is defined to compute the pair-wise similarities of all data observations, especially including those of the missing. By executing the above two procedures iteratively, the discriminative latent representations can be learned and used to group the data into categories with off-the-shelf clustering algorithms. In experiment, the proposed method is validated on a set of benchmark datasets and achieves state-of-the-art performances.

---

## 论文详细总结（自动生成）

好的，根据您提供的论文内容和要求，以下是对论文《Incomplete Multi-view Deep Clustering with Data Imputation and Alignment》的结构化深入总结。

### 论文核心问题与研究动机

*   **核心问题**：在不完全多视图数据（即部分视图的观测数据完全缺失）场景下，如何有效整合多源信息以提升聚类性能。
*   **研究动机与现有方法局限**：
    *   当前多数不完全多视图深度聚类方法通常为每个视图学习特定的潜在表示，然后进行融合。这种做法忽略了同一个数据样本在不同视图下其内在的、唯一的潜在结构应保持不变的特性。
    *   现有方法主要关注如何整合**现有**的可用数据观测，但未能充分挖掘和利用**缺失数据观测之间**的成对相似性信息，这限制了聚类性能的进一步提升。
    *   本文旨在解决上述两个局限性，通过学习一个视图间共享的唯一潜在表示，并利用数据填补和表示对齐技术，来同时利用可用数据和缺失数据的相似性信息。

### 方法论

*   **核心思想**：提出一种名为“带数据填补与对齐的不完全多视图深度聚类”方法。其核心假设是每个数据样本在所有视图下共享一个唯一且不变的潜在表示。模型通过将这一共享潜在表示投影到各视图特征空间，同时实现数据重构、缺失数据填补，并对齐潜在表示与完整数据的相似性。
*   **关键技术细节与流程**：
    1.  **数据重构与填补**：
        *   **前向投影**：模型学习一个共享的潜在表示矩阵 `Z`，并用 `V` 个独立的神经网络（解码器）`g_Θv(Z)` 将其分别投影回 `V` 个视图的特征空间，生成重构数据 `X̂(v)`。
        *   **重构损失 (`Lr`)**：通过计算重构数据 `X̂(v)` 与**可用**观测数据 `X(v)` 之间的均方误差来训练网络。
        *   **数据填补 (`X̄(v)`)**：对于缺失的观测数据，直接将神经网络的输出（即重构数据）`X̂(v)` 作为其填补值，从而构造出完整的视图数据 `X̄(v)`。
    2.  **数据对齐**：
        *   **线性对齐测量**：定义了一种名为“线性对齐”的度量，用于衡量两个矩阵（此处为潜在表示矩阵 `Z` 和填补后的完整视图数据矩阵 `X̄(v)`）之间成对线性相似度的一致性。其计算复杂度为 `O(N)`，与样本数呈线性关系。
        *   **对齐损失 (`La`)**：旨在最大化潜在表示 `Z` 与每个填补完整视图 `X̄(v)` 之间的线性对齐得分，从而利用所有数据（包括缺失部分）的成对相似性来正则化潜在表示的学习。
        *   **自适应视图加权**：引入可学习参数 `w_v` 来平衡不同视图的对齐损失贡献，这些权重根据各视图的对齐损失值动态调整，而非预设超参数。
    3.  **总体优化**：
        *   总损失函数为 `L = Lr + β * La`，其中 `β` 为平衡超参数。
        *   模型通过交替优化策略，使用Adam优化器更新神经网络参数和共享潜在表示 `Z`，并通过Cauchy-Schwarz不等式推导出视图权重 `w_v` 的闭式解。

### 实验设计与对比

*   **数据集**：在4个广泛使用的多视图基准数据集上进行验证：
    *   **HandWritten** (2000个样本, 6视图, 10类)
    *   **Caltech5V** (1400个样本, 5视图, 7类)
    *   **Flower17** (1360个样本, 7视图, 17类)
    *   **MSRCV1** (210个样本, 6视图, 7类)
*   **数据缺失设置**：按照通用策略，随机选择 `m` 比例（m ∈ {0.1, 0.3, 0.5, 0.7, 0.9}）的样本，并使其至少缺失一个视图，以此模拟不完全数据场景。
*   **对比方法**：与5种最新的不完全多视图深度聚类方法进行比较，包括：
    *   DITA-IMVC
    *   DSIMVC
    *   DCP
    *   DVIMVC
    *   CPSPAN
*   **评估指标**：采用四个常用聚类性能指标：准确率、归一化互信息、纯度和调整兰德指数。

### 资源与算力

*   **硬件环境**：实验在一台配置有 **2块 NVIDIA GeForce RTX 3090 GPU** 和 **40个 Intel(R) Xeon(R) Silver 4210R CPU @ 2.40GHz** 的服务器上运行。
*   **软件环境**：Python 3.10.13, PyTorch 1.12.1, CUDA 11.4。
*   **训练细节**：使用Adam优化器，学习率设置为0.001。模型为每个数据集设计了不同神经元数量的全连接网络。唯一的超参数 `β` 在 `{0.01, 0.1, 1, 10, 100}` 范围内网格搜索。论文未明确提及单次或总体的训练时长。

### 实验数量与充分性评估

*   **实验组数**：
    *   **主实验对比**：在4个数据集 × 5种缺失比例 × 4种评估指标的组合下，与5种baseline方法进行了全面比较。
    *   **消融实验**：为验证数据填补和对齐两个核心模块的有效性，设计了丰富的消融实验，包括：
        *   替换填补策略（用均值、零值、随机值填补，以及完全不填补）。
        *   完全移除对齐模块（`β=0`）。
    *   **参数敏感性分析**：分析了唯一超参数 `β` 在不同数据集和缺失比例下的性能影响。
*   **实验公平性**：
    *   所有对比方法均使用作者公开的官方代码，并进行网格搜索以报告最优结果，确保了比较的公平性。
    *   所有方法均多次运行并报告平均结果以消除随机性影响。
    *   实验覆盖了多样的数据集和极限缺失率（高达90%），并进行了充分的消融和参数分析，整体实验设计客观、严谨、充分。

### 主要结论与发现

*   **性能优越性**：提出的方法在几乎所有数据集和缺失比例下都取得了最优的聚类性能，尤其在平均准确率和NMI上均有显著提升。
*   **模块有效性（消融实验）**：
    *   **数据填补模块有效**：与使用均值、零值、随机值填补或完全不填补相比，所提出的基于投影的填补策略能够大幅提升性能，且缺失比例越高，优势越明显。
    *   **数据对齐模块有效**：移除数据对齐损失后，性能普遍下降，证明了利用缺失数据成对相似性进行正则化的必要性。
    *   **协同效应**：同时使用填补和对齐，比只利用可用数据（完全不填补）效果更好，证明了利用缺失数据相似性对学习高质量潜在表示至关重要。
*   **收敛性**：理论分析和实验曲线均表明，算法能单调递减损失并最终收敛。聚类性能随训练提升并趋于稳定。

### 优点（亮点）

*   **新颖的视角**：将传统“数据编码为表示”的范式转变为“表示投影为数据”，自然而然地统一了数据重构和缺失填补。
*   **高效的度量**：提出的线性对齐测量能以线性计算复杂度 `O(N)` 有效地利用缺失数据的相似性信息，这是一个兼具理论意义和计算效率的亮点。
*   **自适应加权**：为不同视图的损失自动分配权重，避免了繁琐的超参数调优，增强了模型的鲁棒性。
*   **实验设计严谨**：在多个数据集和高缺失率下，与最新的方法进行了全面、公平的比较，并通过详尽的消融实验充分验证了所提模块的有效性。

### 不足与局限

*   **潜在表示约束不足**：论文自身在结论部分指出，方法可能因缺乏对共享潜在表示的充分约束（如聚类结构先验），而存在性能提升瓶颈。这是主要的局限性。
*   **实验覆盖有限**：
    *   所使用的神经网络结构仅限于全连接网络，未探讨ConvNets、GCNs或Transformers等其他主流架构。
    *   数据集规模相对较小（最大2000样本），缺乏在大规模数据集上的验证，其线性计算复杂度的优势未能在大规模场景下得到充分体现。
    *   未与基于核方法、子空间方法等传统不完全多视图聚类方法进行对比。
*   **填补质量未量化**：论文虽提出数据填补，但实验仅从最终聚类精度间接证明了其有效性，并未直接评估填补数据本身与真实值的差异或质量。
*   **超参数敏感性**：虽然只有一个超参数 `β`，但参数分析显示，性能对 `β` 的选择较为敏感（尤其是在`β`较大时性能下降），实际应用中可能需要仔细调整。

（完）
