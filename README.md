# Cyrilla's Portfolio

面向学习、写作、项目评审与设计场景的个人网页工具作品集。

[访问作品集](https://hiseeu-yomiiii.github.io/portfolio/)

## 项目简介

本仓库是 Cyrilla Web 的统一展示入口，集中呈现 AI 产品、效率工具、设计工具和专题网页。项目以实际可使用的网页功能为核心，并保持简洁、清晰和移动端友好的界面风格。

## 核心 AI 产品

### 衡准 · Verity

项目材料 AI 质检与评审工具。支持 DOCX/TXT 材料解析、项目理解、证据完整度分析、五维评分、风险识别、评委追问和 S/A/B 行动建议。

- [在线体验](https://hiseeu-yomiiii.github.io/verity/)
- [GitHub 仓库](https://github.com/hiseeu-yomiiii/verity)

### 墨推 · Inkraft

面向大学生中文论文写作的 AI 体检与优化助手，提供论文体检、降重、学术润色、摘要生成、翻译润色和参考文献格式化，并加入改写质量检查与风险提醒。

- [在线体验](https://hiseeu-yomiiii.github.io/inkraft/)
- [GitHub 仓库](https://github.com/hiseeu-yomiiii/inkraft)

### 棱镜 · PrismAI

AI 多角色评审工具。通过不同角色分别审阅材料，再生成综合评分、五维评分和 S/A/B 最终行动清单。

- [在线体验](https://hiseeu-yomiiii.github.io/prism-ai/)
- [GitHub 仓库](https://github.com/hiseeu-yomiiii/prism-ai)

## 效率与设计工具

### Prompt Tools

面向学习、写作、项目与求职场景的 Prompt Builder。选择模板后自动识别主题、字数、风格等占位符，通过表单生成完整 Prompt。

[在线使用](https://hiseeu-yomiiii.github.io/portfolio/prompt-tools.html)

### AI 工具导航

收录常用 AI 与效率工具，支持分类浏览、关键词搜索、标签筛选、收藏和随机推荐。

[在线使用](https://hiseeu-yomiiii.github.io/portfolio/ai-tools.html)

### 配色生成器

根据主色生成互补色、类似色和三角色方案，并提供色阶、界面预览和历史记录。

[在线使用](https://hiseeu-yomiiii.github.io/portfolio/color-palette.html)

### 渐变背景生成器

生成线性、径向、锥形渐变和图案背景，支持颜色节点调整、全屏预览及 CSS 代码复制。

[在线使用](https://hiseeu-yomiiii.github.io/portfolio/gradient-generator.html)

## 专题网页

- **BNPL 先用后付网站**：围绕先用后付产品与消费风险进行信息展示。
- **泰顺廊桥网站**：展示泰顺廊桥文化、传统建筑与相关人文内容。

## 技术特点

- 原生 HTML、CSS 和 JavaScript
- 不使用前端框架
- GitHub Pages 静态部署
- 桌面端与移动端响应式适配
- 支持日夜主题
- 卡片式界面与统一视觉风格
- AI API 通过 Cloudflare Worker 转发
- API Key 保存在 Worker 环境变量中，不写入前端代码

## 仓库页面

```text
index.html                 作品集主页
ai-tools.html              AI 工具导航
prompt-tools.html          Prompt Builder
color-palette.html         配色生成器
gradient-generator.html    渐变背景生成器
```

Inkraft、PrismAI 和 Verity 使用独立仓库维护，本仓库主页提供统一入口。

## 使用与安全提示

AI 产品的输入内容会通过 Cloudflare Worker 发送至相应模型服务完成处理。请勿提交身份证号、联系方式、未公开材料或其他敏感信息。

AI 输出仅作辅助分析与内容优化参考，涉及事实、数据和重要结论时需要人工复核。

## 作者

Cyrilla

© 2026 Cyrilla Web
