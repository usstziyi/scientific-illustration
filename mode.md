下面给你一套可复用的 **“顶会论文风格结构图”提示词模板**，适合生成 CVPR / ICCV / NeurIPS / ICLR 常见的 **method overview / pipeline / architecture figure**。

我把它拆成 4 层：**通用母模板、风格关键词、版式控制词、不同任务专用模板**。你以后只要替换研究内容就能直接用。

---

# 1. 通用母模板

这是最核心的一版，适合大多数科研结构图生成。

```text
Create a publication-quality AI research architecture figure in the style of a top-tier conference paper (CVPR/ICCV/NeurIPS/ICLR). 
The figure should be a clean technical schematic / method overview diagram with a flat vector infographic style and subtle pseudo-3D layered blocks. 
Use a 16:9 layout, high resolution, clear hierarchy, and visually balanced composition.

Requirements:
- academic paper figure style
- model architecture / pipeline diagram
- clean vector shapes
- light blue / gray-blue / pale yellow / pale green scientific color palette
- subtle depth through layered feature maps and stacked modules
- dashed grouping boxes for subfigures or stages
- thin clean arrows showing data flow
- concise labels with publication-style typography
- minimal decoration, maximum clarity
- visually suitable for journal or conference publication
- white or very light gray background
- neat spacing, aligned modules, readable annotations
- no noisy textures, no photorealism, no poster style

Content:
[在这里填你的研究方法内容，用模块化语言描述]
```

---

# 2. 高质量风格关键词库

这些词你可以自由拼接。
核心思路是让模型知道：这不是“艺术插画”，而是“学术论文结构图”。

## 2.1 风格主标签

直接优先加入这些：

```text
publication-quality
conference-paper figure
journal-ready
academic infographic
technical schematic
method overview figure
pipeline diagram
model architecture diagram
research illustration
scientific visualization
```

## 2.2 视觉风格标签

这组最接近你给的参考图：

```text
flat vector style
clean scientific infographic
subtle pseudo-3D
layered feature map blocks
isometric-inspired module rendering
soft shadows
stacked tensors / stacked feature maps
minimalist academic layout
precise annotation
structured visual hierarchy
```

## 2.3 配色标签

参考图就是很典型的低饱和科研色：

```text
low-saturation scientific palette
light blue
gray-blue
pale yellow
pale green
soft orange accents
muted red for emphasis
consistent color coding across branches
```

## 2.4 排版标签

顶会风格很看重这个：

```text
balanced composition
modular arrangement
clear left-to-right information flow
subfigure separation
dashed panel borders
consistent spacing
aligned blocks
clean arrows and connectors
readable labels
high information density but uncluttered
```

## 2.5 负面约束词

这个很重要，防止跑偏成海报、UI、卡通：

```text
no photorealism
no anime
no hand-drawn sketch style
no decorative background
no glossy marketing poster
no unnecessary icons
no clutter
no excessive gradients
no 3D rendering realism
no comic style
```

---

# 3. 一套标准化提示词结构

以后你写提示词，建议按这个顺序：

## 模板结构

```text
[任务类型]
[目标风格]
[画面布局]
[视觉元素]
[文字与标注要求]
[你的研究内容]
[负面约束]
[输出规格]
```

## 套进去就是：

```text
Generate a publication-quality method overview figure.

Style:
Top-tier AI conference paper style (CVPR/ICCV/NeurIPS), clean technical schematic, flat vector infographic with subtle pseudo-3D layered blocks.

Layout:
16:9 horizontal layout, modular composition, left-to-right reading flow, grouped subpanels with dashed borders, balanced spacing and alignment.

Visual elements:
Feature maps, stacked tensors, module blocks, arrows, branching structures, fusion blocks, selection/filtering modules, decoder/refinement stages, color-coded pathways.

Labels:
Concise paper-style labels, readable typography, clear module names, subfigure labels like (a), (b), (c), no excessive text.

Content:
[填你的具体方法]

Constraints:
No photorealism, no poster aesthetic, no decorative icons, no clutter, no dark background.

Output:
2560x1440, journal-ready, scientifically accurate, visually clean and publication appropriate.
```

---

# 4. 可直接复用的英文母提示词

下面这版你几乎可以直接复制，然后只改内容。

```text
Create a high-quality publication-ready research figure for an AI paper. 
The figure should resemble a top-tier conference architecture diagram (CVPR / ICCV / NeurIPS / ICLR), with a clean technical schematic style, flat vector graphics, and subtle pseudo-3D layered feature-map rendering.

Design requirements:
- 16:9 horizontal layout
- resolution 2560x1440
- method overview / pipeline diagram style
- modular composition with clear visual hierarchy
- soft scientific color palette: light blue, gray-blue, pale yellow, pale green, muted orange, restrained red emphasis
- dashed grouping boxes for stages or subfigures
- precise arrows and connectors showing the information flow
- stacked feature maps, tensor blocks, proposal/query blocks, encoder-decoder style modules where appropriate
- minimal but elegant shadows for separation
- publication-style typography with concise labels
- visually clean, balanced, and easy to read
- white or light gray background
- suitable for journal and conference publication

Scientific content:
[Describe the method here in modular form:
input → backbone → feature extraction → query selection → refinement → prediction, etc.]

The figure must prioritize scientific clarity and architectural correctness.
Avoid poster-like aesthetics, photorealism, cartoon elements, UI mockup style, and unnecessary decoration.
```

---

# 5. 中文版母提示词

如果你平时更习惯中文，可用这个版本：

```text
请生成一张适用于顶级 AI 会议论文的科研结构图，风格参考 CVPR / ICCV / NeurIPS / ICLR 常见的 method overview figure / pipeline diagram / model architecture diagram。

风格要求：
- 扁平化矢量信息图风格
- 带轻微 pseudo-3D 层叠模块效果
- 画面简洁、专业、期刊可发表
- 使用低饱和科研配色：浅蓝、灰蓝、浅黄、浅绿，少量橙色或红色作为强调
- 白色或浅灰背景
- 模块排列整齐，层级清晰
- 使用虚线边框划分子模块或子图
- 使用细而清晰的箭头表示数据流
- 字体和标注简洁规范，符合论文插图习惯
- 重点突出科学准确性、可读性和版面平衡

版式要求：
- 横版 16:9
- 分辨率 2560x1440
- 从左到右的信息流
- 可以使用 (a)(b)(c) 形式划分子图
- 避免内容拥挤，保证标签清晰可读

科研内容：
[在这里填你的方法流程和模块说明]

负面要求：
- 不要海报风
- 不要写实 3D
- 不要卡通风
- 不要 UI 界面风
- 不要复杂背景纹理
- 不要多余装饰元素
```

---

# 6. 适合不同科研图类型的专用模板

## 6.1 方法总览图

最常用。

```text
Create a conference-paper style method overview figure for an AI model.
Show the full pipeline from input features, feature extraction, query generation, selection/filtering, refinement, and final prediction.
Use modular blocks, stacked feature maps, arrows, and grouped subpanels.
The style should be flat vector, publication-ready, and visually similar to a CVPR architecture figure.
Resolution 2560x1440, aspect ratio 16:9.
```

## 6.2 多分支网络结构图

适合 backbone + 多头分支 + fusion。

```text
Create a journal-quality architecture diagram for a multi-branch deep learning framework.
Visually separate the classification branch, regression branch, and fusion/refinement branch with clear color coding.
Use stacked feature-map blocks, branching arrows, fusion modules, and dashed boxes for grouped stages.
Maintain a clean top-tier conference figure style with flat vector graphics and subtle layered depth.
```

## 6.3 Encoder-Decoder / Transformer 结构图

适合 DETR / ViT / 多阶段解码。

```text
Create a publication-ready transformer architecture figure in top AI conference style.
Show encoder features, query embeddings, positional embeddings, decoder layers, and iterative refinement stages.
Use stacked tensors, embedding blocks, arrows, and repeated module layouts for decoder stages.
Keep the design minimal, scientific, and visually aligned with CVPR / ICCV method figures.
```

## 6.4 对比图 / Ablation 图

适合 baseline vs ours。

```text
Create a comparison figure for a research paper, showing baseline vs proposed method.
Use side-by-side panels with identical visual language and aligned modules.
Highlight the improvements of the proposed method using restrained red/orange emphasis and cleaner module flow.
Maintain a publication-quality technical schematic style.
```

## 6.5 时序 / iterative refinement 图

适合多阶段 refine。

```text
Create a scientific pipeline diagram for an iterative refinement framework.
Show multiple sequential refinement stages with repeated clean modules, arrows, and intermediate outputs.
Use a structured left-to-right flow and clear stage numbering.
The style should resemble a top-tier AI paper figure, with flat vector graphics and subtle pseudo-3D blocks.
```

---

# 7. 你这类图最适合的“内容写法”

生成结构图时，最关键不是写一大段论文摘要，而是把内容写成 **模块链条**。

不要这样写：

```text
This paper proposes a dynamic distinct query mechanism to improve...
```

而要这样写：

```text
Input feature pyramid → classification subnet and regression subnet → pyramid shuffle on selected layers → class-agnostic NMS as distinct query selection → retain distinct queries only → one-to-one assignment → loss computation
```

对于多子图，最好这样写：

```text
(a) DDQ FCN:
Dense queries from FCN pyramid → classification subnet and regression subnet → pyramid shuffle applied to the last two cls layers and last reg layer → objectness / classification / regression outputs → class-agnostic NMS as DQS → distinct queries retained → one-to-one assignment for training.

(b) DDQ R-CNN:
Last feature maps from DDQ FCN classification and regression branches → concatenate and fuse → distinct query filtering → send retained distinct queries and corresponding boxes to refine head ×2.

(c) DDQ DETR:
Encoder feature embeddings → DQS selects distinct queries → linear projection to content embeddings → corresponding boxes mapped to position embeddings → content and position embeddings enter decoder layer ×6 → DQS before each refinement stage to maintain distinctness.
```

这类写法最利于出图。

---

# 8. 一个“万能加强版”提示词

这版适合你以后直接套任何方法图。

```text
Create a publication-grade AI research architecture figure, visually aligned with top-tier conference papers such as CVPR, ICCV, NeurIPS, or ICLR.

Visual style:
clean technical schematic, flat vector infographic, subtle pseudo-3D stacked tensors and feature maps, low-saturation scientific colors, light blue / gray-blue / pale yellow / pale green palette, restrained orange/red highlights, white or light gray background.

Composition:
16:9 horizontal layout, balanced modular arrangement, left-to-right information flow, dashed boxes for grouped stages or subfigures, consistent spacing and alignment, concise labels, thin precise arrows, visually clean and uncluttered.

Scientific figure conventions:
architecture blocks, feature maps, proposal/query boxes, embedding modules, fusion nodes, filtering/selection stages, decoder/refinement modules, repeated stage structure where needed, subfigure labels (a)(b)(c), publication-style typography.

Content to illustrate:
[replace with your method pipeline in modular steps]

Quality target:
journal-ready, scientifically accurate, visually elegant, easy to read, suitable for direct inclusion in a research manuscript.

Do not use photorealism, poster aesthetics, dramatic lighting, cartoon icons, UI mockup design, noisy textures, or unnecessary visual decoration.
Output resolution: 2560x1440.
```

---

# 9. 给不同模型喂图时的“小技巧”

## 9.1 如果你有参考图

把这句加进去：

```text
Follow the visual language of the reference figure in color palette, panel arrangement, module rendering, spacing, and annotation style, while adapting the content to the new method.
```

## 9.2 如果你想更像“顶会论文”

加：

```text
prioritize scientific clarity over artistic expressiveness
```

## 9.3 如果你想更规整

加：

```text
strict alignment, consistent module sizing, grid-based layout
```

## 9.4 如果你怕字太多太乱

加：

```text
minimize text density, use short labels only
```

## 9.5 如果你想更像你给的 DDQ 图

加：

```text
use layered feature-map slabs, rounded module boxes, dashed blue panel borders, and muted red italic emphasis for key operations
```

---

# 10. 一个专门仿照你这张 DDQ 风格的模板

```text
Create a publication-quality AI method figure strongly inspired by a CVPR-style architecture diagram like the DDQ pipeline figure. 
Use a light gray background, blue dashed panel borders, layered blue feature-map slabs, rounded pale module boxes, muted red emphasis text, and thin gray arrows. 
The visual style should be a clean flat vector scientific infographic with subtle pseudo-3D depth.

Layout:
- 16:9 horizontal figure
- split into 3 subfigures labeled (a), (b), (c)
- each panel contains a compact pipeline with aligned modules and arrows
- strong visual consistency across panels
- readable labels and restrained scientific color palette

Content:
[replace with your own three-part method]

The figure should look like a top-tier computer vision paper architecture illustration, suitable for direct insertion into a manuscript.
Resolution 2560x1440.
```

---

# 11. 最后给你一个实际使用公式

你以后可以直接按这个公式写：

```text
请生成一张【图类型】，
风格参考【参考图 / 顶会风格】，
版式为【16:9 / 横向 / 分栏】，
视觉元素包含【feature map / 模块框 / 箭头 / embedding / decoder 等】，
科研内容为【模块流程】，
要求【科研配色 / 清晰标注 / 期刊级 / 2K】，
避免【海报风 / 写实 / 卡通 / 杂乱】。
```

例如：

```text
请生成一张顶会论文风格的方法总览图，风格参考 CVPR 架构图与 DDQ pipeline 的排版和配色，16:9 横版，使用 layered feature maps、模块框、箭头、虚线分组框和 embedding/proposal block，内容为：输入图像特征 → 双分支特征提取 → 动态查询选择 → 多阶段细化 → 最终预测。要求低饱和科研配色、标注简洁、结构清晰、适合期刊发表，分辨率 2560x1440。避免海报风、写实 3D、卡通化和背景装饰。
```

如果你愿意，我下一步可以直接帮你整理成：
**“可直接复制的中英双语提示词清单”**，或者进一步做成 **适配 ChatGPT / Midjourney / Stable Diffusion / Flux 的不同版本**。


# 12. 最后一个版本

```text
Create a high-quality publication-ready research figure for an AI paper.

Style:
- top-tier conference architecture diagram (CVPR / ICCV / NeurIPS / ICLR)
- clean technical schematic style
- flat vector graphics with subtle pseudo-3D layered feature-map rendering
- white or very light gray background
- publication-style typography with concise labels
- scientifically precise, visually balanced, and easy to read
- avoid poster aesthetics, photorealism, cartoon style, UI mockup style, and decorative clutter

Canvas:
- 16:9 horizontal layout
- 2560x1440 resolution

Layout constraints:
- center the entire multi-panel figure within the canvas
- place all content inside a strict safe area
- keep at least 8–10% blank margin on the left and right, with generous top and bottom margins
- no panel, label, arrow, dashed box, or caption may touch or cross the canvas boundary
- the leftmost panel must be fully inset from the left border
- all subfigures must be fully visible
- use a compact, evenly spaced horizontal composition
- avoid oversized image panels
- keep the first and last panels slightly smaller to prevent edge cropping

Design requirements:
- method overview / pipeline diagram style
- modular composition with clear visual hierarchy
- soft scientific color palette: light blue, gray-blue, pale yellow, pale green, muted orange, restrained red emphasis
- dashed grouping boxes for stages or subfigures
- precise arrows and connectors showing information flow
- stacked feature maps, tensor blocks, proposal/query blocks, encoder-decoder style modules where appropriate
- minimal elegant shadows for separation

Scientific content:
The framework of UnSniffer contains a feature extractor, a known object detector, and a generalized object detector.
(a) a compact input RGB image panel
(b) several channels of deep features encoding known and unknown objects simultaneously, with red circles marking object positions
(c) GOC score distributions before and after training the GOC
(d) negative energy distributions before and after using negative energy suppression
(e) final detection results

Important:
- prioritize scientific clarity and architectural correctness
- ensure panel (a) and its caption are completely visible
- ensure every panel label, caption, and connector is fully inside the canvas
- leave wide white margins on all four sides
```