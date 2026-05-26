---
title: "HetSSNet: Spatial-Spectral Heterogeneous Graph Learning Network for Panchromatic and Multispectral Images Fusion"
title_zh: HetSSNet：用于全色与多光谱图像融合的空间-光谱异质图学习网络
authors: "Mengting Ma, Yizhen Jiang, Mengjiao Zhao, Jiaxin Li, Wei Zhang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=8EUR45XguK"
tags: ["query:multi-modal"]
score: 10.0
evidence: 基于空间-光谱异质图学习的遥感全色与多光谱图像融合
tldr: 针对遥感全色锐化中传统CNN和Transformer难以建模不规则地物的问题，提出空间-光谱异质图学习网络HetSSNet。该方法构建定制化图结构捕获空间光谱关系先验，并在图上学习融合表示。实验表明重建的高分辨率多光谱图像保留丰富细节和光谱信息，超越主流方法。工作为多模态遥感图像融合提供了新颖的图神经网络框架，对处理地理信息中的不规则对象具有重要价值。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-8eur45xguk/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1796, \"height\": 788, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-8eur45xguk/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1793, \"height\": 899, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-8eur45xguk/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1326, \"height\": 654, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-8eur45xguk/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1292, \"height\": 660, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-8eur45xguk/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1822, \"height\": 894, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-8eur45xguk/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1791, \"height\": 489, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-8eur45xguk/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1844, \"height\": 896, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-8eur45xguk/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 860, \"height\": 293, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-8eur45xguk/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1766, \"height\": 830, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-8eur45xguk/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 891, \"height\": 303, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-8eur45xguk/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 890, \"height\": 260, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-8eur45xguk/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 886, \"height\": 271, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-8eur45xguk/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1714, \"height\": 657, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-8eur45xguk/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1050, \"height\": 752, \"label\": \"Table\"}]"
motivation: 传统CNN和Transformer对遥感不规则地物建模存在局限。
method: 提出异质图学习网络，自定义图结构建模空间光谱关系。
result: 融合图像空间细节和光谱保真度优于现有方法。
conclusion: HetSSNet为多模态遥感图像融合提供了有效图学习方案。
---

## Abstract
Remote sensing pansharpening aims to reconstruct spatial-spectral properties during the fusion of panchromatic (PAN) images and low-
resolution multi-spectral (LR-MS) images, finally generating the high-resolution multi-spectral (HR-
MS) images. In the mainstream modeling strategies, i.e., CNN and Transformer, the input images are treated as the equal-sized grid of pixels in the Euclidean space. They have limitations in facing remote sensing images with irregular ground objects. Graph is the more flexible structure, however, there are two major challenges when modeling spatial-spectral properties with graph: 1) constructing the customized graph structure for spatial-spectral relationship priors; 2) learning the unified spatial-spectral representation through the graph. To address these challenges, we propose the spatial-spectral heterogeneous graph learning network, named HetSSNet.
Specifically, HetSSNet initially constructs the heterogeneous graph structure for pansharpening, which explicitly describes pansharpening-specific relationships. Subsequently, the basic relationship pattern generation module is designed to extract the multiple relationship patterns from the heterogeneous graph. Finally, relationship pattern aggregation module is exploited to collaboratively
learn unified spatial-spectral representation across different relationships among nodes with adaptive importance learning from local and global perspectives. Extensive experiments demonstrate the significant superiority and generalization of HetSSNet.

---

## 论文详细总结（自动生成）

好的，作为资深学术论文分析助手，我将使用中文，以 Markdown 形式，对提供的论文进行结构化、深入、客观的总结。

### 1. 论文的核心问题与整体含义

*   **研究背景与问题**：
    *   全色锐化旨在融合高空间分辨率的全色图像和低空间分辨率的多光谱图像，生成高分辨率多光谱图像。
    *   主流方法（如 CNN 和 Transformer）将图像视为欧氏空间中的像素网格，这对于遥感图像中形状不规则的地面物体（如森林、建筑、海洋）而言，建模方式不够灵活，是次优选择。
*   **核心挑战**：
    *   图结构虽然更灵活，但将其用于全色锐化面临两大挑战：
        1.  **图结构构建**：如何定制化地构建图结构，以显式描述全色锐化特有的空间-光谱关系先验。
        2.  **统一表示学习**：如何在此图结构上学习统一的空间-光谱表示，以平衡空间细节和光谱信息的重建。
*   **整体含义**：本论文旨在解决现有方法在处理不规则地物时的局限性，首次探索在非欧氏空间中使用图神经网络来学习统一的空间-光谱特征表示，以提升全色锐化的性能。

### 2. 论文提出的方法论

论文提出了一个名为 **HetSSNet** 的空间-光谱异质图学习网络，其核心思想是通过三个关键模块协同工作：

*   **核心思想**：构建一个能够显式描述全色、多光谱图像内部及之间多种关系的异质图，并在此图上学习包含局部和全局信息的统一空间-光谱表示。
*   **关键技术细节与流程**：
    1.  **空间-光谱异质图构建**：
        *   **节点定义**：将PAN图像和LR-MS图像的每个波段切分成块，转化为特征向量，作为图中两种不同类型的节点。
        *   **边关系定义**：为节点之间定义三种类型的边，分别描述：1）PAN图像自身的空间关系；2）LR-MS图像自身的波段内光谱关系；3）PAN与LR-MS图像间的跨模态光谱关系。边通过K近邻算法和余弦相似度建立。
    2.  **基本关系模式生成模块**：
        *   将构建好的异质图根据边的类型解耦为多个邻接矩阵。
        *   通过逻辑变量控制不同关系的有无，对邻接矩阵进行逻辑运算（XNOR和AND），生成最多 \(2^3-1=7\) 种“基本关系模式矩阵”，以充分挖掘图中潜在的复杂关系组合。
    3.  **关系模式聚合模块**：从局部和全局两个视角学习节点表示。
        *   **局部分支**：为不同的基本关系模式矩阵分配可学习的权重 \(\alpha_r\)，加权聚合后输入图卷积网络，学习包含局部复杂关系的节点特征。
        *   **全局分支**：计算每个节点“全局关系模式”的相似度矩阵，对具有相似全局模式的节点进行特征聚合。具体而言，它先为每种关系模式计算节点与所有其他节点的连接数，再通过可学习权重 \(\beta_i\) 拼接成全局模式矩阵，最终计算节点间的相似度后输入图卷积网络。
        *   **对比学习**：引入对比学习损失 \(L_{cl}\)，最大化同一个节点在局部和全局分支上学习到的表示的一致性，使两个分支协同监督。
*   **优化目标**：最终的损失函数为 L1 重建损失 \(L_1\) 和对比学习损失 \(L_{cl}\) 的加权和。

### 3. 实验设计

*   **数据集**：
    *   实验使用了三个广泛认可的遥感数据集：**WorldView-3**、**QuickBird** 和 **GaoFen-2**。
    *   数据生成严格遵循 Wald 协议。每个数据集包含了训练集和测试集，並明确了 LR-MS、PAN 和 HR-MS 图像的尺寸与比特深度。
*   **基准对比方法**：
    *   实验对比了两大类方法：
        1.  **传统方法**：SFIM， GS， BROVEY。
        2.  **基于学习的方法（14种）**：涵盖了CNN、Transformer、GCN、Mamba等近期主流架构，如 SRPPNN， DCFNet， CTINN， Hyperformer， MDCUN， GPCNet， FusionMamba 等。
*   **评估指标**：
    *   **降分辨率场景（有参考图像）**：使用了 PSNR， SSIM， SAM， ERGAS， SCC 五项指标。
    *   **全分辨率场景（无参考图像）**：使用了 Dλ， Ds， QNR 三项非参考指标。
*   **实验场景**：论文不仅评估了降分辨率下的性能，还在真实的全分辨率场景下验证了方法的泛化能力。

### 4. 资源与算力

*   论文明确给出了训练细节：
    *   **硬件**：实验在 4 块 NVIDIA RTX A6000 GPU 上运行。
    *   **框架**：基于 PyTorch 框架实现。
    *   **时长与参数**：不同数据集的训练迭代次数不同（30000或28000次），批量大小为4，使用 Adam 优化器，并给出了初始学习率和衰减策略。

### 5. 实验数量与充分性

*   **实验数量**：论文进行了非常全面的实验，主要分为以下几组，总数超过几十组：
    1.  **主实验**：在 3 个数据集上，与 17 种（3 种传统 + 14 种深度学习方法）进行定量和定性比较。
    2.  **消融实验**：为验证各个模块的有效性，设计了至少 4 组消融实验，包括：
        *   替换基本关系模式生成模块（+2组）。
        *   分别移除关系模式聚合模块的局部和全局分支（+2组）。
        *   调整图卷积聚合的层数（+4组）。
        *   调整损失函数中的超参数 γ（+4组）。
    3.  **泛化性实验**：在 3 个数据集共 60 张（3数据集 x 20张）未见过的全分辨率真实场景上进行了定量评估。
    4.  **扩展验证**：在8波段 WorldView-3 数据集上与 16 种方法进行比较。
*   **充分性、客观性与公平性**：
    *   **充分性**：实验设计非常扎实，覆盖了多个数据集、多种主流方法、充分的消融实验和泛化性测试，足以支撑其结论。
    *   **公平性**：文中明确指出所有对比方法均在所采用的数据集上重新训练，未直接使用原文数据，这一点保证了实验对比的公平性。Benchmark 的选择也涵盖了从传统到最新的、不同架构的方法，非常全面。

### 6. 论文的主要结论与发现

*   **性能优越**：HetSSNet 在三个数据集上几乎所有的定量指标中都取得了最佳或次佳的性能，特别是在 PSNR 和 SAM 指标上，表明其在空间细节重建和光谱保真度方面尤为突出。
*   **泛化能力强**：在真实全分辨率场景的无参考评价中，HetSSNet 同样表现出色，验证了其优越的泛化能力。
*   **建模方式有效**：消融实验证明了异质图结构、基本关系模式提取、以及从局部和全局视角进行关系聚合的设计均是有效的，对比学习能有效协调两个分支的学习。

### 7. 优点

*   **创新性强**：首次将异质图学习引入全色锐化任务，将图像处理从规则的欧氏空间拓展到更灵活的非欧氏空间，思路新颖。
*   **理论依据明确**：论文通过实验分析揭示了两种“关系先验”，并以此为基础设计图结构，使得模型设计有据可依，量身定制。
*   **模型设计精巧**：通过解耦和重组邻接矩阵生成基本关系模式，并从局部/全局、对比学习等多角度进行聚合，设计思路逻辑清晰，模块化好。
*   **实验扎实可靠**：充足的对比方法、全面的消融实验以及在真实场景下的泛化性验证，极大地增强了结果的可信度。

### 8. 不足与局限

*   **对传感器和处理流程的依赖性**：
    *   模型的超参数（如块大小、特征维度）可能针对实验中的特定传感器（如 WorldView-3）进行了优化，当应用于差异极大的新型传感器或不同处理级别的数据时，泛化能力需要重新评估。
*   **计算效率未深入探讨**：
    *   虽然附录中给出了复杂度分析，但图方法的建模和运算通常比规则网格的卷积计算开销更大。论文未提供与 CNN/Transformer 方法在推理速度、内存占用方面的详细对比，这对于实际部署至关重要。
*   **超参数敏感性**：除 `γ` 外，论文未探讨 KNN 中的 `k` 值、图卷积层数等超参数的敏感性，这些参数对最终构建的图结构和模型性能可能有显著影响。
*   **实验局限性**：
    *   论文仅在特定的、结构相对清晰的城市郊区场景数据集上验证，对于包含云、雾、雪等复杂大气条件，或大范围同质区域（如沙漠、海洋）的极端场景未进行测试。
    *   所有的“全分辨率”测试实际上仍是在卫星对同一地物区域的成像上进行的，属于同源测试，缺乏真正跨传感器、或针对全新区域的异源泛化测试。

（完）
