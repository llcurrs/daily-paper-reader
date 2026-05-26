---
title: Aggregation of Dependent Expert Distributions in Multimodal Variational Autoencoders
title_zh: 多模态变分自编码器中依赖专家分布的聚合
authors: "Rogelio A. Mancisidor, Robert Jenssen, Shujian Yu, Michael Kampffmeyer"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=jYmGi1175R"
tags: ["query:multi-modal"]
score: 7.0
evidence: 学习每个模态子集的贡献以处理缺失模态
tldr: 针对现有多模态变分自编码器中模态独立假设过于乐观的问题，提出CoDE方法，通过依赖专家共识聚合单模态分布，学习每个模态子集的贡献，从而准确近似联合概率，在模态缺失情况下表现更优。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 823, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 609, \"height\": 460, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 607, \"height\": 460, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 644, \"height\": 508, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1729, \"height\": 333, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 640, \"height\": 507, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1586, \"height\": 364, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1749, \"height\": 401, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 586, \"height\": 455, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 866, \"height\": 636, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1612, \"height\": 922, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 836, \"height\": 633, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1656, \"height\": 557, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1659, \"height\": 720, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1468, \"height\": 868, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 527, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 527, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 528, \"height\": 521, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 527, \"height\": 520, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 827, \"height\": 1085, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 724, \"height\": 239, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 824, \"height\": 912, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1638, \"height\": 784, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1555, \"height\": 850, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1526, \"height\": 504, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-jymgi1175r/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 653, \"height\": 495, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1638, \"height\": 394, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 856, \"height\": 397, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1550, \"height\": 594, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1048, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1412, \"height\": 371, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1411, \"height\": 326, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1401, \"height\": 164, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1390, \"height\": 163, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1415, \"height\": 325, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1457, \"height\": 415, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1457, \"height\": 501, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 909, \"height\": 318, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 560, \"height\": 159, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1433, \"height\": 311, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1608, \"height\": 500, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-jymgi1175r/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1302, \"height\": 378, \"label\": \"Table\"}]"
motivation: 现有多模态VAE方法假设模态独立，难以处理模态子集和缺失模态。
method: 提出CoDE方法，利用依赖专家共识聚合单模态分布，学习每个模态子集的贡献。
result: 在缺失模态场景下，模型表现出更好的泛化性能。
conclusion: 为多模态学习提供了更准确且鲁棒的联合分布近似方法。
---

## Abstract
Multimodal learning with variational autoencoders (VAEs) requires estimating joint distributions to evaluate the evidence lower bound (ELBO). Current methods, the product and mixture of experts, aggregate single-modality distributions assuming independence for simplicity, which is an overoptimistic assumption. This research introduces a novel methodology for aggregating single-modality distributions by exploiting the principle of *consensus of dependent experts* (CoDE), which circumvents the aforementioned assumption. Utilizing the CoDE method, we propose a novel ELBO that approximates the joint likelihood of the multimodal data by learning the contribution of each subset of modalities. The resulting CoDE-VAE model demonstrates better performance in terms of balancing the trade-off between generative coherence and generative quality, as well as generating more precise log-likelihood estimations. CoDE-VAE further minimizes the generative quality gap as the number of modalities increases. In certain cases, it reaches a generative quality similar to that of unimodal VAEs, which is a desirable property that is lacking in most current methods. Finally, the classification accuracy achieved by CoDE-VAE is comparable to that of state-of-the-art multimodal VAE models.

---

## 论文详细总结（自动生成）

# 多模态变分自编码器中依赖专家分布的聚合——CoDE‑VAE 详细总结

## 1. 论文的核心问题与整体含义
多模态变分自编码器（VAE）需要估计联合后验分布以计算证据下界（ELBO），现有方法（乘积专家PoE与混合专家MoE）均假设各单模态分布（专家）相互独立。这一假设在实际中过于乐观，因为不同模态只是同一对象的互补信息源，存在自然依赖。独立假设会导致联合分布估计偏差、生成连贯性与质量失衡、ELBO优化时所有模态子集贡献平等的问题。

本文提出**CoDE‑VAE**，旨在通过**依赖专家共识（Consensus of Dependent Experts）**原则，显式建模专家估计误差间的依赖关系，并学习每个模态子集在ELBO优化中的贡献，从而在缺失模态场景下更准确地估计联合分布，实现更优的生成性能和更紧的对数似然下界。

---

## 2. 方法论

### 2.1 核心思想
- 将每个单模态推断分布看作一个“专家”，各专家对隐变量 \(z\) 的每一维给出点估计 \(\mu_{d}\) 及其不确定性 \(\sigma_{d}\)。
- 定义专家估计误差 \(e_{d} = \mu_{d} - \theta_{d}\)，假设误差服从多元高斯分布 \(\mathcal{N}(0,\Sigma_{k})\)，其中协方差矩阵 \(\Sigma_{k}\) 不仅反映各专家的不确定度（对角线），还通过相关系数 \(\rho\) 刻画专家间依赖（非对角线）。
- 将各专家的估计视作对未知隐变量 \(\theta\) 的似然，通过贝叶斯推断（在先验平坦假设下）得到共识分布（联合后验）。此即**依赖专家共识（CoDE）**方法。

### 2.2 共识分布的计算
Lemma 2 给出，给定所有专家估计向量 \(\mu_{k}\) 和已知协方差矩阵 \(\Sigma_{k}\)（\(k\) 为模态子集），共识分布为高斯：
\[
q(z|X_{k}) \sim \mathcal{N}\!\left( A_{k}^{-1}B_{k},\; A_{k}^{-1} \right)
\]
其中 \(A_{k}=u^{\top}\Sigma_{k}^{-1}u\)，\(B_{k}=u^{\top}\Sigma_{k}^{-1}\mu_{k}\)，\(u\) 为设计矩阵。
- 当 \(\rho=0\) 时，CoDE 退化为 PoE（乘积专家），足见 CoDE 是更一般的框架。
- 通过引入依赖（\(\rho>0\)），CoDE 能在专家校准不佳时自动倾向更确定的专家。

### 2.3 新的证据下界（ELBO）
引入指示向量 \(\xi\) 取自类别分布 \(\mathrm{Cat}(\pi)\)，\(\pi = (\pi_{1},\dots,\pi_{K})\) 表示每个模态子集的贡献概率。ELBO 推导为：
\[
\mathcal{L}(X) = \sum_{X_{k}} \big[ \pi_{k} \big( \mathbb{E}_{q_{\phi}(z|X_{k})}[\log p_{\theta}(X|z)] - \text{KL}[q_{\phi}(z|X_{k})\|p(z)] \big) + H(q_{\phi}(\xi|X_{k})) \big] + C
\]
- 可学习参数 \(\pi_{k}\) 根据各子集分布的不确定度（协方差矩阵迹）自动调节贡献，不确定度大的子集贡献小。
- 整体优化过程不使用模态子采样，避免对联合分布近似的损害。

### 2.4 训练流程
- 所有编码器输出 \(\mu_{i}\)、\(\sigma_{i}^{2}\)；
- 指定相关系数 \(\rho\)（交叉验证选取），构建 \(\Sigma_{k}\)；
- 利用 CoDE 聚合得到各子集的 \(q(z|X_{k})\)；
- 按上述 ELBO 计算损失，用 Adam 优化器更新网络参数 \(\theta,\phi\) 以及 \(\pi\)。

---

## 3. 实验设计

### 3.1 数据集与场景
- **MNIST‑SVHN‑Text**：三模态数据集（手写数字、街景数字、描述文本），用于评估异质模态下的生成与对数似然。
- **PolyMNIST**：5 模态 MNIST 变体（不同背景、书写风格），专门考察模态数量增加时生成质量差距。
- **Caltech Birds (CUB)**：真实图像‑文本数据集，用于测评复杂场景的生成连贯性和质量。

### 3.2 对比方法
与主流的 6 种模型对比：MVAE、MMVAE、mmJSD、MoPoE‑VAE、MVTCAE、MMVAE+（其中 MMVAE+ 使用了模态特有隐变量改善生成质量）。

### 3.3 评估指标
- 生成连贯性（条件 / 无条件）：分类器准确率判断生成样本是否具有一致语义。
- 生成质量：Fréchet Inception Distance (FID)。
- 联合对数似然估计（衡量边界紧致性）。
- 分类准确率：用线性分类器评估隐表示判别力。
- **生成质量差距**：多模态 VAE 与单模态 VAE 的 FID 差异，用于反映模型随模态数增加的质量衰减。

### 3.4 超参数选择
- \(\beta\)（KL 正则系数）：在 {0.1,1,5,10,15,20} 交叉验证，对 PolyMNIST 额外设为 2.5。
- \(\rho\)（相关系数）：在 {0,0.2,0.4,0.6,0.8} 中选取最优值。
- 所有实验重复 3 次取平均和标准差，对比均选用各方法的最优超参数，确保公平。

---

## 4. 资源与算力
- 训练均在**单块 NVIDIA A100 GPU** 上完成，使用混合精度加速。
- 处理速度：MNIST‑SVHN‑Text 每批 46ms（PoE 为 36ms），PolyMNIST 每批 1050ms（PoE 为 790ms），CoDE 带来的额外计算开销较低。
- 论文未提及其他 GPU 集群或训练总时长，但指出即使面对 5 模态数据，模型训练在单 GPU 上仍可行。

---

## 5. 实验数量与充分性
实验覆盖充分且设计严谨：
- 3 个不同类型数据集，全面评估异质、多模态模态数、真实复杂场景。
- 多个对比模型（6 个），所有结果基于多次运行与最优超参数对比。
- 系统研究生成质量差距随模态数（2‑5 模态）的变化（图 3）。
- 分析 CoDE 学习系数 \(\pi_{k}\) 与子集分布不确定度的关系（图 5）。
- 消融实验：分开考察 π 学习与 ρ 使用的影响，包括等权重 vs. 可学习权重、ρ=0 vs. 最优 ρ，以及模态相关性边缘案例（表 12）。
- 额外实验：在 CelebA 上对比，结果进一步支持主结论。
- 因此，实验不仅量多且维度全面，结论可信度高。

---

## 6. 主要结论与发现
- CoDE‑VAE 在生成连贯性与质量的权衡上显著优于现有模型，同时给出更紧致的对数似然估计。
- 与依赖子采样方法的模型不同，**CoDE‑VAE 在模态数量增加时生成质量差距缩小甚至消失**，在 PolyMNIST 4/5 模态下可达到单模态 VAE 水平。
- 可学习的子集贡献 \(\pi_{k}\) 与子集分布的不确定度（协方差迹）呈反比，验证了“更确定的子集应贡献更大”的动机。
- 考虑专家依赖（\(\rho>0\)）能提升生成质量、对数似然和分类性能。
- 分类准确率与当前最优多模态 VAE 模型相当。
- 消融实验明确表明：同时学习 π 并使用依赖关系（ρ）比等权且独立假设带来显著增益。

---

## 7. 优点
- **首次将依赖专家共识引入多模态 VAE**，突破独立性假设，理论上更合理。
- CoDE 是通用聚合方法，可兼容任何使用 PoE 的多模态 VAE，并退化为 PoE（ρ=0）。
- **无需子采样**，避免了由此造成的联合分布近似退化和生成质量差距扩大。
- 自适应学习每个子集的 ELBO 权重，使优化更高效。
- 实验设计全面，对比公平，覆盖多种真实与合成数据，并提供代码开源。

---

## 8. 不足与局限
- **相关系数 ρ 需交叉验证**，对大规模复杂数据可能增加计算负担（但实验证明仍可承受）。
- 当前只考虑了正相关依赖（0 至 0.8），未探索负相关的可能场景。
- 训练复杂度仍与子集数目呈指数关系 \(O(2^{M}-1)\)，对于模态数极大的场景可能受限（但文中验证 5 模态可行）。
- 先验分布和似然函数的选择目前固定，不同选择下 CoDE 的影响尚不明确。
- 生成质量在 MNIST‑SVHN‑Text 上略逊于某些专为生成质量优化的模型（如 MMVAE+），但这是在未使用模态特有隐变量的情况下取得的平衡。

（完）
