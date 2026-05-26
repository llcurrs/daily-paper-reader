---
title: "Unity by Diversity: Improved Representation Learning for Multimodal VAEs"
title_zh: 因多样而统一：改进多模态VAE的表示学习
authors: "Thomas M. Sutter, Yang Meng, Andrea Agostini, Daphné Chopard, Norbert Fortin, Julia E Vogt, Babak Shahbaba, Stephan Mandt"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=Z4R2rkPgBy"
tags: ["query:multi-modal"]
score: 5.0
evidence: 具有插补能力的多模态VAE
tldr: 该文针对现有多模态VAE共享约束过强的问题，提出混合专家先验软约束，使各模态编码保留更多信息，提升潜在表示质量。实验表明在表示学习、条件生成和插补任务上的优势。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1456, \"height\": 292, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1429, \"height\": 823, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1305, \"height\": 553, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1414, \"height\": 402, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 739, \"height\": 442, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 876, \"height\": 266, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1427, \"height\": 610, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1422, \"height\": 607, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1452, \"height\": 936, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1452, \"height\": 937, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1419, \"height\": 609, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 589, \"height\": 305, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1454, \"height\": 928, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1395, \"height\": 1218, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1453, \"height\": 929, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1449, \"height\": 591, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1405, \"height\": 551, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 738, \"height\": 507, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1188, \"height\": 783, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-z4r2rkpgby/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1192, \"height\": 783, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-z4r2rkpgby/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1450, \"height\": 398, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-z4r2rkpgby/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1451, \"height\": 686, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-z4r2rkpgby/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1448, \"height\": 687, \"label\": \"Table\"}]"
motivation: 现有多模态VAE硬约束限制表示学习。
method: 提出混合专家先验软约束，引导聚合后验。
result: 表示质量和插补任务性能提升。
conclusion: 软约束增强多模态VAE信息保留。
---

## Abstract
Variational Autoencoders for multimodal data hold promise for many tasks in data analysis, such as representation learning, conditional generation, and imputation.
Current architectures either share the encoder output, decoder input, or both across modalities to learn a shared representation. 
Such architectures impose hard constraints on the model. 
In this work, we show that a better latent representation can be obtained by replacing these hard constraints with a soft constraint. We propose a new mixture-of-experts prior, softly guiding each modality's latent representation towards a shared aggregate posterior.
This approach results in a superior latent representation and allows each encoding to preserve information better from its uncompressed original features. In extensive experiments on multiple benchmark datasets and two challenging real-world datasets, we show improved learned latent representations and imputation of missing data modalities compared to existing methods.

---

## 论文详细总结（自动生成）

好的，作为一名资深学术论文分析助手，我将以 Markdown 格式，对提供的论文进行结构化、深入且客观的总结。

### **1. 核心问题与整体含义**

*   **研究问题**：现有多模态变分自编码器（VAEs）为了学习共享表示，普遍采用在编码器输出、解码器输入或两者上进行聚合的架构（如专家乘积 PoE 或专家混合 MoE）。这些方法对不同模态的潜在表示施加了**硬性约束**。
*   **核心矛盾**：这种硬性聚合导致了一个难以调和的**权衡**——模型要么准确重建数据，要么学习到有意义的共享表示，但难以兼得（尤其在模态间可预测性不强时）。这使得潜在表示质量和生成样本的连贯性受限。
*   **整体含义**：论文旨在通过一种新的**软约束机制**来替代硬性聚合，从而打破上述权衡。其核心思想是 **“因多样而统一”** ，即在保持各模态独立编码、不丢失其特定信息的同时，通过一个更灵活的、数据依赖的先验，引导各模态的潜在表示在统计上趋向一致，最终获得更优的表示和生成效果。

### **2. 方法论**

#### **2.1 核心思想**

论文提出了**多模态变分混合专家先验变分自编码器**。
*   与现有方法**在编码端聚合出一个共享的联合潜在变量**不同，MMVM VAE 为**每个模态保留独立的编码器和解码器**。
*   模型不强制各模态的编码输出必须相同或服从一个简单的聚合分布。取而代之，它设计了一个**新的多模态先验分布**，该先验以“软性”的方式引导不同模态的独立后验分布相互靠近。

#### **2.2 关键技术细节：多模态混合专家先验**

*   **先验定义**：对于包含 $M$ 个模态的样本 $X = \{x_1, \dots, x_M\}$，MMVM VAE 为**每个模态 $m$** 定义了一个相同的、依赖于全部输入数据的先验分布$h(z_m | X)$。这个先验是所有模态编码器后验分布的混合：
    $$h(z | X) = \prod_{m=1}^{M} h(z_m | X), \quad \text{其中} \quad h(z_m | X) = \frac{1}{M} \sum_{\tilde{m}=1}^{M} q_{\tilde{m}\phi}(z_m | x_{\tilde{m}})$$
    
    这个设计的精妙之处在于，每一个模态的“先验”其实是其他所有模态（及自身）当前推断出的后验的混合，这就创造出了一种**跨模态的信息软共享**。

*   **目标函数解析**：在此先验下，VAE 目标函数中的正则化项（KL 散度）可以被解析为一个非常直观的形式：
    $$R = \sum_{m=1}^{M} \text{KL}\left(q^m_\phi(z_m|x_m) \Bigg|\Bigg| \frac{1}{M}\sum_{\tilde{m}} q^{\tilde{m}}_\phi(z_m|x_{\tilde{m}})\right) = M \cdot \text{JS}(q^1_\phi, \dots, q^M_\phi)$$
    
    最小化目标函数等价于**最小化所有单模态后验分布之间的 Jensen-Shannon 散度（JS散度）**。这与对比学习（contrastive learning）中最大化正样本对（此处为同一对象的不同模态）相似度的思想不谋而合，但该模型是在生成式框架下实现的。
*   **最优性证明**：论文通过引理 4.1 和变分法证明，所提出的混合专家先验是该目标下唯一的最优解。

### **3. 实验设计**

*   **基准数据集**：实验在三个常用的多模态基准数据集上进行。
    *   **Translated PolyMNIST**：将手写数字（MNIST）作为共享内容，叠加不同的随机背景和随机位移，产生多个模态。目的在于测试模型在模态间共享信息与独立信息并存时的表现。
    *   **Bimodal CelebA**：将人脸图像与其属性文本描述作为两个模态。
    *   **CUB Image-Captions**：将鸟类图片与人工生成的语言描述作为两个模态。
*   **真实世界数据集**：
    *   **海马体神经活动数据（神经科学）**：记录5只大鼠在记忆任务中的神经活动，**将每只大鼠视为一个独立的模态**，旨在发现跨被试共享的神经模式并量化个体差异。
    *   **MIMIC-CXR（医学影像）**：将胸部X光片的**正面和侧面视图作为两个模态**，用于心肺疾病的分类。
*   **对比基准方法**：论文对比了多种代表性方法，包括：
    *   **独立VAEs（Independent VAEs）**：对各模态单独训练VAE，不进行任何跨模态信息共享。
    *   **聚合式多模态VAEs**：即在编码端进行聚合的经典方法，包括 **PoE**、**MoE**、**MoPoE** 和 **平均聚合（AVG）**。
    *   **MMVAE+**：一种引入模态特定潜在子空间的变体，旨在缓解聚合VAE的生成质量下降问题。
*   **评估指标**：
    *   **潜在表示质量（Latent Representation）**：通过在训练好的编码器输出的单模态潜在表示上训练一个线性分类器，测试其分类准确率。
    *   **生成连贯性（Coherence）**：给定一个模态，条件生成另一个模态的样本，然后用一个在真实数据上预训练的非线性分类器去识别生成样本的内容（如数字/属性），准确率越高，代表生成的模态与输入模态共享信息越一致。
    *   **重建误差（Reconstruction Error）**：作为生成质量的代理指标，衡量模型对原始数据的保真度。

### **4. 资源与算力**

论文详细说明了实验所使用的GPU资源和训练时长，具体如下：

*   **Translated PolyMNIST**：使用 **NVIDIA GTX 2080** GPU，单次实验约需 **7 小时**。为覆盖不同方法和超参数，总计训练了 **330 个模型**，预估总 GPU 时长为 **2310 小时**。
*   **Bimodal CelebA**：使用 **NVIDIA GTX 2080** GPU，单次实验约需 **24 小时**。总计训练了 **180 个模型**，预估总 GPU 时长为 **4320 小时**。
*   **MIMIC-CXR（VAE部分）**：使用 **NVIDIA A100-SXM4-40GB** GPU，单次实验约需 **45 小时**。总计训练了 **9 个模型**，预估总 GPU 时长为 **405 小时**。
*   **MIMIC-CXR（监督分类器）**：使用 **NVIDIA A100-SXM4-40GB** GPU，单个模型约需 **1 小时**，共训练 6 个模型，总时长为 **6 小时**。

### **5. 实验数量与充分性**

*   **实验数量丰富**：实验覆盖了 **3 个基准数据集** 和 **2 个真实世界应用**，涉及领域广泛（图像、文本、神经科学、医学影像）。每个数据集都对比了 **6 种主流方法**。
*   **评估维度多样且设计严谨**：实验同时评估了**表示学习、生成连贯性和重建质量**三个关键维度。通过绘制“重建误差 vs. 分类/连贯性”的散点图，直观展示了不同模型在权衡曲线上的表现，比单一的分数对比更具说服力。
*   **超参数扫描确保公平**：所有模型被实现为 $\beta$-VAE，并对关键超参数 $\beta$ 进行了大范围扫描（如 PolyMNIST 上扫描了 12 个值）。图中的每个点代表了**多个随机种子下某个特定 $\beta$ 值的平均值**，这有效排除了随机性和特定超参数设置带来的偏差，确保了比较的客观和公平。

### **6. 主要结论与发现**

*   **打破权衡，实现双赢**：MMVM VAE 一致地优于所有聚合式多模态VAE。在基准数据集上，它能够在**达到相同甚至更低的重建误差的同时，显著提升潜在表示的分类性能和条件生成的连贯性**，解决了过去方法中二者不可兼得的困境。
*   **卓越的跨模态信息共享能力**：在真实世界任务（如MIMIC-CXR）中，MMVM VAE 能够通过其软共享机制强化较弱的模态。例如，使信息量较少的侧位X光片的潜在表示在疾病分类性能上，可以比肩甚至超越基线方法中信息量更丰富的正位片表示。
*   **神经科学应用潜力**：在分析大鼠记忆实验数据时，MMVM VAE 能够成功地将不同大鼠的神经活动嵌入到一个共享的、按刺激类型（气味）清晰分离的潜在空间中，而基线方法（如独立VAEs或AVG VAE）则往往按个体（老鼠）而非任务特征进行聚类，证明了其在提取跨被试共享神经表征上的有效性。

### **7. 优点**

*   **创新性强**：方法的核心思想——用**多模态混合先验实现软共享**，是一个优雅且富有洞见的创新，从根本上区别于主流的编码器聚合范式，并为VAE目标函数赋予了新的解释（最小化JS散度）。
*   **理论扎实**：不仅有直观的动机和图示，还提供了关于其先验最优性的严谨数学证明。
*   **实验说服力强**：实验部分设计得非常扎实，尤其是在二维图上展示不同 $\beta$ 值下的权衡曲线，结合多维度评估指标，有力地支撑了核心结论。
*   **应用价值高**：在神经科学和医学影像两个具有挑战性的真实领域展示了其优势，证明了该方法不只在玩具数据集上有效，而能解决实际问题。

### **8. 不足与局限**

*   **难以进行无条件生成**：由于先验是数据依赖的，模型不能像标准VAE那样直接从标准高斯分布中采样生成新数据。虽然论文提到此能力可通过伪输入或后验密度估计技术恢复，但其主要设计目标并非无条件生成。
*   **计算成本高昂**：该方法需要为每个模态配齐独立的编码器和解码器，且训练过程涉及复杂的KL散度计算，单次实验的算力消耗比简单的聚合模型更大（如CelebA上长达24小时/次）。
*   **未明确讨论负面样本问题**：目标函数通过JS散度对齐所有模态的后验，这等价于只利用了正样本对。它缺乏一个显式的机制来推开负样本（不同样本的表示），这可能在某些特定场景下限制了表示的判别能力，尽管重建损失能在一定程度上防止表示坍缩。
*   **模态数量 $M$ 的可扩展性**：模态数量较多时，计算混合先验的计算复杂度会随$M$线性增长。对于具有数以十计甚至百计模态的场景，其训练效率可能成为瓶颈。

（完）
