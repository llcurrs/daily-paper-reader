---
title: "CyIN: Cyclic Informative Latent Space for Bridging Complete and Incomplete Multimodal Learning"
title_zh: CyIN：用于桥接完整与不完整多模态学习的循环信息潜在空间
authors: "Ronghao Lin, Qiaolin He, Sijie Mai, Ying Zeng, Aolin Xiong, Li Huang, Yap-Peng Tan, Haifeng Hu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=feuFyonHks"
tags: ["query:multi-modal"]
score: 8.0
evidence: 桥接完整与不完整多模态学习
tldr: 该文针对多模态学习中模态动态缺失导致性能下降的问题，提出循环信息学习框架CyIN，通过令牌和标签级信息瓶颈构建信息丰富潜在空间，弥合完整与不完整学习。实验证实了模型在缺失模态下的鲁棒性提升。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-feufyonhks/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1369, \"height\": 675, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-feufyonhks/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1433, \"height\": 703, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1387, \"height\": 988, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1408, \"height\": 518, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 648, \"height\": 500, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1379, \"height\": 224, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 653, \"height\": 328, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1423, \"height\": 809, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1387, \"height\": 1954, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1349, \"height\": 2282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1462, \"height\": 735, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1113, \"height\": 421, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1431, \"height\": 324, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 816, \"height\": 478, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 685, \"height\": 288, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-feufyonhks/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 652, \"height\": 203, \"label\": \"Table\"}]"
motivation: 模态动态缺失导致预训练模型性能大幅下降。
method: 提出CyIN框架，采用信息瓶颈构建信息丰富空间。
result: 动态缺失模态下保持鲁棒性。
conclusion: CyIN有效弥合完整与不完整多模态学习。
---

## Abstract
Multimodal machine learning, mimicking the human brain’s ability to integrate various modalities has seen rapid growth. Most previous multimodal models are trained on perfectly paired multimodal input to reach optimal performance. In real‑world deployments, however, the presence of modality is highly variable and unpredictable, causing the pre-trained models in suffering significant performance drops and fail to remain robust with dynamic missing modalities circumstances. In this paper, we present a novel Cyclic INformative Learning framework (CyIN) to bridge the gap between complete and incomplete multimodal learning. Specifically, we firstly build an informative latent space by adopting token- and label-level Information Bottleneck (IB) cyclically among various modalities. Capturing task-related features with variational approximation, the informative bottleneck latents are purified for more efficient cross-modal interaction and multimodal fusion. Moreover, to supplement the missing information caused by incomplete multimodal input, we propose cross-modal cyclic translation by reconstruct the missing modalities with the remained ones through forward and reverse propagation process. With the help of the extracted and reconstructed informative latents, CyIN succeeds in jointly optimizing complete and incomplete multimodal learning in one unified model. Extensive experiments on 4 multimodal datasets demonstrate the superior performance of our method in both complete and diverse incomplete scenarios.

---

## 论文详细总结（自动生成）

好的，作为一名资深学术论文分析助手，我将基于您提供的论文内容，以 Markdown 格式对该论文进行结构化、深入、客观的总结。

### **1. 论文的核心问题与整体含义**

*   **研究动机与核心问题**：
    *   当前多模态机器学习模型通常在完整、配对的多模态数据上训练以获得最佳性能。
    *   然而，在真实世界部署中，模态数据常因传感器故障等原因而动态缺失，导致预训练模型性能大幅下降。
    *   现有方法在应对模态缺失时，存在对缺失信息利用不足、受任务无关噪声干扰、需为不同缺失组合训练独立模型，以及牺牲完整模态下性能等问题。
*   **整体含义与目标**：
    *   本文旨在解决**模态缺失问题**，并提出一个名为**CyIN**的统一框架，旨在弥合完整与不完整多模态学习之间的鸿沟。
    *   核心目标是构建一个单一模型，使其在模态完整时能高效融合，在模态动态缺失时也能保持鲁棒性和高性能。

### **2. 论文提出的方法论**

*   **核心思想**：
    *   构建一个**循环信息潜在空间**，在此空间中统一进行完整模态下的特征融合和不完整模态下的信息重建。该空间通过信息瓶颈原理，从低层感知和高层语义两个层面提纯任务相关信息，过滤冗余噪声。
*   **关键技术细节**：
    1.  **信息瓶颈潜在空间**：
        *   **令牌级信息瓶颈**：在任意两个模态的令牌嵌入之间建立信息瓶颈，压缩源模态信息以预测目标模态特征，促进跨模态交互。通过循环选择源和目标模态，捕捉模态内和模态间的动态关系。
        *   **标签级信息瓶颈**：将每个模态的表示作为源，真实标签作为目标，通过信息瓶颈注入高层语义监督，确保潜在空间包含任务相关的判别性特征。
        *   通过变分近似对瓶颈潜在变量进行采样，实现端到端优化。
    2.  **跨模态循环翻译**：
        *   **前向传播**：在信息潜在空间中，利用级联残差自编码器作为翻译器，从保留的模态将信息翻译重建为缺失的模态信息。
        *   **反向传播**：采用循环一致性学习，将前向重建的信息再翻译回源模态，以确保翻译过程保留了关键的模态间动态，增强重建质量。
        *   **泛化至多模态**：当保留模态多于一个时，利用高斯分布的可加性，将多个翻译器的输出整合，生成最终的缺失模态潜在变量。
*   **统一优化与训练**：
    *   整个框架的优化目标由四部分组成：任务预测损失、令牌级信息瓶颈损失、标签级信息瓶颈损失和跨模态循环翻译损失。
    *   采用**多阶段训练策略**：第一阶段专注于构建完整模态下的信息空间；第二阶段逐步引入翻译损失，增强对不完整输入的处理能力。

### **3. 实验设计**

*   **数据集与场景**：
    *   **多模态回归**：MOSI 和 MOSEI（视频情感分析）。
    *   **多模态分类**：IEMOCAP 和 MELD（多模态情感识别）。
    *   模态包括：语言、音频、视觉。
    *   评估场景：
        *   **完整模态输入**。
        *   **固定缺失协议**（如仅语言、仅视觉、仅音频，或缺失双模态等）。
        *   **随机缺失协议**（以不同缺失率随机丢弃某个或某几个模态）。
*   **基准与对比方法**：
    *   与多种先进的基线模型进行对比，涵盖了基于对齐和生成的方法，包括：CCA， DCCA， DCCAE， CRA， MCTN， MMIN， GCNet， IMDer， LNLN， CPM-Net。
*   **评价指标**：
    *   回归任务：七分类准确率、F1分数、平均绝对误差、皮尔逊相关系数。
    *   分类任务：准确率、加权F1分数。

### **4. 资源与算力**

*   论文在“实施细节”部分明确提到：所有实验均在 **NVIDIA H800 GPU** 上完成，使用 **PyTorch 2.4.1** 和 **CUDA 12.4**。
*   在“计算效率”分析中，对比了模型的参数量、总训练时间和推理时间。例如，在MOSI数据集上，CyIN的总参数量为 **123.49M**，总训练时间为 **1.61小时**，单次迭代推理时间为 **22.41秒**。

### **5. 实验数量与充分性**

*   **实验数量充足**：
    *   在**4个数据集**上进行了全面评估。
    *   评估覆盖了**3种不同的输入场景**：完整模态、6种固定缺失、7种随机缺失率。
    *   包含**消融研究**，验证了令牌/标签级信息瓶颈、循环交互/翻译、信息空间等各个核心组件的有效性。
    *   进行了**超参数敏感性分析**和**泛化性测试**。
    *   展示了定性结果，如**t-SNE可视化**和**案例研究**。
*   **客观性与公平性**：
    *   与**11种**现有基线方法进行了对比。
    *   使用了**公开数据集**和**标准评价指标**。
    *   通过**10次固定随机种子运行**取平均值来报告结果，确保了比较的公平性和稳定性。
    *   从实验的广度和深度来看，实验设计非常充分且严谨。

### **6. 论文的主要结论与发现**

*   CyIN 在完整和不完整多模态输入场景下，在多个数据集上均取得了**最先进的性能**，超越了现有基线方法。
*   所构建的**信息瓶颈潜在空间**能有效提纯任务相关特征，同时支持高效的跨模态融合与缺失信息重建。
*   **循环交互和翻译机制**显著提升了完整模态下的特征交互效率，并增强了不完整模态下的信息重建质量。
*   CyIN 在一个统一模型中成功地结合了完整和不完整多模态学习，而无需为特定缺失情况牺牲完整模态的性能。

### **7. 优点**

*   **方法论创新**：首次将令牌级和标签级信息瓶颈以循环方式结合，构建了一个统一的、信息丰富的潜在空间，用于解决模态缺失问题。
*   **模型统一性**：单一模型即可处理完整和各种不完整模态输入，无需针对不同缺失组合训练多个模型，实用性更强。
*   **性能与鲁棒性兼得**：显著提升了在完整模态下的性能，同时在多种严重缺失场景下表现出卓越的鲁棒性，打破了以往方法常需在两者间取舍的困境。
*   **出色的泛化能力**：不仅在固定缺失情况下表现优异，在更贴近现实的随机缺失协议下也展现了稳定的性能。
*   **计算效率**：与部分SOTA方法相比，CyIN在参数量和推理速度上具有优势。

### **8. 不足与局限**

*   **平等对待所有模态**：模型默认所有模态同等重要，忽略了在特定任务中不同模态贡献不均衡的情况（如情感分析中语言通常占主导），这可能不是最优策略。
*   **翻译模块的可替代性**：当前的跨模态翻译器基于级联残差自编码器，性能可能受限于此架构，采用更先进的生成模型（如扩散模型）可能会取得更好的重建效果。
*   **泛化性验证有限**：实验主要在情感分析和计算相关的中等规模数据集上进行，在更大规模、更多样化的多模态理解数据集或与大型语言模型集成时的效果有待进一步验证。

（完）
