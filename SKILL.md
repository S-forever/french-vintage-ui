---
name: french-vintage-ui
description: >
  法式复古小清新UI设计规范。当用户请求生成前端页面、组件或界面设计时，
  自动应用本规范。适用于App和Web端的UI设计，核心调性为"手作感+低饱和自然色系+
  手写体排版+生活化装饰元素"。
  NOT for: 企业级后台管理系统、数据大屏、金融交易界面、游戏UI。
---

# French Vintage UI Design System

## 风格定位（2026-08-28 重写 · 基于 5 张用户参考图拆解 · 去掉旧版"喜茶拙趣/小学生作业本"定位）

> 本 Skill 核心 = **法式乡村小清新（French Pastoral Cottagecore）**。所有视觉必须同时踩中「法式浪漫（法语、缎带、蕾丝、蝴蝶结、樱桃郁金香玫瑰、面包蛋糕甜点、酒与高脚杯）+ 复古杂货贴纸（格纹、波浪花边、彩色蜡笔/水粉填充、做旧纸张颗粒）+ 墨水线条邀请卡（米黄纸、深蓝墨水、手写字体、手绘相框式边框）」三根主轴。

- **核心标签（主轴 8 个）**：墨水线条、彩色贴纸、缎带蝴蝶结、蕾丝波浪、Vichy 小格、法语手写、田园杂货、做旧纸张
- **情绪关键词（12 个）**：柔软、乡村、野餐、奶甜、不费力的精致、复古手账、烘焙午后、花园散步、生日邀请、慢生活、少女心、温柔但不幼稚
- **参考调性（5 个真实参照物，不再虚构）**：
  1. 参考图 1 · 墨水线条邀请卡（Courtney Turns 30 生日沙滩邀请）
  2. 参考图 2 · 杂货贴纸 Tag（Féprdi / L'Dorée / Nana Bakery 椭圆徽章）
  3. 参考图 3 · 复古名牌框（12 款法式丝带/挂孔标签名牌）
  4. 参考图 4 · 乡村水粉贴纸（毛衣、格纹心、可颂熊、樱桃蛋糕、果酱罐、线球猫）
  5. 参考图 5 · 咖啡主视觉海报（The Saturday Perspective · MOMENT 大杯）

### 主风格：双主并行（生成任何页面前先判断本次更偏向哪个）

- **主风格 A · 墨水线条邀请卡风（来自图 1、图 5）**：米黄/米白纸底 + 单一深蓝墨水手写线条 + 衬线/打字机正文 + 手绘相框式闭合边框 + 分割线=不闭合手绘横线。用于 **整页背景、大段文案页、海报、博客封面、邀请函、栏目页**。
- **主风格 B · 杂货标签贴纸风（来自图 2、图 3、图 4）**：彩色低饱和蜡笔/水粉填色 + 8 种典型边框（椭圆徽章/丝带标签/挂孔吊牌/波浪边）+ 7 种底纹（Vichy 格/条纹/网纹/波点/竖条布纹/菱格/蕾丝）+ 缎带蝴蝶结/樱桃/小花贴角。用于 **按钮、Badge、空状态插图、Banner、分类 Tag、章节标题外框、独立装饰画**。

### 组合比例
- 主 A + 主 B 必须同页并存：A 占 60%（纸面底+大段文字区），B 占 40%（贴纸/标签/小装饰画）
- 禁止只出单色墨水页（太素不像法式）；禁止只出贴纸彩色页（太挤不像复古邀请）

## When to Use
当用户请求生成以下类型页面时，自动应用本UI规范：
- 工具类app或web
- 生活方式类展示页
- 轻社交平台（分享生活片段、手账内容）
- 个人博客/日记工具
- 任何需要"温柔治愈""手作感""复古文艺"氛围的界面

## ⚠️ 交互确认流程（必须在生成代码前执行）

在生成任何UI代码之前，必须先暂停并向用户确认主色选择，具体流程如下：

1. **暂停生成**：不要直接输出代码，先向用户展示以下主色选项卡片：

   > 请选择本次页面的主色调：
   >
   > 🅰️ **奶油白** `#F8F5F0` — 温暖柔和，适合阅读、日记类页面
   >
   > 🅱️ **浅灰蓝** `#D0E1E6` — 清冷安静，适合工具类、信息展示类页面
   >
   > 🅲️ **淡芥末黄** `#F6F1C7` — 明亮温馨，适合生活方式、社交类页面
   >
   > 回复 A / B / C 即可，也可以直接告诉我你想要的色值。

2. **等待用户回复**：用户选择后，将该色值作为本次页面的主背景色，其余辅色、强调色按规范自动匹配。

3. **确认后再开始生成代码**。

> 如果用户在对话中已经明确指定了颜色（如"用蓝色调"），则跳过确认步骤，直接使用用户指定的颜色。

### ⚠️ 主色联动规则（2026-08-28 定稿 · 解决贴纸淡/融背景问题）

**杂货标签贴纸风（椭圆徽章/丝带徽章/挂孔吊牌/波浪花边/邮票齿孔/蕾丝圆章）的 fill 底色、底纹透明度、描边粗细，必须跟随主色 A/B/C 切换，禁止一张表吃遍三种主色：**

| 项目 | A · 奶油白底 `#F8F5F0` | B · 浅灰蓝底 `#D0E1E6` / `#D6E4EC` | C · 淡芥末黄底 `#F6F1C7` |
|---|---|---|---|
| **贴纸 fill 底色**（8 种标签全部） | 米白浅纸 `#F5F0E8` · 奶黄纸 `#F6EFD6` · 奶油白 `#F8F5F0`（任选其一） | ✅ **米白浅纸 + 5% 牛奶白偏色 = `#F7F4EF`**（比奶油白再亮一档，拉开和灰蓝背景的亮度差 ≥ 15）；禁止再用米黄纸 `#F6EFD6`（太暖、太接近灰蓝底） | 奶油白 `#F8F5F0` · 米白浅纸 `#F5F0E8`（冷暖对比足够，无需偏色） |
| **SVG `<pattern>` 透明度**（7 种底纹全部） | `0.18–0.35` | ✅ **`0.35–0.50`**（灰蓝底灰雾重，Vichy/条纹/波点必须加深一档才显纸纹感，否则图案融成灰块） | `0.25–0.40` |
| **描边 stroke-width**（所有边框/缝线/齿孔） | `1.6–2.0px` | ✅ **`1.8–2.4px`**（灰蓝底对比度低，粗 0.2-0.4px 让标签轮廓立起来；墨蓝描边从 1.8→2.0 起，牛皮棕从 2.0→2.2 起） | `1.6–2.2px` |
| **噪点层 feFuncA slope**（所有带 fill 的独立 SVG） | `0.12–0.15` | ✅ **`0.16–0.20`**（灰蓝底噪点几乎不可见，slope 加 0.04 才出做旧纸颗粒感） | `0.13–0.17` |

**快速检查口诀（选 B 底时逐条过）**：
1. ✋ 贴纸 fill = `#F7F4EF` 了没？（默认奶油白/米黄纸 → 打回）
2. ✋ pattern opacity ≥ 0.35 了没？（< 0.30 → 打回）
3. ✋ stroke ≥ 1.8px 了没？（1.6px 以下 → 打回）
4. ✋ feFuncA slope ≥ 0.16 了没？（0.12 → 打回）

## 色彩体系（Design Tokens）

### 主色（背景/大面积 · 2026-08-28 基于 5 张参考图校准）
- **奶黄纸** `#F6EFD6`：参考图 1 邀请卡纸本色，整页底色首选
- **奶油白** `#F8F5F0`：参考图 2/3 贴纸页米色，卡片/次级区块底
- **米白浅纸** `#F5F0E8`：参考图 5 咖啡海报纸色，留白/空白区
- **浅灰蓝** `#D6E4EC`：参考图 2/3 部分标签蓝色外框，冷区块背景
- **淡芥末黄** `#F6F1C7`：参考图 4 蛋糕身体/奶油黄，暖区块强调

### 墨水蓝系（所有"线条"默认用这个；参考图 1/5 的蓝色墨水）
- **手写墨水蓝** `#3B56A6`：邀请卡蓝色描边/手绘正文首选（旧 `#445D9F` 升级 → 更接近图 1 的印刷蓝）
- **深打字机蓝** `#2F4B8F`：标题字、主强调线
- **粉蓝（贴纸外框）** `#A9CBE3`：参考图 2/3 蓝标签外框，不用于文字

### 田园色板（参考图 4 水粉贴纸 + 图 2/3 彩色标签）
- **陶土红/砖红** `#C25A4A`：缎带蝴蝶结、心形、樱桃、邮票齿孔
- **奶油粉** `#F4B9C1`：图 4 粉色蛋糕身体
- **淡紫薰衣草** `#C5B9D9`：花边框、小装饰
- **橄榄花园绿** `#6C8A5C`（从旧 `#6C8A5C` 调亮 → 更贴合图 4 树叶/猫眼绿）：植物叶、绿缎带、绿格子
- **薄荷绿** `#A8D8C8`：糖霜/浅绿填充
- **鹅黄浅** `#F1D37D`：奶油黄、小黄花、标签底
- **牛皮棕** `#9B7555`（旧深褐改亮 → 更贴合图 4 可颂/果酱罐棕）：可颂、小熊毛皮、果酱罐

### 强调色（≤ 2 笔的小撞色用）
- **草莓红** `#D9556B`：樱桃、爱心、蝴蝶结上的点
- **深樱桃紫** `#8A3A54`：水果/嘴唇/印章用

### 色彩规则
- 所有颜色必须带"灰度"或"做旧感"
- 禁止使用纯黑（`#000000`）、纯白（`#FFFFFF`）、高饱和荧光色
- **所有装饰画线条默认墨水蓝 `#3B56A6`，文字色默认深打字机蓝 `#2F4B8F`**；牛皮棕/橄榄绿仅在对应语义元素（面包、叶子）上使用
- 单张贴纸/标签内的颜色数量 ≤ 4（含描边色）

## 字体与排版

### 中文字体（⚠️ 2026-08-28 定稿：正文改用打字机体）
- **大标题/重点文字**（4xl+、徽章主标题）：**汇文明朝体GBK**（旧铅字印刷感）→ 朝华打字机 → 迫真打字油印体 → serif
- **打字机风格展示文字**（展示插画下的小字副标题：果酱罐"好好吃"、蛋糕"今天也要好好吃饭"、白猫"今天先躺着"、心情卡片正文）：**朝华打字机** → 迫真打字油印体 → serif
- **正文/说明文字**（段落长文、标签副标题、body 默认）：**朝华打字机** → 迫真打字油印体 → serif（不再优先思源宋体；思源宋体仅作为系统无打字机体时的 fallback）
- **Tailwind fontFamily 标准映射**：
  ```js
  'handwritten-cn':  ['"汇文明朝体GBK"', '"朝华打字机"', '"迫真打字油印体"', 'serif'],
  'typewriter-cn':   ['"朝华打字机"', '"迫真打字油印体"', 'serif'],
  'body-cn':         ['"朝华打字机"', '"迫真打字油印体"', 'serif'],
  ```
- 字体文件放 `fonts/` 目录，HTML `<head>` 用 `@font-face` 声明，`body {}` 全局 font-family 首位也指向朝华打字机；**SVG `<text>` 内联 font-family 禁止硬编码 Noto Serif SC**，必须用上述三条链之一
- 所有 3 款中文字体（汇文明朝体GBK、朝华打字机、迫真打字油印体）均为免费商用，作者特里王，需下载 `.ttf` 到 `fonts/` 目录后 `@font-face` 声明生效

### 英文字体
- 标题/手写部分：Caveat、Dancing Script、Great Vibes
- 正文/标签：Lora、Merriweather、Playfair Display

### 排版规则
- 行距：正文行距 ≥ 1.6倍字号，营造呼吸感
- 字间距：标题字间距略宽（+0.05em），正文紧凑（0em）
- 对齐方式：左对齐为主，避免居中排版（除非是封面或引言）
- 段落间距：段前段后留白 ≥ 1.5倍行距

## 组件语言

### 按钮
- 形状：圆角矩形（圆角 8px–12px），避免直角或全圆角
- 样式：描边按钮为主（深蓝描边 + 透明背景），填充按钮仅用于主操作
- 悬停：颜色加深10% + 轻微上浮 translateY(-2px)
- 文字：手写体或衬线体

### 卡片/区块
- 背景：米白或浅灰蓝，带轻微纸张纹理
- 边框：1px 深蓝细线描边，或细线虚线
- 内边距：≥ 24px，留白充足
- 阴影：无或极淡（box-shadow: 0 1px 3px rgba(42,75,124,0.08)）

### 表单输入框
- 边框：1px 深蓝细线，圆角 6px，或极细下划线
- 聚焦态：边框变粗至 2px + 淡紫色光晕（box-shadow: 0 0 0 2px rgba(197,185,217,0.4)）
- 占位符：浅灰色 #A0A0A0，手写体

### 导航
- Tab栏：无背景色，文字+下划线（深蓝），选中态加粗或变色
- 侧边栏：窄边栏（≤ 240px），米白背景，手绘风格图标

## 装饰元素（法式乡村小清新 · 主 A 墨水邀请卡 + 主 B 杂货标签贴纸 · 2026-08-28 大重写）

> 5 张用户参考图提炼出的装饰体系 = **一张"法语文具纸"（纸面底色/纸张颗粒/墨水笔手写）** + **贴在纸上的"法式杂货贴纸"（蝴蝶结/缎带/Vichy 格/蕾丝边）**。
> 绝对不再使用「喜茶拙趣 / 头大身小 / 不闭合抖动 / ✦ X 交叉 / 💧 水滴」这类 2026-08-28 之前的旧视觉。

### ⚠️ 装饰画强制三层（反面清单：禁止"纯黑+无填色裸白描"）

> 2026-08-28 用户踩坑记录：SVG 装饰画如果全部用 `#1A1A1A` 纯黑线条 + `fill="none"` 白描，会直接跑到「小学生作业本/黑白涂鸦」语感，**和法式复古完全不搭**。必须强制以下三层，否则生成结果直接不合格。

1. **线条层（禁纯黑）**：装饰画的描边色默认用**墨水蓝 `#3B56A6`**；牛皮棕 `#9B7555`（面包/果酱）、橄榄绿 `#6C8A5C`（植物）、陶土红 `#C25A4A`（缎带/樱桃）仅用于对应语义元素。**绝对禁止 `#000 / #111 / #1A1A1A / #222` 这类纯黑近黑**。
2. **填色层（必须有 fill，不能全部 none）**：任何闭合图形（杯、蛋糕、标签、花朵、动物身体）必须填低饱和色。优先填色顺序：奶黄 `#F6EFD6` → 奶油白 `#F8F5F0` → 芥末黄 `#F6F1C7` → 薄荷绿 `#A8D8C8` → 粉蓝 `#D6E4EC` → 奶油粉 `#F4B9C1` → 淡紫 `#C5B9D9`。
3. **噪点纹理层（SVG `<filter>` 层）**：装饰画 SVG 内部必须带一层 `<feTurbulence>` 噪点滤镜（模拟**做旧打印颗粒 / 水彩纸 / 蜡笔颗粒**），推荐参数：`type="fractalNoise" baseFrequency="0.8–1.2" numOctaves="2"` → `feColorMatrix`（变同色/墨蓝灰 + α=0.10–0.16）→ `feBlend multiply`。

> 唯一例外：「散点符号（省略号 / 下划线 / 手绘横向分割线）」允许 `fill="none"` 单色，因为它们是线稿点缀，不算独立装饰画。

### 双主风格装饰语言（必须同时使用）

#### 主 A · 墨水线条邀请卡风（来自图 1、图 5）
用于**整页、栏目、海报封面**的基础层：
- **纸底**：必选 `#F6EFD6` 奶黄纸（图1）或 `#F5F0E8` 米白浅纸（图5），整页 background。
- **相框式外框**：手绘闭合矩形，四角微凹/微凸/不对称（图1 四个角的蓝色相框），`stroke="#3B56A6"` 宽度 2.0–2.8，四边不平行，左右边距 20–40px。**端点必须贴到 viewBox 边缘**（M0/M960/M1600 而非 M24/M936/M1580），否则相框四条边会被裁切（踩坑记录 2026-08-28）。
- **三级排版（图1/5 强制参考）**：
  1. 超大手写标题（COURTNEY TURNS 30 / MOMENT）：Caveat / Great Vibes，字号≈页面宽度 1/8，墨水蓝 `#3B56A6`，**字间距不规则**，字母宽度手写感，轻微旋转。
  2. 居中正文（LETS JUST SPEND A DAY / 正文说明）：打字机体（Lora/Courier Prime/朝华打字机）或衬线（Playfair Display/思源宋体），深打字机蓝 `#2F4B8F`，行距 1.7，垂直居中。
  3. 角落小信息（YOU ARE INVITED / JUNE 25 / GULF SHORES / The Saturday Perspective）：和正文同字体但更小，左对齐或右对齐，与装饰画相邻摆放。
- **分割线 = 不闭合手绘横线**：两端出头，中间有 1-2 处上下波动（图1 "LETS" 与 "YOU ARE INVITED" 之间的手绘分割线），**绝不允许 CSS `hr` 完美水平线**。
- **墨水蓝色插画（图1 右下）**：酒杯、酒瓶、高脚杯、花瓶+花束——**单墨水蓝线条 + fill=none**（只允许这里裸白描，因为它们是"邀请卡同墨水笔画的插画"），线条宽度统一 1.8–2.2。

#### 主 B · 杂货标签贴纸风（来自图 2、图 3、图 4）
用于 **Tag / 章节标题 / 空状态 / 按钮 / 独立装饰画**：
- **8 种典型边框（一张页面内出现 2-3 种，必须覆盖标签和徽章）**：
  1. **椭圆徽章**：内外双椭圆，外圈扇贝波浪边（scalloped），内部留白放法语花体字 → 图 2 前 4 个
  2. **丝带徽章**：椭圆两侧贴红/粉格纹缎带（ribbon），缎带尾部有斜切角 → 图 2 右上 "Be kind to your Mind"
  3. **挂孔吊牌**：圆角矩形 + 顶部圆孔 + 左右两个半圆挂孔（handle），中间区域 45° 斜纹底 → 图 2 左下 "L' Dorée"
  4. **波浪椭圆花边**：椭圆外波浪 + 花/叶/樱桃贴角 → 图 2 左中 / 右下
  5. **格纹底名牌**：矩形或上拱下平形，背景 Vichy 格，顶部一个蝴蝶结 → 图 3 第 3/4 行
  6. **邮票齿孔**：矩形四周等距半圆缺口（perforation）→ 图 4 "Nouveau départ" 名牌
  7. **波浪波浪横条**：横向椭圆，上波下波交替，上下不同弧，内部竖条纹底 → 图 2 右中 "Hair Riot"
  8. **蕾丝边圆章**：正圆/椭圆外双层扇贝 + 缎带蝴蝶结在右上 → 图 3 第 1 行
- **7 种底纹 pattern（必须用 SVG `<pattern>` 实现，透明度 0.18–0.35，叠在纯色填色之上）**：
  1. **Vichy 小格**（红白 `#C25A4A`/米黄 或 蓝白 `#3B56A6`/奶油白）：8–10px 格，三层叠
  2. **条纹布**（stripe）：竖直 3px+间隔 5px，蓝白/粉白/红黄
  3. **波点**（dot）：小圆 1.5–2px，等距 6–8px
  4. **菱格**（diamond / gingham diamond）：斜 45° 小菱形
  5. **蕾丝波浪**：沿边框一圈 scallop（半圆），内部填充 2 条小圆点虚线
  6. **网格布纹**（grid waffle）：纵横 1px 细线
  7. **渐变水花**（watercolor）：径向渐变 + 噪点模拟水彩晕染
- **贴角装饰（⚠️ 2026-08-28 定稿：克制原则）**：
  - **数量**：每个徽章/标签**最多保留 1 个**贴角装饰（右下小花 / 左下爱心 / 右上樱桃 / 左上蝴蝶结），禁止四角全铺满；空角比塞满更显法式轻盈
  - **位置**：优先留 **右下** 或 **左下**，避开主标题文字区域
  - **类型**（挑 1 种即可）：
    - **缎带蝴蝶结**（ribbon bow）：左右两片 + 中间小圆，必用陶土红或橄榄绿
    - **小樱桃**（cherry pair）：两圆红果 + 绿梗 + 一片小叶子
    - **小花**（4 瓣/5 瓣）：花瓣粉、花心黄、1 条绿梗 + 叶
    - **心形**（爱心）：陶土红 + 白色 Vichy 小格纹填充

### 典型装饰画元素库（按出现频次，≥ 15 个，来自 5 张图）
按"生成某个场景时优先挑哪几个"排序：
1. **缎带蝴蝶结 / 彩色丝带**（出现频次最高，图 2/3 每个标签都有）
2. **樱桃 pair / 草莓（带籽）/ 树莓**（图 2 "L' Dorée" + 图 4 蛋糕顶 7 颗樱桃）
3. **小花束（花瓶/高脚杯里的郁金香+小花）**（图 1 右下）
4. **葡萄酒瓶 + 2 只高脚杯**（图 1 右下，生日/聚会/餐饮）
5. **可颂 / 法棍 / 面包棍**（图 4 右上熊抱法棍 + 中间可颂）
6. **奶油蛋糕（圆/三角 + 7 颗红樱桃 + 奶油花 + 法语）**（图 4 左中 "Amitié"）
7. **果酱罐 / 蜂蜜罐（Vichy 红白格盖子 + 手写标签布盖+麦穗/饼干）**（图 4 下中 "Bon Maman"）
8. **茶杯+茶碟（大纯色填色+细描边，图 5 咖啡杯巨型）**
9. **毛衣（费尔岛提花 + 爱心/鸭子/草莓/格纹 + 袖肘补丁，图 4 左上）**
10. **小熊 / 白色猫 / 黑色猫（真实比例+围裙/蝴蝶结/玩线球，图 4 右下两只猫）**
11. **旋转木马（带礼物盒/小熊/圣诞树小挂饰）**（图 4 左下）
12. **苹果盘（2 个半个苹果+叉子+蓝白格布，图 4 右中）**
13. **贴纸式名牌（邮票齿孔/蕾丝边/缎带挂孔，图 2 全部）**
14. **法语手写缎带条（Bon appétit / Nouveau départ / Petites choses）**（图 4 中部横条）
15. **小旗子（挂孔吊牌两侧半圆挂耳）、邮票边、麦穗、郁金香、洋甘菊**

> 装饰画造型法则= **圆润 + 真实比例 + 明显描边 + 厚实填色 + 水彩噪点**。**不再使用"头大身小/火柴人/不闭合断笔/抖动草稿线"**（这些是拙趣风，法风不做）。

### 大色块水粉贴纸风（辅助风格 B-1，来自图 4 · 用于大色块插图、Banner、空状态）

> **反面清单**：这里绝对禁止「头大身小 / 不闭合断笔 / 抖动草稿线」—— 这些是拙趣风，法风插画一律**真实比例 + 明显描边 + 厚实填色 + 水彩噪点**。

- **线条**：墨水蓝 `#3B56A6` / 牛皮棕 `#9B7555` / 橄榄花园绿 `#6C8A5C` / 陶土红 `#C25A4A`（按语义：蓝色=物品轮廓、棕=面包果酱/标签文字、绿=植物、红=缎带樱桃），粗线 1.8–2.4px，**完全闭合、硬拐点、无断笔无抖动**，端点 round
- **色彩填充**：
  - 奶黄 `#FDF3DC`、奶油粉 `#F4B9C1`、米白浅纸 `#F5F0E8`、粉蓝 `#D6E4EC`、薄荷绿 `#A8D8C8`、淡紫 `#C5B9D9`、牛皮棕 `#9B7555`
  - 填充必须叠 `<feTurbulence>` 噪点（`baseFrequency="0.8–1.1"` + `α=0.10–0.16` + multiply），模拟水彩晕染/蜡笔颗粒
  - 高频使用**红白 Vichy 格**（果酱罐盖/缎带心/名牌底）或**蓝白格**作为填充底纹
- **造型法则**：圆润 + 真实比例（面包是正常面包、猫是正常猫、毛衣是正常毛衣，不允许给静物长"两点眼+弧线嘴"—— 只给猫/熊/玩具这种活物留极简表情）
- **典型高频元素（按图 4 出现顺序）**：
  1. 费尔岛提花毛衣（爱心+鸭子+草莓+格纹+袖肘补丁）
  2. Vichy 格心形（陶土红扇贝边 + 红白格 fill）
  3. Bon Maman 果酱罐（红白格盖 + 手写布标签 + 麦穗/饼干）
  4. 小熊抱法棍（棕色毛 + 浅蓝色围裙）
  5. 圆顶奶油蛋糕 + 7 颗红樱桃顶 + 侧面法语手写
  6. 粉色心形蛋糕 + "Je t'aime" + 三角切片 + 小叉子
  7. 旋转木马（白马 + 礼物盒/小熊/圣诞树小挂饰）
  8. 苹果/梨子盘（2 个半个 + 金属叉 + 蓝白格餐布）
  9. 白猫玩蓝白毛线球（真实比例，非蛋形）
  10. 黑猫带头巾 + 蝴蝶结领（真实比例）
- **手写法语缎带条**：搭配手写体法语短语（*Nouveau départ* / *petites choses* / *Bon appétit* / *Amitié* / *Je t'aime*），邮票齿孔/蕾丝扇贝/缎带蝴蝶结外框包裹。⚠️ **缎带长度原则（2026-08-28 定稿）**：缎带主体 path 只比两端的装饰符号（♡、·、小花等）各超出 **~5px**，不要全程铺满整个 viewBox — 短缎带比长缎带更轻盈精致

### 墨水线条点缀风（辅助风格 A-1，来自图 1/5 · 用于分割线、边框、批注、Loading）

> 仅**分割线 / 相框式外框 / 同墨水色的插画群**允许 `fill="none"` 单色白描；其它场景必须填色+噪点。

- **笔触**：墨水蓝 `#3B56A6`，统一宽度 1.6–2.2px，完全闭合，**允许手绘不规整（轻微波动、两端出头）** 但不允许不闭合断笔
- **相框式外框（必出=参考图 1 四边框）**：4 条手绘矩形边，四角微凹/微凸/不对称，`stroke="#3B56A6"` 宽度 2.0–2.8，四边不平行；整页/单卡片均可用
- **手绘不闭合横线（分割线）**：一条 180–360px 宽的手绘横线，两端出头 6–10px，中间有 1–2 处上下波动（±3px），**绝不允许 CSS `hr` 完美水平线**
- **同墨水色插画群（图 1 右下高脚杯+酒瓶+花）**：多物体组合，全部 `stroke="#3B56A6"` + `fill="none"`，宽度统一 1.8–2.2，适合正文角落插图
- **手写体标注**：
  - 卡片/海报角落搭配中法英手写短语（"Tea time / 下午茶"、"Petites choses / 小事"、"Bon appétit ♡"、"Nouveau départ / 新的开始"）
  - 字迹倾斜（-3°~+3°）+ 轻微旋转，字体：Caveat / Great Vibes / Playfair Display Italic
  - 严禁"碎碎念自言自语"（拙趣风），法风是**法语短句 / 栏目小标 / 日期署名**
- **多方向排版（图 5 海报）**：允许竖排 + 横排 + 巨型花体字组合，左侧竖排正文（rotate(-90°) 或 writing-mode: vertical-rl）、右上角小字竖框、中部巨型 MOMENT 式花体标题

### 排版与布局原则

- 装饰元素散落在页面边角、卡片间隙、标题旁，不沿网格对齐
- 每个区块最多1–2个装饰元素，大面积留白
- 贴纸/插图可轻微旋转（-5°~5°），模拟"随手贴上去"的松弛感
- 整体遵循"少即是多"：有呼吸感、不乱、不挤

### 标签装饰（复古手绘标签风）

标签用于承载标题、日期、页码等短文字内容，是页面的核心装饰元素之一。所有标签必须具备"手工贴纸/印章"的物理质感，严禁使用规则的几何矩形或纯CSS圆角边框。

- **出现频次（强约束）**：同一页面（一屏可见或一页文档）内的标签装饰（云朵标签 / 花边标签 / 带耳标签 / 徽章形等）总数必须控制在 **1~3 个**
  - 最小 1 个（必要时如只有主标题，可以只有 1 个大标签）
  - 最多 3 个（例如：标题大标签 + 日期花边小标签 + 1 个分类带耳标签）
  - 超过 3 个后，必须改用其他形式（纯手写体文字、极简单线 Tag、非标签式圆角文字）
  - Tag 区内多个带耳标签（一行排列的分类小标签）可**按 1 组计为 1 次**，不必按单个数

#### 标签轮廓（形状）

- **禁止完美几何形**：轮廓必须带有手绘不规则感——轻微的波浪、凹凸、不对称弧线
- **推荐轮廓类型**：
  - 云朵形：多弧段拼接的不规则椭圆
  - 花边形/蕾丝边：连续的半圆小波浪（scalloped edge）
  - 波浪形：上下弧线 + 左右微凸
  - 带耳标签：左右两侧有延伸的"耳朵"或蝴蝶结
  - 徽章形：椭圆 + 顶部/底部的小三角形凸起
- **边框线条**：手绘感粗线（牛皮棕/橄榄花园绿/陶土红），粗细不均，局部可断续

##### 手绘不规则感的实现要点（必须遵循）

- **花边半径不均匀**：花边形标签的每朵小圆/扇贝半径在 9~13 之间随机取，不允许全部 r=10；位置也做轻微上下偏移（±1~3px）
- **双耳不对称**：带耳标签左右耳的形状、大小、弯曲必须不同（左瘦右胖、左尖右扁、或右耳带 Q 曲线左耳走直线）
- **外轮廓凹凸化**：外框不要用 `L16 10 L124 10 Q130 10 130 16` 这种等距等宽矩形，顶边/底边拆成多段 Q 曲线，中间段做 ±2~3px 上下起伏
- **内层书写区波浪化**：内衬条不做完美圆角矩形，边沿用多段 Q 曲线连接，每段控制点轻微上下偏移
- **局部笔压加粗**：在主描边下再叠一条更粗（stroke-width=2.6~3）、更短（10~30px）的局部笔触，模拟手画时停顿压笔
- **局部断线**：在主描边的一角（右上/左下）画 5~7px 同底色的矩形，把主描边"擦断"一小段，模拟手绘没画到底
- **草稿辅助线**：在轮廓外层加一条 `translate(1,-1)` 或 `translate(-1,1)` 的轻微虚线（`stroke-dasharray="2 3"` / `"3 2 1 2"`），做不透明 0.15~0.22，模拟草稿纸痕迹
- **缝线不均匀**：`stroke-dasharray` 禁止使用 `"2 2"` 等距针脚，改用 `"3 1 2 2 1 3"` / `"1 3 3 1 2 2"` / `"2 3 1 3 2"` / `"3 2 1 2 3 1"` 等随机组合，上下两条缝线 dash 规则要不同
- **每个标签要有 1 组独有的角落小装饰**：花 / 樱桃 / 蝴蝶结 / 心形 / 小叶子 / 小星星 散落边角，3 个同页面的标签装饰不能重复
- **3 个以上同页面标签**：标签1、标签2、标签3 的外轮廓 shape 不能相同（一个上拱下凸、一个顶部缺口、一个左右凹凸），装饰位置也不能雷同

#### 标签边框装饰

- **双层边框**：外轮廓 + 内侧细线（模仿邮票/印章的双线结构）
- **虚线/缝线效果**：用点状虚线模拟缝纫针脚
- **小点缀沿边分布**：
  - 小花朵、小叶片、小樱桃沿边框排列
  - 小星星、小圆点（波点）散落边框内侧
  - 心形、蝴蝶结点缀在角落
- **格纹/条纹填充背景**：标签内部可使用红白格、蓝白格、细条纹、波点作为底纹

#### 标签配色

- 使用低饱和的粉糯色系，单张标签内不超过3种颜色：
  - 粉蓝 `#B8D4E3`、粉粉 `#E8A0A0`、米黄 `#F5EDD8`、薄荷绿 `#C5D8C5`、淡紫 `#D5C5DB`
- 边框颜色比填充色深1-2度，模拟印刷墨色

#### 标签内文字

- 文字使用花体/手写体（英文可用 Caveat / Playfair Display Italic，中文可用汉仪尚巍手书）
- 文字可轻微倾斜，不严格居中，模拟手写排版
- 可搭配法语/英语短句（如 *L' Dorée* / *Nouveau départ* / *Be kind to your mind*）

#### 标签顶部装饰物

- 标签上方或角落可附加：
  - 蝴蝶结（红色/绿色/棕色丝带）
  - 小熊头像、小樱桃、小花朵
  - 丝带飘带效果

#### 标签的使用场景

- **页面标题**：用较大花边标签包裹主标题
- **日期标记**：用小型印章式标签标注日期
- **分类标签/Tag**：用格纹底纹的小型标签
- **空状态提示**：用带插图的中型标签（标签内含小图案 + 短句）

#### 标签 SVG 代码示例

**云朵形标题标签（含蝴蝶结）**
```html
<svg width="320" height="140" viewBox="0 0 320 140">
  <defs>
    <filter id="tagNoise">
      <feTurbulence type="fractalNoise" baseFrequency="0.85" numOctaves="2"/>
      <feColorMatrix type="saturate" values="0"/>
      <feComponentTransfer><feFuncA type="linear" slope="0.08"/></feComponentTransfer>
      <feBlend in="SourceGraphic" mode="multiply"/>
    </filter>
    <pattern id="tagStripe" width="10" height="10" patternUnits="userSpaceOnUse" patternTransform="rotate(0)">
      <rect width="10" height="10" fill="#F5EDD8"/>
      <rect width="3" height="10" fill="#FDF3DC" opacity="0.8"/>
    </pattern>
  </defs>
  <!-- 蝴蝶结（左上） -->
  <path d="M48 20 Q32 10 28 24 Q36 34 52 28" stroke="#C25A4A" stroke-width="1.8" fill="#E8A0A0" opacity="0.95"/>
  <path d="M52 28 Q68 14 72 30 Q64 38 50 32" stroke="#C25A4A" stroke-width="1.8" fill="#E8A0A0" opacity="0.95"/>
  <circle cx="56" cy="24" r="4" fill="#C25A4A" opacity="0.9"/>
  <!-- 云朵轮廓 -->
  <path d="M56 70 Q52 46 82 40 Q102 18 140 28 Q168 14 200 28 Q232 18 258 38 Q288 44 282 72 Q290 96 264 106 Q240 122 200 116 Q168 128 136 116 Q104 126 82 110 Q50 102 56 70 Z"
        stroke="#9B7555" stroke-width="2.4" fill="url(#tagStripe)" stroke-linejoin="round" filter="url(#tagNoise)" opacity="0.95"/>
  <!-- 内层细虚线 -->
  <path d="M70 70 Q66 50 88 46 Q108 30 140 38 Q166 26 198 38 Q226 28 250 46 Q274 52 270 72 Q276 90 256 100 Q232 112 200 108 Q172 116 140 108 Q110 116 90 104 Q68 96 70 70 Z"
        stroke="#C25A4A" stroke-width="1" fill="none" opacity="0.6" stroke-dasharray="3 3"/>
  <!-- 标签文字：Caveat 手写体 -->
  <text x="160" y="78" font-family="Caveat, cursive" font-size="32" fill="#9B7555" text-anchor="middle" transform="rotate(-1 160 78)">Journal Today</text>
  <text x="160" y="100" font-family="'Noto Serif SC', serif" font-size="14" fill="#6C8A5C" text-anchor="middle" transform="rotate(-0.5 160 100)">今日手账</text>
</svg>
```

**花边形日期标签**
```html
<svg width="180" height="80" viewBox="0 0 180 80">
  <!-- 花边框（scalloped edge） -->
  <g stroke="#6C8A5C" stroke-width="1.8" fill="#C5D8C5" opacity="0.95">
    <circle cx="26" cy="20" r="10"/><circle cx="42" cy="12" r="10"/>
    <circle cx="60" cy="10" r="10"/><circle cx="80" cy="8" r="10"/>
    <circle cx="100" cy="10" r="10"/><circle cx="120" cy="12" r="10"/>
    <circle cx="138" cy="16" r="10"/><circle cx="154" cy="22" r="10"/>
    <circle cx="160" cy="40" r="10"/><circle cx="160" cy="52" r="10"/>
    <circle cx="154" cy="66" r="10"/><circle cx="140" cy="72" r="10"/>
    <circle cx="122" cy="76" r="10"/><circle cx="100" cy="78" r="10"/>
    <circle cx="80" cy="78" r="10"/><circle cx="58" cy="76" r="10"/>
    <circle cx="40" cy="72" r="10"/><circle cx="26" cy="66" r="10"/>
    <circle cx="20" cy="52" r="10"/><circle cx="20" cy="40" r="10"/>
  </g>
  <!-- 内层 -->
  <path d="M36 40 Q36 26 54 22 L126 22 Q144 26 144 40 Q144 54 126 58 L54 58 Q36 54 36 40 Z"
        stroke="#6C8A5C" stroke-width="1.6" fill="#FDF3DC" stroke-linejoin="round"/>
  <!-- 日期文字 -->
  <text x="90" y="40" font-family="Caveat, cursive" font-size="22" fill="#9B7555" text-anchor="middle">8月28日</text>
  <text x="90" y="56" font-family="Playfair Display, serif" font-style="italic" font-size="11" fill="#6C8A5C" text-anchor="middle" transform="rotate(1 90 56)">— Thursday —</text>
</svg>
```

**带耳分类标签（格纹底）**
```html
<svg width="140" height="52" viewBox="0 0 140 52">
  <defs>
    <pattern id="tagVichy" width="8" height="8" patternUnits="userSpaceOnUse">
      <rect width="8" height="8" fill="#F5EDD8"/>
      <rect width="8" height="4" fill="#E8A0A0" opacity="0.45"/>
      <rect width="4" height="8" fill="#E8A0A0" opacity="0.45"/>
      <rect width="4" height="4" fill="#C25A4A" opacity="0.55"/>
    </pattern>
  </defs>
  <!-- 左"耳朵" -->
  <path d="M12 14 L4 26 L4 26 L12 38 Z" stroke="#9B7555" stroke-width="1.8" fill="url(#tagVichy)"/>
  <!-- 右"耳朵" -->
  <path d="M128 14 L136 26 L136 26 L128 38 Z" stroke="#9B7555" stroke-width="1.8" fill="url(#tagVichy)"/>
  <!-- 主体 -->
  <path d="M16 10 L124 10 Q130 10 130 16 L130 36 Q130 42 124 42 L16 42 Q10 42 10 36 L10 16 Q10 10 16 10 Z"
        stroke="#9B7555" stroke-width="2" fill="url(#tagVichy)" stroke-linejoin="round"/>
  <!-- 缝线 -->
  <path d="M18 14 L122 14 M18 38 L122 38" stroke="#9B7555" stroke-width="0.7" opacity="0.5" stroke-dasharray="2 2"/>
  <!-- 文字 -->
  <text x="70" y="30" font-family="Caveat, cursive" font-size="20" fill="#9B7555" text-anchor="middle" transform="rotate(-1.5 70 30)"># Diary</text>
</svg>
```

### ❌ 禁止使用的装饰（法式乡村版 · 2026-08-28 扩展）

- 精致矢量插画、扁平化 icon set（Material Icons / undraw / Storyset 等商业插画）
- 3D 角色/场景渲染、等距视角图形、玻璃拟态、金属质感、霓虹灯
- 完美几何图形 + 等宽描边（所有 SVG 必须手绘不规则）
- 高饱和渐变、发光效果、彩虹渐变、金属渐变
- **纯黑线系列**：`#000` / `#111` / `#1A1A1A` / `#222` 任何纯黑近黑（法风线条一律蓝/棕/绿/红）
- **拙趣风残留**：头大身小/火柴人、不闭合断笔、抖动草稿线、铅笔草稿辅助线、静物长"两点眼+弧线嘴"拟人五官
- **旧散点符号系列**：✦ X 交叉四角星、✚ 纯十字小朵、💧 小圆+短竖水滴（一律换法式 6 散点：小花/蝴蝶结/樱桃 pair/小爱心/小星星/省略号）
- **Header 扒边小人**、"慢慢来"虚线圆圈装饰（永久禁止复用）

### 装饰元素代码实现要点（法式乡村版 · 2026-08-28 彻底清掉拙趣风）

生成装饰性 SVG 时，**必须严格按「强制三层」执行**（`SKILL.md L141-149`），禁止 `#000/#1A1A1A` 纯黑线、禁止 `fill="none"` 裸白描（唯一例外：图 1 同墨水色插画群 + 相框外框 + 手绘分割横线）。

#### 1. 线条（必须按语义取色，禁纯黑）

| 语义元素 | 默认描边色 | 默认描边宽 | 端点/拐角 |
|---|---|---|---|
| 纸张外框 / 相框式外框 / 标签外框 | 墨水蓝 `#3B56A6` | 2.0–2.8px | round / round |
| 人物/物品轮廓（猫、毛衣、蛋糕、果酱罐） | 牛皮棕 `#9B7555` 或 墨水蓝 `#3B56A6` | 1.8–2.4px | round / round |
| 缎带、蝴蝶结、樱桃、爱心、邮票齿孔 | 陶土红 `#C25A4A` | 1.6–2.0px | round / round |
| 植物叶、绿格、绿缎带、花茎 | 橄榄绿 `#6C8A5C` | 1.4–2.0px | round / round |
| 内分层线 / 缝线 / 波浪内衬 | 和主描边同色 + opacity 0.5–0.65 | 0.7–1.2px | round |
| 手绘分割横线 / 同墨水插画群（高脚杯+酒瓶） | 墨水蓝 `#3B56A6` | 1.6–2.2px | round |

#### 2. 填色（必须填，不能全部 `fill="none"`）

闭合图形填色优先级：
```
奶黄 #F6EFD6 → 奶油白 #F8F5F0 → 芥末黄 #F6F1C7
→ 薄荷绿 #A8D8C8 → 粉蓝 #D6E4EC → 奶油粉 #F4B9C1
→ 淡紫 #C5B9D9 → 牛皮棕 #9B7555 → 粉糯蓝 #A9CBE3
```
单张贴纸/标签内颜色 ≤ 4（含描边色），禁止高饱和撞色。

#### 3. 噪点层（每个独立装饰 SVG 必带）— ⚠️ 2026-08-28 新增 feBlend / feComposite 二分法

**两种模式必须按元素类型严格区分**（踩过的坑：全用 feBlend 会让带填充色的插画背后出现灰色矩形遮罩）：

##### 模式 A：feBlend multiply — 适合"线类/描边类/外框类"元素（噪点铺满 viewBox 有做旧感）

```html
<defs>
  <filter id="frameGrain" x="0" y="0" width="100%" height="100%">
    <feTurbulence type="fractalNoise" baseFrequency="1.0" numOctaves="2" seed="3"/>
    <feColorMatrix type="saturate" values="0"/>
    <feComponentTransfer><feFuncA type="linear" slope="0.12"/></feComponentTransfer>
    <feBlend in="SourceGraphic" mode="multiply"/>
  </filter>
</defs>
```

✅ 适用元素：
- 外框蓝线 / 相框式手绘边框（frameGrain）
- 标题扇贝波浪描边（titleGrain）
- 咖啡杯 / 大色块填色主体（mugGrain）
- 邮票外框（stampGrain）
- 日期缎带主体（dateGrain）
- 吊牌蝴蝶结 / 挂耳（hangGrain）

##### 模式 B：feComposite operator="in" — 适合"带填充色的独立插画"（噪点严格裁剪到图形内，SVG 空白区域透明）

```html
<defs>
  <filter id="jamGrain" x="0" y="0" width="100%" height="100%">
    <feTurbulence type="fractalNoise" baseFrequency="0.95" numOctaves="2" seed="7"/>
    <feColorMatrix type="saturate" values="0"/>
    <feComponentTransfer><feFuncA type="linear" slope="0.13"/></feComponentTransfer>
    <feComposite in="SourceGraphic" operator="in"/>
  </filter>
</defs>
```

✅ 适用元素：
- 带填充色的标签/徽章（Breakfast 丝带徽章 ribGrain、Diary 吊牌 diagGrain2、Slow Day 邮票 stampGrain2）
- 独立插画贴纸（Bon Maman 果酱罐 jamGrain、樱桃圆蛋糕 cakeCGrain、白猫 catGrain）
- 任何你不希望背后出现灰色方块的元素

❌ 反面清单：给独立插画用 feBlend multiply → SVG viewBox 空白区域会被噪点+multiply 渲染成灰色矩形遮罩

**通用参数范围**：
- `baseFrequency`: 0.80（大颗粒水彩色）→ 1.20（细密打印颗粒）
- `<feFuncA slope>`: 0.10（淡）→ 0.16（深）

#### 4. Vichy 格 pattern（法风标签/装饰必出 ≥ 1 处）

```html
<pattern id="vichyRed" width="10" height="10" patternUnits="userSpaceOnUse">
  <rect width="10" height="10" fill="#F6EFD6"/>
  <rect width="10" height="5"  fill="#C25A4A" opacity="0.30"/>
  <rect width="5"  height="10" fill="#C25A4A" opacity="0.30"/>
  <rect width="5"  height="5"  fill="#C25A4A" opacity="0.50"/>
</pattern>
<!-- 蓝白格：把 #C25A4A 替换为 #3B56A6 即可 -->
```
格宽 8–10px，透明度 0.18–0.35，叠在纯色填色之上（pattern 先画，再用 fill="url(#vichyRed)"）。

#### 5. 法式散点符号（替换旧的 ✦/✚/💧，每主体周围 2–3 个）

| 新散点 | 笔画 & 色 | viewBox |
|---|---|---|
| 4 瓣小花（petite fleur） | 4 片 `path` + 中心 1 点；花瓣粉/紫，花心黄，梗绿；≤ 6 笔 | 20×20 |
| 微型蝴蝶结（mini bow） | 左片 + 右片 + 中心圆；陶土红或橄榄绿；≤ 3 笔 | 20×16 |
| 樱桃 pair（petit cerise） | 2 圆（草莓红/陶土红）+ 1 条绿梗 + 1 片小叶；≤ 4 笔 | 22×18 |
| 小爱心（petit cœur） | 双 Q 曲线心形；陶土红 fill + 墨水蓝描；≤ 2 笔 | 18×16 |
| 小星星（petite étoile） | 4 笔（X 交叉 + 上下 2 小圆点，注意这是法风 4 角星≠旧 X 交叉散点）；墨水蓝或奶油黄 fill | 18×18 |
| 省略号（petits points） | 3 个小圆点；墨水蓝 + 间距 4–5px；≤ 3 笔 | 20×6 |

⚠️ 禁止散点颜色=`#1A1A1A`，散点色必须来自法式色板（蓝/棕/绿/红/粉）。

#### 6. 标签外框（8 种典型 + 手绘不规则感 9 条）

参考 `SKILL.md L251-273` 标签装饰章节：**花边半径不均匀、双耳不对称、外轮廓凹凸化、内层书写区波浪化、局部笔压加粗、局部断线、草稿辅助线、缝线不均匀、每组独有角落装饰、3 个以上形状不重复**。

#### 7. 反面代码清单（生成即不合格）

- ❌ `stroke="#000"` / `#111` / `#1A1A1A` / `#222`（任何纯黑近黑）
- ❌ `<path stroke="#xxx" fill="none">` 占独立装饰画 100%（除了图 1 同墨水插画群 / 相框外框 / 分割横线）
- ❌ 给静物（吐司、标签、云朵、杯子、铅笔、御守）画"两点眼+弧线嘴"拟人五官（猫/熊/玩具除外）
- ❌ `stroke-dasharray="2 2"` 等距缝线（改为 `"3 1 2 2 1 3"` 这类随机组合，上下不同）
- ❌ `<feTurbulence>` 缺失 / 噪点 filter 为空（每个独立装饰 SVG 必须带）
- ❌ 散点仍然使用 `✦ X 交叉 / ✚纯十字 / 💧小圆+短竖`（必须换上面 6 种法式散点）
- ❌ **给带填充色的独立插画用 feBlend multiply**（会在 SVG viewBox 空白区域渲染灰色矩形遮罩 → 改用 feComposite operator="in"，详见 L444-491）
- ❌ **viewBox 未给有向延伸的元素留安全区**（樱桃梗、长羽毛、蝴蝶结飘带等向外延伸的 path，viewBox 顶部/底部/两侧要多留 6-8px → 樱桃散点示例：viewBox="0 -6 28 32" 而非 "0 0 28 24"）
- ❌ **CSS 用通配属性匹配误伤样式**（如 `main section[style*="border-radius"] { background: transparent !important; }` 会把卡片的 bg-paper 也强制透明 → 禁止用 `style*=` / 宽选择器 + `!important` 来改背景色）
- ❌ **插画本体中间堆手写文字**（Bon Maman 果酱罐布标签、樱桃蛋糕侧面的法语手写 → 插画保持干净轮廓+填色，文字放缎带/标题栏/独立标签上）
- ❌ **SVG `<text>` 内联 font-family 硬编码 Noto Serif SC**（SVG 属性优先级高于 CSS 和 Tailwind，硬写 Noto 会完全挡住本地下载的朝华打字机/汇文明朝体 → 必须改为标准链：`'汇文明朝体GBK', '朝华打字机', '迫真打字油印体', serif` 或 `'朝华打字机', '迫真打字油印体', serif`）
- ❌ **日期缎带全程铺满 viewBox**（缎带主体 path 长度 = viewBox 宽度 → 改为只比两端 ♡/·/小花各超 ~5px，短缎带更轻盈）
- ❌ **标题徽章四角全贴满装饰**（左上蝴蝶结+右上樱桃+左下爱心+右下小花四件套 → 最多保留 1 个，优先右下/左下，空角比塞满更显法式轻盈）
- ❌ **选了主色 B（浅灰蓝底）却用 A 底默认贴纸色值**：标签 fill 仍是 `#F6EFD6/#F8F5F0`、pattern opacity 仍是 `0.18–0.35`、stroke-width 仍是 `1.6–2.0px`、feFuncA slope 仍是 `0.12` → 会导致贝壳/邮票/吊牌标签淡到融在背景里；B 底必须换成 L64-79 的 B 底专用表
- ❌ **B 底贴纸 fill 仍用米黄纸 `#F6EFD6`**：米黄纸暖色和灰蓝冷色太接近、亮度差 < 10 → 标签完全融背景；B 底贴纸 fill 必须 `#F7F4EF`（米白浅纸 + 5% 牛奶白偏色）
- ❌ **B 底 pattern opacity < 0.30**：Vichy 格/条纹/波点叠在灰蓝底上压成一块灰，看不出纸纹；必须 ≥ 0.35，最佳 0.40–0.45
- ❌ **新任务生成代码跳过字体初始化模板**（没写 @font-face 3 段 / 没写 `body{}` 首位朝华打字机 / 没在 tailwind.config 里声明 `handwritten-cn` / `typewriter-cn` / `body-cn` → 中文字体 100% 回落到系统微软雅黑/苹方，Skill 全部字体规则失效）
- ❌ **tailwind.config 里 body-cn 仍写 `思源宋体 Regular` / `Noto Serif SC`** → 与正文 L99-127 定稿冲突；正文已统一改为朝华打字机优先，思源宋体只作系统级 fallback，不在 tailwind fontFamily 链里出现

## 动效与交互
- 页面加载：淡入 + 轻微上浮（opacity 0→1, translateY 10px→0）
- 按钮悬停：颜色加深 + translateY(-2px)
- 卡片点击：轻微下沉 translateY(2px) + 阴影加深
- 滚动动画：元素随滚动淡入（intersection observer + fade-in）
- 过渡曲线：transition: all 0.3s ease-in-out
- 禁止：弹性弹跳、快速滑动、高对比度闪烁
- 装饰元素（如小人、树叶）可使用微妙的"呼吸"动效：轻微缩放（scale 1.0~1.03）+ 缓慢旋转（-2°~2°），周期 3~5s
- 加载动画使用简笔画小人做日常动作（喝茶、发呆、浇花），而非标准 spinner
- 禁止丝滑拟真动效——动效应带一点"笨拙的停顿与弹跳"

## 反面清单（Anti-Patterns）
- ❌ 纯黑/纯白背景
- ❌ 高饱和荧光色（亮粉、电光蓝、霓虹绿）
- ❌ 直角或全圆角组件
- ❌ 无衬线粗体（Arial Black、Impact、Helvetica Bold）
- ❌ 密集排版/无留白
- ❌ 标准化扁平图标（Material Icons等）—— 应使用手绘风格图标
- ❌ 金属质感、玻璃拟态、霓虹灯效果
- ❌ 复杂渐变（彩虹渐变、金属渐变）
- ❌ 强弹窗/硬切换 —— 应用轻柔滑入或淡入
- ❌ 无纹理的平滑纯色背景
- ❌ 精致的商业插画（undraw/Storyset风格的扁平人物插画）
- ❌ 3D图标、等距视角图形、玻璃拟态
- ❌ 完美对称的装饰图案
- ❌ 过度装饰——页面不应看起来"很设计"

## 代码输出要求
- 使用 Tailwind CSS 类名优先
- 颜色值使用 CSS 变量管理，禁止硬编码
- 组件必须包含 hover/active/disabled 状态
- 字体通过 Google Fonts CDN 引入
- 装饰元素优先使用 SVG inline，避免外部图片依赖
- 生成页面禁止在右上角、右下角或任何边缘位置显示"由AI生成"、"AI Generated"、"Generated by AI"等角标、水印、免责声明或任何暗示内容由AI生成的标识

---

# HTML `<head>` 字体初始化模板（⚠️ 新任务第一步：必须原样抄入）

> **为什么要放到最前面执行？** 因为 3 款中文字体（汇文明朝体GBK/朝华打字机/迫真打字油印体）**全靠本地 `.ttf` + `@font-face` 声明**，浏览器不会从任何 CDN 自动拉取。如果 `<head>` 里缺了下面任一块，中文字体直接回落到系统微软雅黑/苹方，Skill 定的规则全白搭。

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- ===== ① Google Fonts（仅英文，中文走本地） ===== -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Caveat:wght@400;600&family=Lora:ital,wght@0,400;0,600;1,400&family=Playfair+Display:ital,wght@0,400;1,400&family=Noto+Serif+SC:wght@400;600&display=swap" rel="stylesheet">

  <!-- ===== ② 本地中文字体 @font-face（3 个 .ttf 必须放 fonts/ 目录） ===== -->
  <style>
    @font-face {
      font-family: '汇文明朝体GBK';
      src: url('fonts/HuiwenMingchaoGBK.ttf') format('truetype');
      font-weight: normal;
      font-style: normal;
      font-display: swap;
    }
    @font-face {
      font-family: '朝华打字机';
      src: url('fonts/ZhaohuaTypewriter.ttf') format('truetype');
      font-weight: normal;
      font-style: normal;
      font-display: swap;
    }
    @font-face {
      font-family: '迫真打字油印体';
      src: url('fonts/PozhenTypewriter.ttf') format('truetype');
      font-weight: normal;
      font-style: normal;
      font-display: swap;
    }

    /* ===== ③ body 全局默认：朝华打字机优先（正文走这条） ===== */
    body {
      font-family: '朝华打字机', '迫真打字油印体', 'Noto Serif SC', 'Lora', serif;
    }
    /* 标题类标签默认用汇文明朝体（<h1> <h2> <h3> 直接生效，不用手写 font-handwritten-cn） */
    h1, h2, h3 {
      font-family: '汇文明朝体GBK', '朝华打字机', '迫真打字油印体', serif;
    }
  </style>

  <!-- ===== ④ Tailwind CDN + 扩展主题（色板 + fontFamily 3 中文字体类） ===== -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          // ↓↓ 完整色板直接抄下面 "Tailwind CSS 配置参考" 的 colors 段 ↓↓
          colors: { /* 复制 SKILL.md L613-646 的 colors {...} */ },
          // ↓↓ 中文字体 3 类必须和 L99-127 / tailwind.config 保持一致 ↓↓
          fontFamily: {
            'handwritten-cn': ['"汇文明朝体GBK"', '"朝华打字机"', '"迫真打字油印体"', 'serif'],
            'typewriter-cn':  ['"朝华打字机"', '"迫真打字油印体"', 'serif'],
            'body-cn':        ['"朝华打字机"', '"迫真打字油印体"', 'serif'],
            'handwritten-en': ['"Caveat"', '"Dancing Script"', '"Great Vibes"', 'cursive'],
            'body-en':        ['"Lora"', '"Merriweather"', '"Playfair Display"', 'serif'],
          },
          // ↓↓ 其余 borderRadius / boxShadow / spacing 也抄配置参考 ↓↓
        }
      }
    }
  </script>
</head>
```

### 新任务字体自检 Checklist（生成代码前必须逐条通过）
1. ✅ **字体文件存在吗？** → `project-root/fonts/` 下必须有 3 个文件：`HuiwenMingchaoGBK.ttf`、`ZhaohuaTypewriter.ttf`、`PozhenTypewriter.ttf`；**没有 → 先提醒用户放文件，或把 @font-face 的 src 替换为可访问的 CDN URL**（禁止直接删掉 @font-face）
2. ✅ **@font-face 3 段齐了吗？** → `<style>` 里 `汇文明朝体GBK` / `朝华打字机` / `迫真打字油印体` 三条各一条，一条都不能缺
3. ✅ **`body {}` 全局 font-family 首位 = 朝华打字机？** → 禁止首链是 `Noto Serif SC` / `serif` / `sans-serif`
4. ✅ **SVG `<text>` 内联 font-family 没用 Noto Serif SC？** → 必须写 `'汇文明朝体GBK', '朝华打字机', '迫真打字油印体', serif` 或 `'朝华打字机', '迫真打字油印体', serif`

---

# Tailwind CSS 配置参考

```js
// tailwind.config.js  — 2026-08-28 基于5张参考图校准法式乡村小清新色板
module.exports = {
  theme: {
    extend: {
      colors: {
        // 主色（背景/大面积）
        'paper': '#F8F5F0',       // 奶油白（卡片/次级区块底）
        'cream-paper': '#F6EFD6', // 奶黄纸（整页底色首选，图1邀请卡）
        'ivory': '#F5F0E8',       // 米白浅纸（留白/空白区，图5海报纸）
        'mist-blue': '#D6E4EC',   // 浅灰蓝（冷区块背景）
        'mustard': '#F6F1C7',     // 淡芥末黄（暖区块强调）

        // 墨水蓝系（所有"线条"默认用这里）
        'ink-blue': '#3B56A6',    // 手写墨水蓝（邀请卡描边/手绘正文首选）
        'typewriter-blue': '#2F4B8F', // 深打字机蓝（标题字/主强调线）
        'sticker-blue': '#A9CBE3',// 粉蓝贴纸外框（不用于文字）

        // 田园色板（图4水粉贴纸+图2/3彩色标签）
        'terracotta': '#C25A4A',  // 陶土红/砖红（缎带/心形/樱桃/齿孔）
        'cream-pink': '#F4B9C1',  // 奶油粉（蛋糕身体）
        'lavender': '#C5B9D9',    // 淡紫薰衣草（花边框/小装饰）
        'olive': '#6C8A5C',       // 橄榄花园绿（植物叶/绿缎带/绿格子）
        'mint': '#A8D8C8',        // 薄荷绿（糖霜/浅绿填充）
        'goose': '#F1D37D',       // 鹅黄浅（奶油黄/小黄花/标签底）
        'cow-brown': '#9B7555',   // 牛皮棕（可颂/小熊毛皮/果酱罐/标签文字）

        // 强调色（≤ 2 笔的小撞色用）
        'strawberry': '#D9556B',  // 草莓红（樱桃/爱心/蝴蝶结点）
        'cherry-deep': '#8A3A54', // 深樱桃紫（水果/印章）

        // 粉糯色系（法式杂货标签底，兼容旧命名）
        'cream-yellow': '#FDF3DC',
        'blush-pink': '#F4B9C1',
        'powder-blue': '#A9CBE3',
        'dusty-pink': '#E8A0A0',
        'soft-mint': '#A8D8C8',
        'dusty-lilac': '#C5B9D9',
        'deep-brown': '#9B7555',  // 兼容旧class，指向牛皮棕
      },
      fontFamily: {
        // ⚠️ 2026-08-28 定稿：中文字体 3 类，与正文 L99-127 保持一致，禁止手动修改
        'handwritten-cn':  ['"汇文明朝体GBK"', '"朝华打字机"', '"迫真打字油印体"', 'serif'],
        'typewriter-cn':   ['"朝华打字机"', '"迫真打字油印体"', 'serif'],   // 插画下小字/心情卡片正文
        'body-cn':         ['"朝华打字机"', '"迫真打字油印体"', 'serif'],   // 正文/段落（不再优先思源宋体）
        // 英文字体
        'handwritten-en': ['"Caveat"', '"Dancing Script"', '"Great Vibes"', 'cursive'],
        'body-en': ['"Lora"', '"Merriweather"', '"Playfair Display"', 'serif'],
      },
      borderRadius: {
        'soft': '6px',            // 软圆角，避免尖锐感
        'pill': '999px',          // 胶囊形按钮
      },
      boxShadow: {
        'paper': '0 2px 8px rgba(59, 86, 166, 0.06)',      // 纸张浮起感阴影（墨水蓝透明）
        'hand-drawn': '0 1px 3px rgba(59, 86, 166, 0.10)',// 手绘线条投影
        'sticker': '2px 3px 0 rgba(155, 117, 85, 0.18)',  // 贴纸硬投影（牛皮棕透明）
      },
      spacing: {
        'notebook': '1.5rem',     // 手账本行距基准
      }
    }
  }
}
```

### 使用规则
- 所有文字颜色必须使用 `typewriter-blue` / `ink-blue` 或其变体，禁止使用 `#000000`。
- 整页背景色优先使用 `cream-paper`（奶黄纸），卡片/次级区块使用 `paper`（奶油白），冷区块用 `mist-blue`，暖区块强调用 `mustard`。
- 装饰性线条默认 `ink-blue`；缎带蝴蝶结/樱桃用 `terracotta`；植物/叶子用 `olive`；面包/果酱罐/标签文字用 `cow-brown`。
- 所有圆角统一使用 `soft` 或 `pill`，避免直角。
- 阴影仅用于卡片或浮层，使用 `paper` / `hand-drawn` / `sticker`，禁止使用深色硬阴影。

---

# 组件模板参考

## 卡片组件（Card）

```html
<div class="bg-mist-blue rounded-soft p-6 shadow-paper border border-lavender/30">
  <h2 class="font-handwritten-en text-2xl text-ink-blue mb-2">Outside is Summer</h2>
  <p class="font-body-en text-base text-ink-blue leading-relaxed">
    "The trivial and boring days accumulate into seasons, and seasons accumulate into life."
  </p>
  <div class="mt-4 flex items-center gap-2">
    <span class="text-xs text-lavender">— Kim Ae-ran</span>
  </div>
</div>
```

## 按钮组件（Button）

```html
<button class="bg-terracotta text-paper font-handwritten-en px-6 py-2 rounded-pill shadow-hand-drawn hover:bg-mint transition-colors duration-300">
  Read More
</button>
```

## 分隔线组件（Divider）

```html
<div class="border-t border-lavender/40 my-6"></div>
```

或手绘风格：

```html
<div class="h-px bg-ink-blue/20 my-6 relative">
  <span class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 text-lavender text-xs">✦</span>
</div>
```

## 引用块组件（Blockquote）

```html
<blockquote class="border-l-4 border-olive pl-4 py-2 bg-paper/50 rounded-r-soft">
  <p class="font-body-cn text-ink-blue italic">
    “琐碎而无聊的日子一天天积累下来成为四季，四季积累下来就是人生。”
  </p>
  <footer class="text-sm text-lavender mt-2">— 《外面是夏天》</footer>
</blockquote>
```

## 标签组件（Tag）

```html
<span class="bg-mustard text-ink-blue text-xs font-handwritten-en px-3 py-1 rounded-pill">
  #SummerVibes
</span>
```

## 导航栏组件（Navbar）

```html
<nav class="bg-paper border-b border-lavender/30 px-6 py-4">
  <div class="flex justify-between items-center">
    <h1 class="font-handwritten-cn text-2xl text-ink-blue">My Journal</h1>
    <div class="flex gap-4">
      <a href="#" class="font-body-en text-ink-blue hover:text-terracotta transition-colors">Home</a>
      <a href="#" class="font-body-en text-ink-blue hover:text-terracotta transition-colors">Entries</a>
      <a href="#" class="font-body-en text-ink-blue hover:text-terracotta transition-colors">About</a>
    </div>
  </div>
</nav>
```

## 图片容器组件（Image Frame）

```html
<div class="relative rounded-soft overflow-hidden shadow-paper border border-lavender/20">
  <img src="/path/to/image.jpg" alt="Hand-drawn illustration" class="w-full h-auto object-cover">
  <div class="absolute bottom-0 left-0 right-0 bg-paper/80 p-3">
    <p class="font-handwritten-en text-sm text-ink-blue">A quiet afternoon in the garden</p>
  </div>
</div>
```

### 组件使用规则
- 所有组件必须使用 `font-handwritten-*` 作为标题字体，`font-body-*` 作为正文字体。
- 所有组件的圆角必须使用 `rounded-soft` 或 `rounded-pill`。
- 所有组件的阴影必须使用 `shadow-paper` 或 `shadow-hand-drawn`。
- 所有组件的边框颜色必须使用 `lavender/30` 或 `ink-blue/20`。
- 所有组件的文字颜色必须使用 `ink-blue` 或其变体。
- 所有组件的背景色必须使用 `paper`、`mist-blue` 或 `mustard`。
- 所有组件的间距必须使用 `notebook` 或其倍数。
