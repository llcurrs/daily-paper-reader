---
title: Learning Reconfigurable Representations for Multimodal Federated Learning with Missing Data
title_zh: 学习可重构表示以应对具有缺失数据的多模态联邦学习
authors: "Manh Duong Nguyen, Trong Nghia Hoang, Thanh Trung Huynh, Quoc Viet Hung Nguyen, Phi Le Nguyen"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=rMqQdJJz5r"
tags: ["query:multi-modal"]
score: 8.0
evidence: 处理多模态联邦学习中的数据缺失
tldr: 该文针对客户端多模态数据不完整且异构的联邦学习场景，提出基于可学习客户端特定标记的局部自适应表示方法，解决特征不对齐问题。实验表明模型聚合效果和在下游任务上的性能提升。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-rmqqdjjz5r/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1425, \"height\": 391, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rmqqdjjz5r/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1430, \"height\": 630, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rmqqdjjz5r/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 515, \"height\": 321, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rmqqdjjz5r/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1444, \"height\": 389, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rmqqdjjz5r/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1302, \"height\": 1030, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rmqqdjjz5r/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1443, \"height\": 660, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rmqqdjjz5r/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1446, \"height\": 1143, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rmqqdjjz5r/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1305, \"height\": 531, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-rmqqdjjz5r/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1429, \"height\": 592, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rmqqdjjz5r/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 793, \"height\": 557, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rmqqdjjz5r/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 578, \"height\": 342, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rmqqdjjz5r/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1452, \"height\": 624, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rmqqdjjz5r/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1281, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rmqqdjjz5r/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1376, \"height\": 1222, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rmqqdjjz5r/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 652, \"height\": 453, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rmqqdjjz5r/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1316, \"height\": 664, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rmqqdjjz5r/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 883, \"height\": 196, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rmqqdjjz5r/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1391, \"height\": 701, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rmqqdjjz5r/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1190, \"height\": 179, \"label\": \"Table\"}]"
motivation: 多模态联邦学习中数据不完整与异构导致特征不对齐。
method: 提出局部自适应表示，利用可学习标记对齐特征。
result: 在多种缺失模式下聚合效果提升。
conclusion: 重塑表示学习有效处理多模态联邦缺失数据。
---

## Abstract
Multimodal federated learning in real-world settings often encounters incomplete and heterogeneous data across clients. This results in misaligned local feature representations that limit the effectiveness of model aggregation. Unlike prior work that assumes either differing modality sets without missing input features or a shared modality set with missing features across clients, we consider a more general and realistic setting where each client observes a different subset of modalities and might also have missing input features within each modality. To address the resulting misalignment in learned representations, we propose a new federated learning framework featuring locally adaptive representations based on learnable client-side embedding controls that encode each client’s data-missing patterns.

These embeddings serve as reconfiguration signals that align the globally aggregated representation with each client's local context, enabling more effective use of shared information. Furthermore, the embedding controls can be algorithmically aggregated across clients with similar data-missing patterns to enhance the robustness of reconfiguration signals in adapting the global representation. Empirical results on multiple federated multimodal benchmarks with diverse data-missing patterns across clients demonstrate the efficacy of the proposed method, achieving up to 36.45\% performance improvement under severe data incompleteness. The method is also supported by a theoretical analysis with an explicit performance bound that matches our empirical observations. Our source codes are provided at [https://github.com/nmduonggg/PEPSY](https://github.com/nmduonggg/PEPSY)

---

## 论文详细总结（自动生成）

# 论文总结：Learning Reconfigurable Representations for Multimodal Federated Learning with Missing Data

## 1. 论文的核心问题与整体含义
- **研究动机**：现实世界中的多模态联邦学习常面临客户端数据不完整和异构的双重挑战——既可能缺失整个模态（如某一客户端只有声音而无生理信号），也可能模态内部存在部分特征缺失（如传感器故障）。这两种缺失事件同时发生，导致各客户端本地学习到的特征表示处于不对齐的空间中，直接聚合会破坏全局模型的性能。
- **现有工作局限**：先前方法或假设所有客户端拥有相同模态但部分缺失特征，或假设模态不同但无特征缺失，尚未覆盖两者同时出现的更一般化场景。
- **整体含义**：本文提出一种新型框架，通过可学习的客户端“嵌入控制”编码每个客户端的数据缺失模式，并将其作为重构信号来对齐全局表示与本地上下文，从而解决表示不对齐问题，实现鲁棒的多模态联邦学习。

## 2. 论文提出的方法论
- **核心思想**：构建一个可共享的数据缺失配置文件（data-missing profile），将每个客户端的模态特定信息、数据特定信息以及缺失模式信息提炼为一组嵌入控制。这些嵌入控制充当指令，将全局聚合的表示重构为适应当地上下文的全模态表示。
- **关键技术细节**：
  - **客户端设计**：
    - 将每个实例的表示分解为三个部分：模态特定特征（\(w^{\text{mod}}_{di}\)，由共享嵌入提供）、数据特定特征（\(w^{\text{ins}}_{di}\)，对缺失模态采用可观测模态特征的均值进行重构）、缺失模式特征（\(w^{\text{mis}}_{di}\)，通过与配置文件的查询‑键匹配获得）。
    - 引入**数据特定损失 \(L_{\text{ds}}\)**，鼓励同一实例的不同模态特征相互靠近，不同实例的相互远离，减少对缺失模态的依赖。
    - 通过余弦相似度从本地缺失配置文件中为每个实例选择 \(κ\) 个最相关的嵌入控制，并引入**相关性正则化 \(R\)** 以避免注意力过于分散。
    - 拼接三类特征后，利用**重构对比损失 \(L_{\text{rc}}\)** 使重构特征与全模态特征对齐，形成全模态表示，再通过跨模态注意力融合得到最终特征送入预测头。
  - **服务器聚合**：
    - 各客户端上传神经参数（通过 FedAvg 聚合）和数据缺失配置文件。
    - 由于各客户端学习到的嵌入控制顺序不一致，采用**非参数聚类（PFPT）** 将相似的嵌入控制聚合为全局配置文件，动态适应缺失复杂度。
  - **训练总体目标**：\(L = L_{\text{task}} + \lambda(L_{\text{ds}} + L_{\text{rc}}) - \eta R\)。
- **理论保障**：定理3.1证明，在有模态缺失时模型输出与全模态输出的期望偏差由 \(L_{\text{ds}}\) 和 Lipschitz 常数等控制，验证了通过最小化 \(L_{\text{ds}}\) 可提升对缺失模态的鲁棒性。

## 3. 实验设计
- **数据集与场景**：
  - **PTBXL**：12 导联心电数据集，共 3963 个样本，5 分类任务，模拟 12 个模态。
  - **Sleep‑EDF**：5 个生理信号模态的睡眠分期数据集，重新划分为 5 分类。
  - 两种数据分布：**IID**（均匀划分）和 **Non‑IID**（Dirichlet 分布 α=0.5）。
  - **缺失模拟**：定义样本缺失比率 \(p_s\) 与模态缺失比率 \(p_m\)，构造二进制缺失矩阵，控制整体缺失度 \(p_m \times p_s\)；实验涵盖多种组合（如 0.2 到 1.0 步长）。
- **对比方法**：
  - 标准联邦方法：**FedProx**（忽略缺失）；
  - 专门处理模态缺失的方法：**FedMSplit**、**MIFL**；
  - 处理特征缺失的方法：**FedInMM**、**FedMAC**。
- **评估指标**：服务器端测试集的分类准确率。

## 4. 资源与算力
- **硬件**：实验使用 **NVIDIA A6000 GPU（48 GB 显存）**。
- **训练配置**：共 32 个客户端，每轮随机选取 10 个参与，每个客户端本地训练 **3 epoch**，通信总轮数 **1000 轮**（PTBXL）或 **500 轮**（EDF）。
- **训练时间**：论文给出了每轮训练时间对比（Table 6），PEPSY 每轮约 **140 秒**左右，高于 FedProx 等基准方法（约 50–100 秒），这是其额外计算开销的体现。
- **未明确说明**：未报告完整训练过程的总体时间或总 GPU 卡数，但这些信息在表格和附录中有部分体现。

## 5. 实验数量与充分性
- **实验数量**：论文中汇报了大量实验，包括：
  - 不同缺失统计下的主要结果（两张表覆盖 32 个组合，每次重复有 error bar）；
  - 训练与测试缺失统计不一致的鲁棒性测试（多种组合）；
  - 消融实验：聚合算法对比、对齐损失权重影响、缺省配置文件（‑NP）与缺失重构损失（‑NR）的消融；
  - 可视化分析：模态对齐 t‑SNE、配置文件收敛性、控制嵌入多样性。
  - 附录中增加了更广泛的缺失度组合以及图像‑传感器混合模态的实验。
- **充分性与公平性**：实验设计全面覆盖了不同缺失度、数据异质性和方法组件，对比基线涉及多种缺失处理思路，且多次运行提供标准差，具备客观性与公平性。

## 6. 论文的主要结论与发现
- 所提出的 **PEPSY** 框架在各项缺失场景下均优于现有方法，尤其在严重缺失时可带来 **高达 36.45% 的性能提升**。
- 数据缺失配置文件能够有效捕捉各客户端的局部缺失特性，并通过重构信号将偏差表示转化为数据完整的表示，显著提高全局模型的聚合效果。
- 理论分析表明，预测输出在有缺失与全模态下的偏差可以通过训练损失 \(L_{\text{ds}}\) 进行控制，为方法提供了理论支撑。
- 消融实验证实，数据缺失配置文件与重构对比损失是方法成功的关键组件。

## 7. 优点
- **方法新颖性**：首次以可学习嵌入控制的形式编码缺失模式，实现了一种不共享数据、不依赖 imputation 的对齐机制。
- **联邦适应**：服务器端采用非参数聚类聚合缺失配置文件，能灵活应对不同客户端缺失模式的变化，具备良好的扩展性。
- **理论与实证结合**：提供了明确的泛化界，并用多样化实验充分验证，在理论指导下设计损失函数。
- **实验全面**：覆盖了多个数据集、IID/Non‑IID、多种缺失度组合以及跨缺失分布的泛化测试，对比基线种类丰富。

## 8. 不足与局限
- **计算开销较大**：每轮训练时间约为基准方法的 2~3 倍，服务器端非参数聚类进一步增加了复杂度，可能影响在资源受限环境中的实用性。
- **大规模缺失域迁移**：文中提到，当客户端任务域差异显著时，可能需要更多的嵌入控制来有效重构，目前方法未针对该情形给出自适应方案。
- **依赖从头训练**：未利用预训练基础模型，这可能限制其在拥有领域基础模型时的效率提升潜力。
- **模态覆盖**：主要实验基于生理信号模态，虽附录包含图像‑信号混合模态的尝试，但整体实验对象仍以传感器信号为主，对其他模态类型（如文本、视频）的验证有待补充。

（完）
