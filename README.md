# ✨ 启发星球金句卡片 & 封面图生成器

这是一个为「启发星球」项目设计的视觉内容生成器，支持创建带关键词/引导语的**金句卡片**与**封面图**，并支持本地批量生成、在线编辑、下载与部署展示。

---

## 🚀 功能特点

### 🖼 封面图生成器
- **背景图自定义**：支持上传本地照片或使用内置背景库
- **智能适配**：自动优化不同尺寸需求（桌面/移动端）
- **实时预览**：所见即所得的编辑体验
- **一键导出**：高清PNG格式下载
- **情绪标签筛选**：快速找到符合意境的背景图（开发中）

👉 在线体验：
- [桌面版编辑器](https://sunling.github.io/flashcard-for-inspiration-planet/cover-editor.html)
- [移动端优化版](https://sunling.github.io/flashcard-for-inspiration-planet/cover-editor-mobile.html)

---

### 📒 金句卡片生成器
- **全字段自定义**：标题/金句/事例自由编辑
- **智能日期计算**：自动生成会议日期和下次会议时间
- **批量处理**：支持本地一键生成多张卡片
- **高清导出**：优化打印质量的竖版图片
- **在线展示**：生成后可立即发布查看

👉 在线体验：
- [卡片编辑器](https://sunling.github.io/flashcard-for-inspiration-planet/card-editor.html)
- [示例展示墙](https://sunling.github.io/flashcard-for-inspiration-planet)

---

## 🧰 使用指南

### 1. 安装依赖

```bash
npm install
```

### 2. 本地生成内容

```bash
npm run gen:cards   # 批量生成金句卡片
npm run gen:cover   # 批量生成封面图
```

---

## 🗂 项目结构概览

```
flashcard-for-inspiration-planet/
├── data/                   # 金句卡片和封面图数据 json
├── docs/                   # GitHub Pages 托管目录
│   ├── cover-editor.html   # 封面图关键词式编辑器
│   ├── cover-editor-mobiel.html   # 封面图关键词式编辑器移动端
│   ├── card-editor.html    # 金句卡片编辑器
│   ├── card.css            # 金句卡片样式
│   ├── cover.css           # 封面图样式
│   ├── index.html          # 金句卡片展示页
│   ├── generated/
│   │   ├── cards/          # 导出的金句卡片图像
│   │   └── covers/         # 导出的封面图图像
|   ├── images/             # 所有背景图资源
│   └── images.json         # 背景图元数据（含情绪标签）          
├── scripts/                # puppeteer 生成脚本
│   ├── generate-card.js
│   ├── generate-cover.js
│   └── ...
├── templates/              # HTML模板
│   │── card.html           # 金句卡片模板html
│   │── cover.html          # 封面图模板html 
├── README.en.md  
└── README.md
```

---

欢迎体验 & 欢迎建议 🌱
