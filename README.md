# French Vintage UI 🎀

法式复古小清新 UI 设计规范 Skill — 适用于 App 和 Web 端的 AI 辅助界面生成。

核心调性：**手作感 + 低饱和自然色系 + 手写体排版 + 生活化装饰元素**。

---

## 适用场景

- 小清新风格博客 / 手账 / 杂货铺页面
- 烘焙、花艺、咖啡、生活方式类 App
- 礼物卡、节日贺卡、邀请函页面

> 不适用于：企业级后台管理系统、数据大屏、金融交易界面、游戏 UI。

---

## 规范内容

| 模块 | 说明 |
|---|---|
| **色彩体系** | 16 色设计令牌（奶黄纸、奶油白、墨水蓝、陶土红、橄榄花园绿等） |
| **主色选择** | A 奶油白底 / B 浅灰蓝底 / C 淡芥末黄底，三套联动规则 |
| **中文字体** | 3 类：`handwritten-cn`（汇文明朝体GBK）/ `typewriter-cn`（朝华打字机）/ `body-cn`（朝华打字机） |
| **英文字体** | 2 类：`handwritten-en`（Caveat / Dancing Script）/ `body-en`（Lora / Merriweather） |
| **字体初始化模板** | HTML `<head>` 完整代码段（@font-face × 3 + body 全局 + Tailwind CDN） |
| **杂货标签贴纸风** | 8 种组件规范（椭圆徽章 / 丝带 / 挂孔吊牌 / 邮票齿孔 / 蕾丝圆章等） |
| **底纹 pattern** | 7 种（Vichy 格 / 条纹 / 波点 / 蕾丝 / 网格 / 满版印章 / 信纸线） |
| **噪点滤镜** | feBlend / feComposite 二分法（线类用 multiply，填充类用 in） |
| **动效与交互** | 淡入上浮 / 悬停加深 / 缓动曲线 / 心情卡片呼吸感 |
| **反面代码清单** | 12 条踩坑规则（避免常见错误） |

---

## 中文字体文件

3 款中文字体需下载到项目 `fonts/` 目录：

| 字体 | 文件名 | 用途 |
|---|---|---|
| 汇文明朝体GBK | `fonts/HuiwenMingchaoGBK.ttf` | 标题 / 重点文字 |
| 朝华打字机 | `fonts/ZhaohuaTypewriter.ttf` | 正文 / 插画小字 |
| 迫真打字油印体 | `fonts/PozhenTypewriter.ttf` | 打字机风格 fallback |

三款字体均由 **特里王** 制作，免费商用。

---

## 使用方式

将 `SKILL.md` 放入项目的 `.trae/skills/french-vintage-ui/` 目录，AI 生成页面时会自动应用本规范。

技术栈：Tailwind CSS + SVG inline + Google Fonts（英文）+ 本地 @font-face（中文）。

---

## 版本历史

| 版本 | 日期 | 说明 |
|---|---|---|
| v1.0 | 2026-08-28 | 首次定稿 |
