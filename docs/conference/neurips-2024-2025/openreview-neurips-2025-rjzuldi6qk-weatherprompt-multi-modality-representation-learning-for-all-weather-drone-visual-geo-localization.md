---
title: "WeatherPrompt: Multi-modality Representation Learning for All-Weather Drone Visual Geo-Localization"
title_zh: WeatherPrompt：面向全天候无人机视觉地理定位的多模态表示学习
authors: "Jiahao Wen, Hang Yu, Zhedong Zheng"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=RjZUldI6Qk"
tags: ["query:multi-modal"]
score: 7.0
evidence: 融合图像与文本模态实现全天候无人机视觉地理定位
tldr: 针对无人机视觉定位在恶劣天气下性能下降的问题，提出WeatherPrompt，通过融合图像嵌入与大型多模态模型合成的气象文本描述，学习天气不变表征。框架包含免训练天气推理机制和文本上下文融合模块。实验表明，该方法在多种天气条件下显著提升定位精度，为鲁棒无人机导航提供了多模态解决方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-rjzuldi6qk/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1314, \"height\": 353, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rjzuldi6qk/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1400, \"height\": 780, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rjzuldi6qk/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1440, \"height\": 674, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rjzuldi6qk/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1400, \"height\": 374, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-rjzuldi6qk/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1449, \"height\": 454, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rjzuldi6qk/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1447, \"height\": 325, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rjzuldi6qk/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1329, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rjzuldi6qk/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 706, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rjzuldi6qk/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 709, \"height\": 214, \"label\": \"Table\"}]"
motivation: 恶劣天气导致无人机视觉定位特征退化，现有方法泛化不足。
method: 利用大模型合成多天气文本描述，与图像嵌入融合学习天气不变特征。
result: 在雾、雨等天气条件下，定位性能优于现有方法。
conclusion: 展示了语言与视觉融合在无人机鲁棒定位中的价值。
---

## Abstract
Visual geo-localization for drones faces critical degradation under weather perturbations, \eg, rain and fog, where existing methods struggle with two inherent limitations: 1) Heavy reliance on limited weather categories that constrain generalization, and 2) Suboptimal disentanglement of entangled scene-weather features through pseudo weather categories.
We present WeatherPrompt, a multi-modality learning paradigm that establishes weather-invariant representations through fusing the image embedding with the text context. 
Our framework introduces two key contributions: First, a Training-free Weather Reasoning mechanism that employs off-the-shelf large multi-modality models to synthesize multi-weather textual descriptions through human-like reasoning. It improves the scalability to unseen or complex weather, and could reflect different weather strength. 
Second, to better disentangle the scene and weather features, we propose a multi-modality framework with the dynamic gating mechanism driven by the text embedding to adaptively reweight and fuse visual features across modalities. The framework is further optimized by the cross-modal objectives, including image-text contrastive learning and image-text matching, which maps the same scene with different weather conditions closer in the representation space. 
Extensive experiments validate that, under diverse weather conditions, our method achieves competitive recall rates compared to state-of-the-art drone geo-localization methods. Notably, it improves Recall@1 by 13.37\% under night conditions and by 18.69\% under fog and snow conditions. Our code is available at https://github.com/Jahawn-Wen/WeatherPrompt.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究动机**：无人机视觉地理定位在**雨、雾、雪等恶劣天气**下性能急剧退化，现有方法存在两个固有局限：
  - 过度依赖**封闭的天气类别**（如晴天、雨天），难以泛化到未见或复合天气。
  - **场景语义与天气扰动特征高度纠缠**，仅靠伪粗粒度天气标签无法有效解耦，导致跨天气检索性能差。
- **整体含义**：提出 **WeatherPrompt**，一种**多模态学习范式**，通过融合图像嵌入与大型多模态模型生成的**链式思维文本描述**，学习**天气不变的表征**，从而显著提升全天候跨视角地理定位鲁棒性。

### 2. 方法论
#### 2.1 免训练天气推理机制
- 利用现成大视觉语言模型（**Qwen2.5-VL**）通过**链式思维（CoT）提示**自动生成结构化文本描述，无需人工标注。
- **两阶段描述生成**：
  1. **天气估计阶段**：三步推理（全局能见度评估→局部气象线索识别→综合天气分类），强制输出准确、一致的天气标签。
  2. **空间语义阶段**：基于天气先验，依次推理宏观布局（建筑分布、道路方向）、微观结构（物体计数、形状）和拓扑关系，生成结构化场景描述。
- 仅从每个区域随机采样**一张无人机图像**作为代表，结合合成天气变化（使用`imgaug`库）生成多天气图像-文本对，避免信息冗余。

#### 2.2 多模态对齐与动态门控融合
- **框架组成**：预训练视觉编码器（Swin Transformer）、文本编码器（BERT）、跨模态融合模块、轻量分类头。
- **动态门控机制**：文本嵌入 \(f_T\) 通过两层线性变换生成通道级门控向量 \(g \in (0,1)^{B \times D}\)，融合特征为  
  \[
  f_{\text{fuse}} = g \odot f_I + (1 - g) \odot f_T
  \]
  使得气象语义自适应调节视觉通道，实现场景-天气特征解耦。
- **优化目标**（联合损失）：
  - **Image-Text Contrastive (ITC)**：对齐全局视觉和文本表示。
  - **Image-Text Matching (ITM)**：利用硬负样本增强细粒度判别力。
  - **Localized Alignment (LOA)**：监督预测的视觉区域坐标（中心+宽高）与文本描述的局部区域对齐，使用IoU和L1损失。
  - **分类交叉熵 (CE)**：基于融合特征预测地理位置类别。
  - 总损失：\(\mathcal{L}_{\text{total}} = \mathcal{L}_{\text{ITC}} + \mathcal{L}_{\text{ITM}} + \mathcal{L}_{\text{LLA}} + \mathcal{L}_{\text{CE}}\)

### 3. 实验设计
- **数据集**：
  - **University-1652**：1652个大学场景，训练701个地点、测试951个，每个地点包含多张无人机视图和一张卫星视图。
  - **SUES-200**：200个上海地点，覆盖4种飞行高度（150–300m），更真实的城市、公园、湖泊等场景。
  - **真实世界视频**：从YouTube收集54段无人机-卫星视频对，覆盖暗光、雨、雾三种天气。
- **天气模拟**：使用`imgaug`生成10种天气条件（Normal, Fog, Rain, Snow, Fog+Rain, Fog+Snow, Rain+Snow, Dark, Over-exp, Wind）。
- **对比方法**：包括ResNet-101, DenseNet121, Swin-T, IBN-Net, LPN, Sample4Geo, Safe-Net, CCR, MuSe-Net 等主流跨视角地理定位方法。
- **评估指标**：Recall@1、AP，分Drone→Satellite和Satellite→Drone两个检索方向。

### 4. 资源与算力
- **GPU**：单张 **NVIDIA RTX A6000**（48GB显存）。
- **训练设置**：SGD优化器（动量0.9，权重衰减0.0005），训练210轮，学习率在第120和180轮衰减10倍。输入图像尺寸384×384。
- **推理速度**：平均每查询**0.024秒**。
- **训练时间**：论文**未明确报告**总训练时长或显存占用细节。

### 5. 实验数量与充分性
- **主要对比实验**：
  - 在**University-1652**上展示10种天气下的Drone↔Satellite双向检索结果（共约20个子表项）。
  - 在**SUES-200**上同样进行双向多天气评估（约20个子表项）。
- **消融研究**（Table 3）：
  1. **门控机制对比**：拼接融合 vs. 静态平均门控 vs. 动态门控（验证动态门控提升约2.3% AP）。
  2. **CoT步骤数量**：从0步（无文本）到2、4、6步推理，表明步骤越多性能越好（6步最佳）。
  3. **真实世界混合天气**：Dark+Rain+Fog下的检索性能（R@1、R@5、R@10及AP），大幅领先对比方法。
- **定性展示**：通过检索案例可视化恶劣天气下的匹配效果。
- **充分性与公平性**：实验覆盖两个主流基准、多种天气复合、消融细致，对比方法包含SOTA，并统一使用官方的训练/测试分割和评价指标，**公平性较好**。但未提供多次运行的**标准差或置信区间**，也未进行统计显著性检验。

### 6. 主要结论与发现
- WeatherPrompt在**University-1652**上Drone→Satellite任务平均R@1达**77.14%**，较最优对比方法提升**+11.99%**；Satellite→Drone平均R@1达87.72%，提升3.04%。
- 在**SUES-200**上同理取得**显著提升**（Drone→Satellite R@1从52.02%→62.52%；Satellite→Drone R@1从69.43%→80.73%）。
- 在**夜间**和**雾+雪**等极端条件下改进尤为突出（R@1分别提升13.37%和18.69%）。
- 在**未见复合天气**（Dark+Rain+Fog）下仍保持高准确率（AP: Drone→Satellite 64.94%，Satellite→Drone 72.15%），验证了方法的跨域泛化能力。
- 消融实验证实了**CoT结构提示**和**动态气象门控**的关键作用。

### 7. 优点
- **创新性免训练描述生成**：利用大模型和CoT提示自动产出高质量多气象文本，规避人工标注，易于扩展。
- **语义解耦策略**：文本驱动的动态门控实现了场景与天气特征的细粒度分离，增强了对未见天气的鲁棒性。
- **多粒度对齐**：全局（ITC）、实例级（ITM）与局部区域（LOA）三层对齐，促使模型学习更鲁棒的多模态表示。
- **实验全面**：在两个跨视角基准、10种天气组合及真实视频上全面验证，消融实验设计严谨。
- **实用导向**：单次推理仅0.024秒，适合资源受限的无人机平台。

### 8. 不足与局限
- **数据集地理与天气多样性不足**：依赖的University-1652和SUES-200覆盖的场景和气象类型仍有限，可能影响在极端/区域特有天气下的泛化。
- **语言模型固有偏差**：描述生成采用的Qwen2.5-VL在预训练语料中可能携带描述粒度偏差（例如“薄雾”与“雾”的区分），可能影响对齐精度。
- **隐私与伦理未讨论**：论文未探讨视觉地理定位技术在隐私监控、敏感区域识别等方面的负面影响。
- **统计可靠性待加强**：未提供多次实验的误差条或标准差，结果的统计显著性未被验证。
- **计算资源信息不完整**：未报告完整训练时长、显存占用，不利于完全复现的资源预估。
- **合成天气可能与真实退化存在差距**：训练中天气效果通过`imgaug`合成，与真实世界中的复杂退化（如动态雨痕、非均匀雾）可能存在分布差异，虽然作者用YouTube视频做了验证，但数量有限。

（完）
