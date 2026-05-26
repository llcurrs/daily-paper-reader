---
title: "Bifurcate then Alienate: Incomplete Multi-view Clustering via Coupled Distribution Learning with Linear Overhead"
title_zh: 分叉后疏离：通过线性开销的耦合分布学习进行不完整多视图聚类
authors: "Shengju Yu, Yiu-ming Cheung, Siwei Wang, Xinwang Liu, En Zhu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=EFMAjY8dVZ"
tags: ["query:multi-modal"]
score: 7.0
evidence: 处理多视图聚类中的缺失模态
tldr: 针对现有不完整多视图聚类方法未能同时捕捉视角共享与特定特征的问题，BACDL算法通过分叉特征簇并施加疏离约束以增强簇间判别性，同时利用耦合分布学习将视角引导融入特征簇分配，从而无需填补缺失视角即可进行聚类。实验表明，该方法在多个不完整多视图数据集上的聚类精度显著超越基线，其缺失视角处理机制为遥感多模态缺失模态学习提供了可迁移的方法论基础。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-efmajy8dvz/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1778, \"height\": 763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-efmajy8dvz/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1730, \"height\": 778, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-efmajy8dvz/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1720, \"height\": 1094, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-efmajy8dvz/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1726, \"height\": 1097, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-efmajy8dvz/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1739, \"height\": 576, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-efmajy8dvz/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1744, \"height\": 1796, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 861, \"height\": 304, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1717, \"height\": 1658, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 860, \"height\": 462, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 867, \"height\": 996, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 865, \"height\": 1001, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 866, \"height\": 1001, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 897, \"height\": 1731, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1778, \"height\": 596, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1778, \"height\": 598, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1777, \"height\": 596, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1778, \"height\": 597, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1609, \"height\": 1121, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1609, \"height\": 1114, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1552, \"height\": 1079, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-efmajy8dvz/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1549, \"height\": 1085, \"label\": \"Table\"}]"
motivation: 现有不完整多视图聚类方法未能同时捕捉视角共享与特定特征。
method: 提出BACDL算法，通过特征簇分叉、疏离约束与耦合分布学习处理缺失视图。
result: 在多个不完整多视图数据集上聚类精度显著提升，超越现有方法。
conclusion: 该方法为缺失模态学习提供了有效方案，可迁移至遥感缺失模态处理。
---

## Abstract
Despite remarkable advances, existing incomplete multi-view clustering (IMC) methods typically  leverage  either perspective-shared or perspective-specific determinants to encode cluster representations. To address this limitation, we introduce a BACDL algorithm designed to explicitly capture both concurrently, thereby exploiting heterogeneous data more effectively. It chooses to bifurcate feature clusters and further alienate them  to enlarge the discrimination. With distribution learning, it successfully couples view guidance into feature clusters to alleviate  dimension inconsistency. Then, building on the principle  that samples in one common cluster own similar marginal distribution and conditional distribution, it unifies the association between feature clusters and sample clusters to bridge all views. Thereafter, all incomplete sample clusters are reordered and mapped to a common one to formulate  clustering embedding. Last, the overall linear overhead endows it with a resource-efficient characteristic.

---

## 论文详细总结（自动生成）

好的，这是对论文《Bifurcate then Alienate: Incomplete Multi-view Clustering via Coupled Distribution Learning with Linear Overhead》的结构化中文总结。

### 1. 论文的核心问题与整体含义
*   **研究背景**：多视图聚类（MVC）是处理日益增长的异构数据（即同一对象通过不同渠道或模态采集的数据）的关键技术，但现实应用中常因设备故障等原因导致某些视图存在样本缺失，形成不完整多视图聚类（IMC）问题。
*   **现存局限**：现有IMC方法通常仅利用 **“视角共享”**（所有视图共有的模式）或 **“视角特定”**（某视图独有的模式）其中一种决定性因素来学习聚类表征。这种单一范式无法充分挖掘数据特征间的内在联系，限制了模型性能。
*   **整体含义**：本文旨在突破此局限，提出一种名为**BACDL**的新范式，能**同时显式地捕捉视角共享和视角特定的双重决定性因素**，从而更有效地利用异构数据，实现更强大的不完整多视图聚类。

### 2. 方法论
本文提出的BACDL算法的核心思想、技术细节和算法流程如下：
*   **核心思想**：受非负矩阵分解启发，BACDL通过“分叉”和“疏离”两个关键步骤，显式地建模并增强两类特征的判别性。
*   **关键步骤与公式化**：
    1.  **分叉与疏离**：将特征簇矩阵 $C_r$ “分叉”为视角共享矩阵 $C$ 和视角特定矩阵 $C_r$，并引入视角引导矩阵 $P_r$ 将二者耦合为 $[P_rC|C_r]$。通过最小化二者的内积 $\langle P_rC, C_r \rangle$，实现“疏离”以增强判别性。
    2.  **损失函数构建**：最终损失函数结合了三部分：
        *   **基础重构与桥接损失 ($L_0$)**：基于“同一聚类样本具有相似边缘和条件分布”的原理，通过统一关联矩阵 $D$ 桥接所有视图，旨在最小化带权重的重构误差： $\min \sum_{r=1}^v a_r^2 \| \mathbf{X}_r \mathbf{G}_r - [\mathbf{P}_r \mathbf{C}|\mathbf{C}_r] \mathbf{D} \mathbf{E}_r^\top \mathbf{G}_r \|_F^2$。
        *   **疏离损失 ($L_1$)**：最小化共享与特定特征簇的内积 $\langle \mathbf{P}_r \mathbf{C}, \mathbf{C}_r \rangle$，强制它们变得不相似。
        *   **聚类嵌入损失 ($L_2$)**：通过旋转变换矩阵 $F_r$ 和自适应权重 $b_r$，将所有视图的样本簇 $\mathbf{E}_r$ 重排序并映射到一个公共的聚类嵌入矩阵 $\mathbf{E}$ 上，公式为 $\max \operatorname{Tr}(\mathbf{E}^\top \sum_{r=1}^v b_r \mathbf{E}_r \mathbf{F}_r)$。
    3.  **优化与效率**：设计了一个**九步交替优化规则**：通过推导各变量的乘性更新规则（如 $\mathbf{E}_r, \mathbf{C}, \mathbf{D}$ 等）并交替迭代求解，最终对公共矩阵 $\mathbf{E}$ 进行谱聚类得到结果。理论上证明该算法具有收敛性，且其计算和内存开销与样本数 $n$ 成**线性关系**，使其具备资源高效特性。

### 3. 实验设计
*   **数据集与场景**：使用了八个不同规模和特征的多视图基准数据集进行验证，包括`FLOEVEN`、`SYNTHREED`、`DEOLOG`、`YALTHREE`、`BGFEA`、`AWTEN`、`HDIGTWO`和`YOUFOURV`。实验模拟了多种不完整场景。
*   **对比基线**：与11种近期的主流IMC算法进行了广泛比较，包括`LRTL`、`TCIMC`、`AGCIM`、`LSIMV`、`GIMC`、`IMVCI`、`PIMVC`、`HCCGL`、`USETL`、`LBIMV`和`UIMC`。
*   **评估指标**：采用聚类纯度（PUR）、准确率（ACC）和F分数（FSC）三个常用指标。

### 4. 资源与算力
*   论文**未明确提及**使用的具体GPU型号、数量或训练时长。其重点在于通过理论证明算法的**时间复杂度和空间复杂度均为线性** $O(n)$，并通过与其他算法的运行时间和内存占用的实验对比来佐证其资源高效性。

### 5. 实验数量与充分性
*   **实验数量充足且多维**：实验设计相当充分，主要包括：
    *   **不同缺失率比较**：在三个不同缺失率（0.2, 0.5, 0.8）下对所有算法进行了性能比较（主要结果表）。
    *   **额外缺失率验证**：补充了在缺失率为0.3, 0.4, 0.6, 0.7下的对比实验。
    *   **资源效率实验**：单独对比了各算法的运行时间和内存开销。
    *   **消融实验**：系统性地验证了模型中各个组件（视角共享/特定特征、疏离操作、公共样本簇、空间旋转、视角权重、样本簇权重）的有效性。
    *   **参数敏感性分析**：可视化了模型性能对两个超参数 $\lambda$ 和 $\beta$ 的敏感度。
    *   **收敛性与稳定性分析**：绘制了目标函数值随迭代次数的下降曲线，并以误差棒展示了结果的稳定性。
*   **公平性与客观性**：对比使用了多个基准数据集、多种评价指标和现有最优方法。超参数在一定范围内搜索，保证了对比的公平性。

### 6. 主要结论与发现
*   **性能优越**：BACDL在绝大多数数据集和缺失率下，聚类性能均优于或可比于当前最优的IMC方法。
*   **广泛适用**：与其他因计算复杂度过高而无法运行在大规模数据集（如`YOUFOURV`）上的方法相比，BACDL能正常工作并取得有竞争力的结果。
*   **资源高效**：实验证实了其理论上的线性开销优势，在运行时间和内存消耗上整体处于最优或次优水平。
*   **组件有效**：消融实验证明，“双决定性因素”范式、疏离操作等各个设计组件均对提升聚类性能有积极作用。

### 7. 优点
*   **新颖的范式**：首次提出同时挖掘视角共享和视角特定特征的双决定性因素范式，是对现有IMC方法的重要补充。
*   **方法设计精巧**：通过“分叉-疏离”机制和耦合分布学习，有效地解决了特征维数不一致、特征判别性不足等问题。
*   **理论与实证并重**：不仅给出了详细的优化推导和收敛性证明，还通过大量实验充分验证了方法的有效性、效率和稳定性。
*   **高可扩展性**：经理论和实验验证的线性复杂度，使得该方法能有效应用于大规模不完整多视图数据。

### 8. 不足与局限
*   **假设限制**：部分推导（如寻找损失函数下界时假设 $n > k$）依赖于特定条件，在样本数少于簇数的极端场景下可能受限。
*   **性能波动**：在个别数据集（`FLOEVEN`， `YALTHREE`）的部分指标上结果略逊于最优方法，作者推测可能是因为从构建的谱嵌入而非原始数据生成标签时，可能减弱了视图数据的多样性。
*   **缺失机制**：实验采用随机缺失模式，未验证算法在更复杂的非随机缺失（MNAR）机制下的鲁棒性。

（完）
