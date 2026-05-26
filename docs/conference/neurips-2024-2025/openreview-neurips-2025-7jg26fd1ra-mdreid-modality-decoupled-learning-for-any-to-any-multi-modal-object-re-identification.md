---
title: "MDReID: Modality-Decoupled Learning for Any-to-Any Multi-Modal Object Re-Identification"
title_zh: MDReID：面向任意到任意多模态物体重识别的模态解耦学习
authors: "Yingying Feng, Jie Li, Jie Hu, Yukang Zhang, Lei Tan, Jiayi Ji"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=7jg26Fd1ra"
tags: ["query:multi-modal"]
score: 5.0
evidence: 解耦模态特征实现任意到任意的多模态匹配
tldr: 多模态物体重识别通常假设模态匹配，但在实际应用中模态不一致问题突出。MDReID通过模态解耦模块分离模态共享与特定特征，并利用模态感知聚合实现任意模态到任意模态的检索，实验表明在多种模态不匹配场景下表现鲁棒，但未在遥感图像分类中测试。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-7jg26fd1ra/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1441, \"height\": 520, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7jg26fd1ra/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1423, \"height\": 799, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7jg26fd1ra/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1436, \"height\": 347, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-7jg26fd1ra/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1090, \"height\": 687, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7jg26fd1ra/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1439, \"height\": 353, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7jg26fd1ra/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1242, \"height\": 417, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7jg26fd1ra/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 694, \"height\": 253, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7jg26fd1ra/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 328, \"height\": 251, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7jg26fd1ra/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 343, \"height\": 248, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7jg26fd1ra/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1244, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7jg26fd1ra/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 640, \"height\": 192, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7jg26fd1ra/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 535, \"height\": 141, \"label\": \"Table\"}]"
motivation: 现有多模态重识别假设模态匹配，难以应对真实应用中模态不一致的挑战。
method: 提出MDReID，包含模态解耦模块和模态感知聚合，分离共享与特定特征，支持任意模态匹配。
result: 在多个基准上，MDReID在模态不匹配情况下显著优于现有方法，但尚未在遥感分类中评估。
conclusion: 为多模态学习中的模态不一致问题提供了有效思路，有望扩展到遥感图像缺失模态场景。
---

## Abstract
The challenge of inconsistent modalities in real-world applications presents significant obstacles to effective object re-identification (ReID). However, most existing approaches assume modality-matched conditions, significantly limiting their effectiveness in modality-mismatched scenarios. To overcome this limitation and achieve a more flexible ReID, we introduce MDReID to allow any-to-any image-level ReID systems. MDReID is inspired by the widely recognized perspective that modality information comprises both modality-shared features, predictable across modalities, and unpredictable modality-specific features, which are inherently modality-dependent and consist of two key components: the Modality Decoupling Module (MDM) and Modality-aware Metric Learning (MML). Specifically, MDM explicitly decomposes modality features into modality-shared and modality-specific representations, enabling effective retrieval in both modality-aligned and mismatched scenarios. MML, a tailored metric learning strategy, further enhances feature discrimination and decoupling by exploiting distributional relationships between shared and specific modality features. Extensive experiments conducted on three challenging multi-modality ReID benchmarks (RGBNT201, RGBNT100, MSVR310) consistently demonstrate the superiority of MDL. MDReID achieves significant mAP improvements of 9.8\%, 3.0\%, and 11.5\% in modality-matched scenarios, and average gains of 3.4\%, 11.8\%, and 10.9\% in modality-mismatched scenarios, respectively.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **背景与问题**：在实际视频监控、智能交通等应用中，物体重识别常面临多种光谱传感器（RGB、近红外NIR、热红外TIR）混合部署的情况，导致查询图像与库图像的模态组合不可预知（如RGB查询、NIR库，或部分模态缺失）。然而，现有大多数多模态ReID方法均假设查询与库的模态完全对齐（即“模态匹配”），严重限制了其在真实异质环境下的灵活性与鲁棒性。
- **核心目标**：提出一种**任意到任意（any-to-any）**的图像级多模态物体重识别框架——MDReID，使其无论查询与库图像来自何种模态组合，都能有效检索，填补了当前方法在“模态不匹配”场景下的空白。
- **核心思想**：将每个模态的特征显式解耦为**模态共享特征**（可跨模态预测、迁移）和**模态特定特征**（保留不可预测的独特信息），并设计专门的度量学习策略强化二者的正交性与互补性，从而在不同模态组合下均能获得高判别力表征。

### 2. 方法论

MDReID基于ViT架构，包含两个关键组件：**模态解耦学习（MDL）** 和**模态感知度量学习（MML）**。

#### 2.1 模态解耦学习（MDL）
- 为每个模态输入（如RGB、NIR、TIR）在ViT的patch嵌入序列前额外添加两个可学习的令牌：**模态特定令牌** \(I^M_{sp}\) 和**模态共享令牌** \(I^M_{sh}\)。经过Transformer编码后，得到一个样本的全部特征。
- 构造固定维度的全特征向量 \(v_{full} = [I^R_{sp}, I^N_{sp}, I^T_{sp}, I^R_{sh}, I^N_{sh}, I^T_{sh}]\)，并维护一个二值**可用性掩码**（某模态存在则对应位置为1，否则为0）。
- 在检索时，无论查询与库的模态如何，均按掩码生成各自的零填充特征向量。相似度由两部分加权求和：
  - **模态特定相似度** \(Sim_{sp}\)：仅在同模态特定特征之间计算点积，并由联合可用性掩码缩放。
  - **模态共享相似度** \(Sim_{sh}\)：计算所有可用共享特征两两之间的相似度矩阵，再与配对掩码点乘后求和。
- 最终总相似度为 \((Sim_{sp} + Sim_{sh}) / 2\)，实现了对任意模态组合的灵活支持。

#### 2.2 模态感知度量学习（MML）
在训练阶段（假设所有模态均存在），为强化解耦效果，引入两个互补损失：
- **表示正交性损失（ROL）**：定义理想的6×6相关性目标矩阵 \(A\)（特定特征间呈单位阵无跨模态关联，共享特征间全为1高相关，特定与共享间为0正交），计算特征向量内积相似度矩阵与\(A\)的均方误差，强制共享特征跨模态对齐，特定与共享正交。
- **知识差异损失（KDL）**：借鉴三元组思想，确保**组合特征（特定+共享）**比单用特定或单用共享特征更能拉近同类、推远异类样本。通过约束组合特征与单类特征在正样本最大距离和负样本最小距离上的差异实现互补。
- 总MML损失为 \(L_{MML} = w_1 \cdot L_{ROL} + w_2 \cdot L_{KDL}\)。

#### 2.3 整体优化
基础损失包括标签平滑交叉熵损失 \(L_{ce}\) 和三元组损失 \(L_{tri}\)，总目标为 \(L = L_{ce} + L_{tri} + L_{MML}\)。

### 3. 实验设计

- **数据集**：三个公开多光谱ReID基准——
  - **RGBNT201**：行人重识别，包含201个ID，各提供RGB、NIR、TIR三模态图像，共4787张。评测多种模态匹配与不匹配场景。
  - **RGBNT100**：车辆重识别，100辆车，17250组三模态图像。
  - **MSVR310**：车辆重识别，310辆车，6261张图像，同样包含RGB/NIR/TIR。
- **评价指标**：平均精度（mAP）和CMC Rank-1、Rank-5、Rank-10。
- **对比方法**：
  - 单谱方法：MUDeep、HACNN、BoT、TransReID、AGW等。
  - 多谱方法：PFNet、EDITOR、TOP-ReID、UniCat、CCNet、HTT、RSCNet等。
- **评测场景**：
  - 全模态匹配（RNT-to-RNT）。
  - 部分模态缺失（如仅使用两种模态，或缺少一种/多种）。
  - 模态不匹配（如RT-to-NT、R-to-N、R-to-NT等四种典型跨模态组合）。
  - 补充对比了专门针对R-to-N跨模态方法的DEEN。

### 4. 资源与算力

- **硬件**：所有实验在**单块NVIDIA RTX 4090 GPU**上完成。
- **框架与精度**：PyTorch，CUDA 12.5，Python 3.8，使用CLIP-Base视觉编码器作为主干。
- **训练配置**：图片大小调整为256×128或128×256，采用随机翻转、裁剪、擦除等增强。优化器为Adam，batch size 64，学习率基值3.5e-4，视觉编码器微调学习率5e-6，训练**50个epoch**。
- 论文未明确给出单次训练的总时长，但提供了各方法与MDReID的特征提取和检索耗时对比（如RGBNT201上MDReID提取特征仅需3.27s），表明计算效率较高，参数仅57.2M，FLOPs 22.3G，明显低于TOP-ReID等模型。

### 5. 实验数量与充分性

- **实验矩阵全面**：
  - **主流数据集全覆盖**：3个数据集上均进行了模态匹配、模态不匹配、缺失模态等全面评测。
  - **系统消融实验**：在RGBNT201上逐步验证MDL、ROL、KDL的贡献，共计5组配置，并分析了超参数\(w_1\)和\(w_2\)的影响（各测试5个取值）。
  - **对比广泛**：与10余种单谱/多谱先进方法比较，涉及多种模态组合下的表格数据。
  - **专门分析**：评估了仅用共享/特定特征时的性能，并与跨模态专用方法DEEN对比，证明单一模型即可泛化。
  - **可视化解释**：通过t-SNE特征可视化展示ROL、KDL对特征分布的解耦效果。
  - **计算量分析**：对比参数、FLOPs和时间开销。
- **客观性与公平性**：所有对比均基于官方开源实现或原文结果，实验设定明确，使用相同骨干网络为基线，确保了公平比较。消融实验从单一模块逐步累加，结论可信。

### 6. 主要结论与发现

- MDReID在三个数据集的所有评估场景下均取得**最优或次优**性能：
  - 模态匹配场景mAP提升达9.8%（RGBNT201）、3.0%（RGBNT100）、11.5%（MSVR310）。
  - 模态不匹配场景平均mAP增益分别为3.4%、11.8%、10.9%。
  - 在部分模态缺失时，mAP平均超越TOP-ReID约10.0%。
- **解耦学习显著有效**：MDL将特征分为共享与特定后，平均mAP/ R-1相对基线提升11%以上。
- **ROL和KDL互补**：ROL强制共享特征对齐和跨组件正交，是性能提升的关键；KDL进一步确保组合特征优于独立特征，二者结合效果最佳。
- **高计算效率**：在参数量、FLOPs和实际推理速度上均显著优于主流方法，实现了精度与效率的最优平衡。

### 7. 优点

- **任务设定新颖实用**：首次系统性地定义并解决“任意到任意”多模态物体重识别问题，直接应对真实部署中的模态不确定性。
- **方法设计精巧**：
  - 将模态特征解耦为可预测的共享部分和不可预测的特定部分，从机理上缓解跨模态匹配困难。
  - 提出的掩码特征向量与相似度计算方式，可无缝处理各种模态存活与缺失的组合。
  - MML通过相关性矩阵和知识差异损失从度量层面强化了解耦，特征可视化结果显示特征空间分布更加清晰。
- **性能全面领先**：在行人、车辆两类数据上均大幅度提升，尤其在不匹配和缺失场景下鲁棒性极强。
- **高效轻量**：仅需57.2M参数、22.3G FLOPs，推理速度远超同精度水平的大模型，适合部署。
- **可复现性强**：提供了完整代码、实验细节及超参数选择依据。

### 8. 不足与局限

- **精度仍难满足实际部署**：作者在附录中明确承认，即使显著提升，当前任意到任意场景下的绝对精度（如R-to-N mAP仅16.6%）仍不足以直接用于高可靠性要求的生产环境。
- **数据集规模与模态多样性有限**：现有公开数据集仅涉及RGB、NIR、TIR三种模态，且样本量不大，MDReID在更大规模、更多模态类型（如深度图、高光谱）上的泛化性未知。
- **未在遥感等特殊领域验证**：论文未涉及遥感图像分类、场景理解等同样存在多模态缺失的应用，其结论的扩展性尚需进一步检验。
- **潜在社会影响未充分讨论**：文中虽提及无负面社会影响，但重识别技术本身涉及隐私与监控伦理，这一维度未作探讨。

（完）
