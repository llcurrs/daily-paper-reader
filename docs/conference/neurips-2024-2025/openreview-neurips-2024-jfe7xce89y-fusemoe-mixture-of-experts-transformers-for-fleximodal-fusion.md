---
title: "FuseMoE: Mixture-of-Experts Transformers for Fleximodal Fusion"
title_zh: FuseMoE：面向柔性模态融合的专家混合Transformer
authors: "Xing Han, Huy Nguyen, Carl William Harris, Nhat Ho, Suchi Saria"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=jfE7XCE89y"
tags: ["query:multi-modal"]
score: 7.0
evidence: 通过专家混合门控处理缺失模态与不规则数据
tldr: 针对多模态学习中模态缺失与数据不规则采样问题，提出FuseMoE框架，采用创新门控函数的专家混合模型。该框架能有效集成任意数量模态，并在缺失模态场景下保持鲁棒性。实验验证其在提高预测性能方面的有效性，为缺失模态处理提供通用解决方案。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-jfe7xce89y/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1466, \"height\": 406, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jfe7xce89y/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1425, \"height\": 389, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jfe7xce89y/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1268, \"height\": 520, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jfe7xce89y/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1496, \"height\": 385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jfe7xce89y/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1445, \"height\": 325, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jfe7xce89y/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 805, \"height\": 745, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jfe7xce89y/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1396, \"height\": 551, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jfe7xce89y/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1394, \"height\": 553, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jfe7xce89y/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1394, \"height\": 547, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jfe7xce89y/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1398, \"height\": 535, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jfe7xce89y/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1400, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jfe7xce89y/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 872, \"height\": 357, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jfe7xce89y/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1498, \"height\": 469, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-jfe7xce89y/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1443, \"height\": 280, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-jfe7xce89y/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1424, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-jfe7xce89y/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1455, \"height\": 337, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-jfe7xce89y/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1459, \"height\": 267, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-jfe7xce89y/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1463, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-jfe7xce89y/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 800, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-jfe7xce89y/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1426, \"height\": 293, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-jfe7xce89y/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1337, \"height\": 906, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-jfe7xce89y/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1458, \"height\": 195, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-jfe7xce89y/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1457, \"height\": 266, \"label\": \"Table\"}]"
motivation: 多模态数据常面临模态缺失和不规则采样，现有方法难以应对。
method: 提出FuseMoE，利用专家混合和新型门控函数灵活整合多模态。
result: 在缺失模态和不规则数据下显著提升预测性能。
conclusion: FuseMoE为缺失模态场景下的多模态融合提供了有效框架。
---

## Abstract
As machine learning models in critical fields increasingly grapple with multimodal data, they face the dual challenges of handling a wide array of modalities, often incomplete due to missing elements, and the temporal irregularity and sparsity of collected samples. Successfully leveraging this complex data, while overcoming the scarcity of high-quality training samples, is key to improving these models' predictive performance. We introduce ``FuseMoE'', a mixture-of-experts framework incorporated with an innovative gating function. Designed to integrate a diverse number of modalities, FuseMoE is effective in managing scenarios with missing modalities and irregularly sampled data trajectories. Theoretically, our unique gating function contributes to enhanced convergence rates, leading to better performance in multiple downstream tasks. The practical utility of FuseMoE in the real world is validated by a diverse set of challenging prediction tasks.

---

## 论文详细总结（自动生成）

好的，根据您提供的论文内容，以下是关于 “FuseMoE: Mixture-of-Experts Transformers for Fleximodal Fusion” 的结构化中文总结。

### 1. 论文的核心问题与整体含义

*   **研究背景**：多模态数据在实际应用中普遍存在（如医疗数据、情感分析），但这类数据常常面临两大难题：
    *   **模态缺失**：并非所有样本都包含全部模态的数据，导致输入不完整。
    *   **时间不规则性与稀疏性**：不同模态数据的采样频率和时点不一致，形成不规则的时间序列。
*   **核心问题**：现有的多模态融合方法大多设计用于固定数量的完备模态，缺乏有效机制来灵活、可扩展地处理模态缺失和时间不规则性问题，这限制了模型在真实复杂场景下的预测性能。
*   **论文目标**：提出一种新型混合专家框架（FuseMoE），旨在灵活集成任意数量、可能存在缺失和不规则采样的模态数据，并通过理论分析和实验验证其有效性，以提升在“FlexiModal数据”场景下的预测表现。

### 2. 论文提出的方法论

*   **核心思想**：FuseMoE 框架通过三个关键组件协同工作来处理多模态融合问题。
    1.  **模态与不规则性编码器**：采用离散化多时间注意力（mTAND）模块，配合简单的插补方法，将不规则采样的时间序列数据统一编码为固定长度的标准嵌入表示，解决时间不规则问题。
    2.  **专家混合（MoE）融合层**：作为模型核心，包含一个门控网络（路由）和多个专家网络（前馈神经网络FFN）。系统根据输入动态地、稀疏地选择最相关的专家子集来处理特定模态组合，从而提升模型容量和效率。
    3.  **创新的Laplace门控函数**：与传统Softmax门控函数不同，FuseMoE提出使用基于L2距离的Laplace门控函数：`hl(x) = TopK(-∥W - x∥²)`。理论上，该函数能提供更快的参数收敛速率，并在处理多模态数据时性能更优。
*   **路由设计**：提供了三种灵活的路由策略以平衡模态间依赖和模态内特性：
    *   **联合路由器**：将所有模态的嵌入拼接后统一路由。
    *   **逐模态路由器**：为每个模态使用独立路由器，但共享同一个专家池。
    *   **分离式路由与专家**：为每个模态分配独立的路由器和专属的专家池。
*   **缺失模态处理**：通过引入一个可学习的“缺失指示嵌入”来代表缺失模态，并利用熵正则化损失引导路由器为其分配特定的、不常用的专家，从而动态减少来自缺失数据专家的负面影响。

### 3. 实验设计

*   **使用的数据集/场景**：
    *   **医疗数据（FlexiModal）**：MIMIC-III和MIMIC-IV数据集，包含生命体征、临床笔记、胸部X光片（CXR）、心电图（ECG）等模态，用于住院死亡预测（48-IHM）、住院时长预测（LOS）和25种表型分类（25-PHE）。
    *   **情感分析**：CMU-MOSI和CMU-MOSEI数据集，包含文本、音频和视频模态，用于情感和情绪识别。
    *   **活动识别**：物理活动监测（PAM）数据集，包含17个传感器数据，用于日常活动识别。
    *   **图像分类**：CIFAR-10数据集，用于验证Laplace门控在视觉任务上的泛化能力。
*   **对比方法**：
    *   **医疗数据基准**：MISTS， MulT， MAG， TFN， HAIM。
    *   **情感分析基准**：TFN， MulT， MAG， 以及标准Softmax门控MoE。
    *   **时间序列基准**：Transformer， GRU-D， SeFT， mTAND， IP-Net。
    *   **图像分类基准**：基于ViT的Vision-MoE（使用标准Softmax门控）。
*   **评估指标**：AUROC， F1 Score， MAE， Pearson相关系数（Corr）， 准确率（Acc-2）等，具体指标依据任务而定。

### 4. 资源与算力

*   论文在附录G.1中提到，所有模型均使用一台配备**4块A5500 GPU（24GB内存）**的Lambda Workstation进行训练。实际训练时，**仅使用单块GPU**即可完成。
*   未提及总训练时长或每个实验的具体耗时，但附录图12（a）给出了模型计算效率与资源占用的比较分析。

### 5. 实验数量与充分性

*   **实验数量充足**：论文在**四个不同的应用领域（医疗、情感、活动、图像）的六个数据集**上进行了大量实验。
*   **对比全面**：将FuseMoE与针对特定领域的多个顶尖基准模型进行了比较。
*   **消融实验详尽**：
    *   **路由器设计**：比较了3种不同的路由器设计。
    *   **门控函数**：对比了Laplace、Softmax和Gaussian门控。
    *   **模态数量**：验证了模型向更多模态扩展的能力。
    *   **缺失模态**：设计了特定实验验证模型在模态缺失下的性能。
    *   **模型组件**：对不规则编码器、时间序列编码器、CXR/文本编码器等不同模块的选择进行了消融研究。
    *   **MoE超参数**：研究了专家数量对性能的影响。
*   **实验客观性**：所有结果均为**5次随机实验的平均值**，并在结果表格中标注了标准差，确保了结果的统计可靠性。对比方法均来自原论文的官方实现或广泛引用的基线模型，保证了比较的公平性。

### 6. 论文的主要结论与发现

*   **性能优越**：FuseMoE框架在所有评估数据集上，特别是在FlexiModal数据场景（如MIMIC-IV）中，相比现有基准模型**取得了显著且持续的预测性能提升**。
*   **门控函数优势**：无论是在理论上（更快的收敛速率）还是实验上，**Laplace门控函数的性能均优于标准的Softmax门控函数**，尤其是在处理异质性输入和缺失数据时。
*   **扩展性与鲁棒性**：得益于MoE结构，FuseMoE能**有效扩展到更多模态**，并且通过逐模态路由和熵损失机制，对**模态缺失表现出强大的鲁棒性**，甚至在某些任务上性能优于使用完整数据的场景。
*   **关键模块有效性**：消融实验证明，不规则编码器（mTAND）、MoE融合层以及熵正则化损失均对模型最终性能有积极贡献。

### 7. 优点

*   **创新的方法论**：提出了一个高度灵活、可扩展的MoE多模态融合框架，并首次将Laplace门控函数应用于该领域，附带理论收敛性保证。
*   **问题导向性强**：直接针对真实世界数据中普遍存在的“模态缺失”和“时间不规则性”这两大痛点，提供了优雅的解决方案。
*   **全面的实验验证**：实验设计横跨多个领域和任务，包含丰富的消融和对比分析，结论具有高度说服力。
*   **理论实践结合**：不仅有坚实的理论分析（参数估计收敛速率），还有扎实的工程实现和全面的实验佐证。

### 8. 不足与局限

*   **编码器过参数化风险**：论文在“讨论与局限性”部分自省，当输入数据规模较小时，当前的不规则性编码方法**可能导致模型过参数化**。
*   **对罕见模态的依赖**：从图12（c）的专家权重分析看，当某种模态样本极少时，模型可能对其依赖性不高。尽管能处理缺失，但在少量样本下对该模态特征的充分学习能力未得到专门验证。
*   **计算成本**：虽然MoE层稀疏激活，但相比单模型方法，FuseMoE的**总参数规模显著增大**（图12（a）），可能对存储和显存有更高要求。

（完）
