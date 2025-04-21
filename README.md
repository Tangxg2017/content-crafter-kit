# ✨ 启发星球金句卡片 & 封面图生成器

这是一个为「启发星球」项目设计的视觉内容生成器，支持创建带关键词/引导语的**金句卡片**与**封面图**，并支持本地批量生成、在线编辑、下载与部署展示。

---

## 🚀 功能特点

### 🖼 封面图生成器
- 支持自定义背景图
- 支持上传本地照片作为背景图，方便使用旅行照片或真实生活场景
- 支持实时预览 + PNG 下载
- 后续支持情绪标签筛选背景图

👉 在线体验：
- [封面图编辑器](https://sunling.github.io/flashcard-for-inspiration-planet/cover-editor.html)

---

### 📒 金句卡片生成器
- 自定义标题 / 金句 / 具体事例
- 自动计算会议日期、下次会议时间
- 每张卡片配背景图，导出为高清竖图
- 本地批量生成 + 上传展示

👉 在线体验：
- [金句卡片编辑器](https://sunling.github.io/flashcard-for-inspiration-planet/card-editor.html)

👉 示例展示：[所有卡片](https://sunling.github.io/flashcard-for-inspiration-planet)

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
