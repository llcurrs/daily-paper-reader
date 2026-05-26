---
title: Hyper-Modality Enhancement for Multimodal Sentiment Analysis with Missing Modalities
title_zh: 超模态增强用于缺失模态下的多模态情感分析
authors: "Yan Zhuang, Minhao LIU, Wei Bai, Yanru Zhang, Wei Li, Jiawen Deng, Fuji Ren"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=mPOQZMBKaN"
tags: ["query:multi-modal"]
score: 4.0
evidence: 通过跨样本检索解决多模态情感分析中的缺失模态问题
tldr: HME框架通过从其他样本中检索语义相关线索增强每个观测模态，避免显式重建，减少对完整训练数据的依赖，从而在不完整输入下实现鲁棒的多模态情感分析。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-mpoqzmbkan/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1396, \"height\": 786, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mpoqzmbkan/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1408, \"height\": 296, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mpoqzmbkan/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1388, \"height\": 593, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mpoqzmbkan/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1331, \"height\": 438, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mpoqzmbkan/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1330, \"height\": 439, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mpoqzmbkan/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1329, \"height\": 552, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mpoqzmbkan/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1441, \"height\": 357, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mpoqzmbkan/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1250, \"height\": 460, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1422, \"height\": 1440, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1386, \"height\": 305, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1415, \"height\": 500, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1413, \"height\": 387, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1406, \"height\": 428, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1359, \"height\": 1064, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1358, \"height\": 1063, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1379, \"height\": 373, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1299, \"height\": 302, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1074, \"height\": 145, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1075, \"height\": 407, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1087, \"height\": 577, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1078, \"height\": 425, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1262, \"height\": 293, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 549, \"height\": 144, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 536, \"height\": 142, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 714, \"height\": 222, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mpoqzmbkan/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 997, \"height\": 301, \"label\": \"Table\"}]"
motivation: 现实场景中情感分析常面临模态缺失，显式重建方法依赖完整数据，难以应对固有缺失输入。
method: 提出超模态增强框架，通过跨样本检索，为观测模态检索语义相关线索进行增强，并引入不确定性感知机制。
result: 实验表明，该方法在不完整数据下有效提升情感分析性能，降低了对完整训练数据的依赖。
conclusion: HME为缺失模态处理提供了无需重建的新思路，对真实缺失场景更具适用性。
---

## Abstract
Multimodal Sentiment Analysis (MSA) aims to infer human emotions by integrating complementary signals from diverse modalities. However, in real-world scenarios, missing modalities are common due to data corruption, sensor failure, or privacy concerns, which can significantly degrade model performance. To tackle this challenge, we propose Hyper-Modality Enhancement (HME), a novel framework that avoids explicit modality reconstruction by enriching each observed modality with semantically relevant cues retrieved from other samples. This cross-sample enhancement reduces reliance on fully observed data during training, making the method better suited to scenarios with inherently incomplete inputs. In addition, we introduce an uncertainty-aware fusion mechanism that adaptively balances original and enriched representations to improve robustness. Extensive experiments on three public benchmarks show that HME consistently outperforms state-of-the-art methods under various missing modality conditions, demonstrating its practicality in real-world MSA applications.

---

## 论文详细总结（自动生成）

## 论文总结：Hyper-Modality Enhancement for Multimodal Sentiment Analysis with Missing Modalities

### 1. 核心问题与整体含义
- **研究动机**：多模态情感分析（MSA）在现实应用中常因数据损坏、传感器故障或隐私问题导致某些模态（如视频、音频）缺失。现有方法多依赖于**显式重建缺失模态**或**教师-学生蒸馏**，这些策略在训练时通常需要完整的模态数据进行监督，难以适应“训练集本身就不完整”的真实场景。
- **整体含义**：论文提出**超模态增强（HME）框架**，不进行模态重建，而是通过**跨样本检索语义相关线索**来增强当前可观测的模态，并利用**不确定性感知融合**平衡原始与增强表示，从而在不依赖完整训练数据的前提下实现鲁棒的缺失模态情感分析。

### 2. 方法论
#### 2.1 核心思想
- 避开显式模态重建，直接从当前样本的可用模态出发，从**同一个批次的其他样本**中提取相似表示来充实该模态的特征。
- 通过**可学习 prompts** 聚合跨样本信息，并利用变分信息瓶颈（VIB）压缩噪声，最终用不确定性权重融合原始特征与增强特征。

#### 2.2 关键技术细节
- **预处理模块**：使用1D卷积对齐维度，Transformer Encoder 提取动态特征，池化得到模态表示 \(H_m\)。
- **超模态表示生成模块（Hyper-Modality Representation Generation）**：
  1. **模态增强（Modality Enhancement）**：对每个模态，计算批次内所有样本的余弦相似度，选取大于阈值 \(t_s\) 的样本，再求平均得到增强表示 \(H'_m\)；若无可选样本则用该模态所有非缺失表示的平均。然后通过 **Perceiver 模型**，用可学习的 prompts \(E'_m\) 作为 query，从 \(H'_m\) 中聚合信息，得到增强的模态表示 \(E_m\)。同时，引入跨模态的共享 prompts \(E'_S\) 聚合所有可用模态的信息得到 \(E_S\)。
  2. **超模态生成（Hyper-Modality Generation）**：以语言模态为例，用 \(E_L\) 作为 query 分别与 \(E_V\)、\(E_A\) 做交叉注意力，再以 \(E_S\) 为 query 融合两者，生成超模态表示 \(R_m\)。三个模态均进行此操作。
  3. **变分信息瓶颈（VIB）**：对 \(R_m\) 进行压缩去噪，优化 \(\mathcal{L}_{VIB} = \frac{1}{N}\sum \mathcal{L}_{TASK}(\hat{y}_{vib}, y) + \beta\,KL(p(z|x)\|\mathcal{N}(0,I))\)，得到紧凑表示 \(F_m\) 及对应的标准差 \(\sigma_m\)。
- **多模态超模态融合模块（Multimodal Hyper-Modality Fusion）**：
  - 将标准差倒数作为不确定性权重 \(\zeta_m\)，并限制在区间 \([t_l, t_u]\) 内，确保增强表示的影响不超过原始表示。
  - 对每模态，将 \(H_m\) 和 \(F_m\) 拼接后计算注意力权重，再与不确定性权重 \(U^2_m = [1.0, \zeta_m]\) 结合，得到融合表示 \(S_m\)。
  - 三个模态的 \(F_m\) 堆叠后同样用不确定性权重 \(U^3_m = \frac{e^{\zeta_m}}{\sum e^{\zeta_m}}\) 进行融合，得到 \(S_H\)。
  - 将所有融合特征送入 Transformer 编码器和 MLP，输出最终预测 \(\hat{y}\)。
- **整体损失**：\(\mathcal{L}_{all} = \mathcal{L}_{TASK}(\hat{y}, y) + \alpha \mathcal{L}_{VIB}\)，其中 \(\alpha\) 为平衡系数。

#### 2.3 算法流程（文字概括）
> 对每个批次：
> 1. 提取各模态初始表示，模拟缺失（随机置零），经卷积和 Transformer 得 \(H_m\)。
> 2. 对每个模态，基于余弦相似度选择相似样本，平均后输入 Perceiver + 提示 tokens 生成增强表示 \(E_m\)，同时生成共享表示 \(E_S\)。
> 3. 通过交叉注意力将 \(E_m\) 与其他模态的 \(E\) 交互，再由 \(E_S\) 聚合得 \(R_m\)，经 VIB 压缩为 \(F_m\)。
> 4. 利用 \(F_m\) 的标准差计算不确定性权重，与 \(H_m\) 融合，再跨模态融合，最终预测情感标签。

### 3. 实验设计
- **数据集与场景**：
  - 主要数据集：CMU-MOSI、CMU-MOSEI、IEMOCAP（回归/分类任务），另有 UR-FUNNY、MUStARD 用于泛化分析。
  - 评估指标：准确率（ACC）、F1 分数；MOSI 和 MOSEI 使用二分类（正/负）指标，IEMOCAP 使用四分类平均指标。
- **缺失模拟协议**：
  - **固定缺失协议**：训练时全模态，验证和测试时固定去除某一种或多种模态（如仅保留语言、仅保留视频等）。
  - **随机缺失协议**：训练、验证、测试时按全局缺失率（MR = \(1 - \frac{\sum a_i}{3N}\)，\(a_i\) 为第 \(i\) 个样本可用模态数）随机丢弃模态，MR 取 0.0~0.7（步长 0.1）。
- **对比方法**：GCNet、MPLMM、DiCMoR、IMDer、LNLN 等专门针对缺失模态的 SOTA 模型。部分方法因设定不同，重新实现并标记为 †。

### 4. 资源与算力
- **硬件**：所有实验在 **NVIDIA GTX 3090 GPU** 上进行（文中未明确数量，推测单卡）。
- **训练时长**：论文给出了 MOSI 数据集上训练 100 个 epoch 的时间对比。HME 训练仅需 **684 秒**，远少于 MPLMM（约 3,433s）、DiCMoR（约 12,792s）和 IMDer（约 175,138s），效率显著。
- **参数规模**：HME 约 1.18 亿参数，处于中等水平。
- **峰值显存**：随 batch size 变化，例如 batch size=64 时峰值约 5.6GB，256 时约 13.2GB。

### 5. 实验数量与充分性
- **主要对比实验**：在 3 个数据集、两种缺失协议、多种缺失模式（固定 7 种，随机 8 种缺失率）下，与 5 种 SOTA 方法比较，表格覆盖全面。
- **消融实验**：移除各模态增强表示（w/o \(E_m\)）、移除共享表示（w/o \(E_S\)）、移除不确定性权重（w/o \(U_m\)）、移除超模态生成模块（w/o HMG）、移除 VIB（w/o VIB），展示了各组件的贡献。
- **深入分析**：
  - 训练损失收敛曲线与 t-SNE 可视化。
  - 不确定性权重与缺失率、相似度阈值的关系分析。
  - 错误分析（负增强现象）、泛化实验（跨数据集、作为插件 module）、计算效率对比、超参数敏感性（\(t_s, t_u, l_p\)）等。
- **评估公平性**：为公平对比，对基线方法进行重实现且与原作保持相同训练范式；采用五轮平均，并报告 95% 置信区间。
- 总体来看，实验设计**系统、充分、客观**。

### 6. 主要结论与发现
- HME 在固定和随机缺失协议下**一致优于现有 SOTA**，尤其在模态缺失严重时优势更明显。
- **跨样本增强**和**不确定性融合**是性能提升的关键，消融实验表明移除任一组件均导致性能下降。
- VIB 能有效过滤相似样本引入的噪声，提高表示质量。
- HME **不依赖训练时的完整模态数据**，更贴近真实部署场景，且计算效率高。

### 7. 优点
- **无需显式重建**：避免了重建损失和伪缺失训练的限制，可直接用不完整数据训练。
- **跨样本增强思想**：充分利用批次内样本间语义相关性，打破了单样本独立处理的局限。
- **不确定性感知融合**：利用 VIB 输出的标准差动态评估增强表示的可信度，抑制噪声。
- **高效且有效**：相对同类方法大幅缩短训练时间，同时保持较低参数量。
- **实验全面**：涵盖多个数据集、多种缺失模式、丰富的消融与分析实验，支撑力强。

### 8. 不足与局限
- **冗余与噪声**：VIB 力求压缩去噪，但**生成多个模态的独立表示仍可能存在信息冗余**。
- **原始模态噪声未考虑**：方法仅处理来自其它样本的噪声，**未对原始模态内部可能存在的噪声**进行建模。
- **负增强风险**：相似样本可能标签相反，尽管 VIB 和阈值能部分缓解，但**极端情况下冲突信号仍会影响模型**。
- **对批次大小的依赖**：增强表示的多样性依赖于批次内的可用样本，**小批量可能削弱效果**；且增大批次会提高显存需求。
- **泛化局限性**：跨数据集迁移时（如从 MUStARD 到 UR-FUNNY）性能下降明显，表明**对数据分布差异较为敏感**。
- **可解释性**：学习到的 prompts 无法显式区分各样本的贡献，**增强过程的可解释性**有待提升。

（完）
