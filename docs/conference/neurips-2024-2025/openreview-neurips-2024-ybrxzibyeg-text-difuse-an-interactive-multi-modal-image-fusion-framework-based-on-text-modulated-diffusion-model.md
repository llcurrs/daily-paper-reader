---
title: "Text-DiFuse: An Interactive Multi-Modal Image Fusion Framework based on Text-modulated Diffusion Model"
title_zh: Text-DiFuse：基于文本调制扩散模型的交互式多模态图像融合框架
authors: "Hao Zhang, Lei Cao, Jiayi Ma"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=yBrxziByeG"
tags: ["query:multi-modal"]
score: 7.0
evidence: 多模态图像融合框架
tldr: 该文针对多模态融合中的复合退化问题，提出基于文本调制扩散模型的交互式融合框架Text-DiFuse，将特征级信息集成到扩散过程中，实现自适应退化去除与融合。实验表明提升了融合图像质量。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-ybrxzibyeg/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1422, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ybrxzibyeg/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1442, \"height\": 860, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ybrxzibyeg/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1414, \"height\": 930, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ybrxzibyeg/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1412, \"height\": 913, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ybrxzibyeg/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1414, \"height\": 408, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ybrxzibyeg/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1430, \"height\": 359, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ybrxzibyeg/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1430, \"height\": 319, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ybrxzibyeg/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1379, \"height\": 494, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-ybrxzibyeg/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 427, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ybrxzibyeg/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1442, \"height\": 423, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ybrxzibyeg/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1442, \"height\": 438, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ybrxzibyeg/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1445, \"height\": 315, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ybrxzibyeg/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1411, \"height\": 156, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-ybrxzibyeg/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1303, \"height\": 354, \"label\": \"Table\"}]"
motivation: 现有多模态融合忽略复合退化与前景对象显著性。
method: 提出Text-DiFuse，融合特征级信息到扩散模型。
result: 自适应去除退化，突出对象显著性。
conclusion: 文本调制扩散模型提升多模态图像融合质量。
---

## Abstract
Existing multi-modal image fusion methods fail to address the compound degradations presented in source images, resulting in fusion images plagued by noise, color bias, improper exposure, etc. Additionally, these methods often overlook the specificity of foreground objects, weakening the salience of the objects of interest within the fused images. To address these challenges, this study proposes a novel interactive multi-modal image fusion framework based on the text-modulated diffusion model, called Text-DiFuse. First, this framework integrates feature-level information integration into the diffusion process, allowing adaptive degradation removal and multi-modal information fusion. This is the first attempt to deeply and explicitly embed information fusion within the diffusion process, effectively addressing compound degradation in image fusion. Second, by embedding the combination of the text and zero-shot location model into the diffusion fusion process, a text-controlled fusion re-modulation strategy is developed. This enables user-customized text control to improve fusion performance and highlight foreground objects in the fused images. Extensive experiments on diverse public datasets show that our Text-DiFuse achieves state-of-the-art fusion performance across various scenarios with complex degradation. Moreover, the semantic segmentation experiment validates the significant enhancement in semantic performance achieved by our text-controlled fusion re-modulation strategy. The code is publicly available at https://github.com/Leiii-Cao/Text-DiFuse.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **研究背景**：现有多模态图像融合方法（如红外-可见光、医学图像融合）在源图像存在复合退化（如噪声、偏色、曝光不当）时，融合结果质量差，且缺乏对前景目标（如行人、车辆）的显著性关注，不利于后续任务（如语义分割、目标检测）。
- **核心问题**：
  - **复合退化挑战**：传统方法难以同时去除多种退化并有效融合多模态信息。
  - **目标欠定制化局限**：现有方法对场景中所有区域采用相同融合规则，忽略了用户对特定前景目标的兴趣。
- **整体含义**：提出一个交互式多模态图像融合框架Text-DiFuse，首次将特征级信息融合显式嵌入扩散模型，实现自适应退化去除与融合；并通过文本调制和零样本定位，允许用户用自然语言定制融合规则，增强目标显著性。

### 2. 方法论

- **核心思想**：耦合信息融合与扩散模型，同时支持文本控制的再调制。
- **关键技术细节**：
  - **显式耦合范式（扩散融合）**：
    - 将退化去除先验嵌入扩散模型的编解码网络，对亮度分量和色彩分量独立扩散（基于iDDPM）。
    - 设计**融合控制模块（FCM）**，基于CBAM注意力的卷积层生成多模态特征的融合权重（公式3）。
    - 在T步反向采样中，编码特征经FCM融合后输入解码器，同时完成去噪和融合，约束融合结果保留最大对比度和丰富纹理（强度损失L_int和梯度损失L_grad，公式9-11）。
    - 色彩分量经单独扩散去噪后，与亮度融合结果组合，得到最终融合图像。
  - **文本控制的融合再调制策略**：
    - 利用OWL-ViT进行文本驱动的开放词汇目标检测，SAM进行像素级分割得到目标掩码M。
    - 设计再调制模块，结合内置对比度增强先验，生成调制系数{κ}，调整目标区域的特征融合权重（公式12），最终通过掩码加权保持非目标区域原有分布（公式13）。
- **算法流程**：
  1. 输入退化多模态图像对，分离亮度[\(X_b\)]和色彩[\(X_c\)]。
  2. 色彩分量经扩散模型去噪得到清洁色彩分量。
  3. 亮度分量与另一模态（如红外）作为条件，输入共享编码器，在每步采样中通过FCM融合特征，预测噪声和方差，更新潜变量，最终生成清洁融合亮度分量。
  4. 融合亮度与色彩分量合成最终图像。
  5. 用户可通过文本指令触发再调制，增强目标区域的显著性。

### 3. 实验设计

- **数据集**：
  - 红外-可见光融合（IVIF）：MSRS数据集（485训练/100测试），泛化评估用LLVIP（60对）、RoadScene（25对）。
  - 医学图像融合（MIF）：哈佛医学数据集（160训练/50测试），含CT-MRI、PET-MRI、SPECT-MRI。
  - 再调制验证：MFNet数据集（用于RGB-T语义分割）；MSRS用于目标检测。
- **对比方法**：9种先进方法：RFN-Nest、GANMcC、SDNet、U2Fusion、TarDAL、DeFusion、LRRNet、DDFM、MRFS。在增强预处理实验中额外引入CLIP-LIT、SDAP、AWB。
- **评估指标**：EN、AG、SD、SCD、VIF；语义分割用mIoU，目标检测用mAP。

### 4. 资源与算力

- **计算资源**：实验在 **NVIDIA RTX 3090 GPU** 和 Intel i7-10700K CPU 上进行。未明确提供训练时长或GPU数量。

### 5. 实验数量与充分性

- **实验组数**：
  - 主要对比实验：在MSRS和哈佛数据集上与9种方法对比，含定量和定性分析。
  - 增强预处理对比实验：对上述方法增加去噪、低光增强、白平衡预处理后再对比。
  - 泛化性实验：在LLVIP和RoadScene上测试。
  - 再调制验证：在MFNet上的语义分割（6种RGB-T分割方法 + SegNext在不同输入上的训练）；在MSRS上的目标检测（YOLOv5）。
  - 消融实验：8种变体，验证FCM不同融合规则、损失函数、扩散/自编码器路线。
- **充分性与客观性**：实验覆盖了复合退化、不同模态、跨数据集泛化、语义下游任务、多个先进对比方法和多种指标，消融设计较全面，对比公平（含预处理增强基线）。实验规模足够支撑所提主张。

### 6. 主要结论与发现

- Text-DiFuse在多种复杂退化场景下均达到SOTA融合性能（定量指标最优，定性结果噪声/偏色/曝光改善显著）。
- 文本控制的再调制策略能有效提升融合图像中目标显著性，并在语义分割和目标检测中带来一致的精度增益（mIoU和mAP提升）。
- 显式耦合范式比传统的“先增强后融合”串联方式更优越，信息融合与退化去除深度结合有利于互补信息保留。
- 设计组件（FCM、损失函数L_int、L_grad、扩散模型本身）均对最终性能有重要贡献。

### 7. 优点

- **方法创新**：首次将特征级融合显式嵌入扩散采样过程，解决了复合退化下的融合难题；引入文本交互实现个性化目标增强，贴近实际应用需求。
- **性能突出**：在多种融合场景和下游任务上一致超越众多基线，含增强预处理后的公平对比。
- **实验扎实**：多维度的消融实验、泛化测试、语义验证，论证充分。
- **开源可复现**：提供代码，详述实验配置。

### 8. 不足与局限

- **效率较低**：作者在论文中承认扩散模型采样慢导致推理效率低（未在正文强调，但在附录中提及），限制了实时应用。
- **计算需求不透明**：未报告训练时间和具体GPU使用时长，难以评估训练成本。
- **退化类型有限**：仅针对偏色、噪声、曝光不当三类退化，未涵盖模糊、遮挡等其他常见退化。
- **依赖零样本定位模型**：再调制效果受限于OWL-ViT和SAM的性能，复杂场景下目标定位可能不准确。
- **评估侧重图像质量**：虽然进行了下游任务实验，但仅在有限数据集上测试，未来应在更多实际应用（如自动驾驶、医疗诊断）中验证。

（完）
