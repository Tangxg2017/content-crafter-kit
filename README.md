# ✨ 启发星球金句卡片 & 封面图生成器

这是一个用来创作「启发星球」金句卡片与封面图的小工具集合，支持本地生成 + GitHub Pages 在线编辑与下载。

---

## 📦 项目结构

```
flashcard-for-inspiration-planet/
├── data/                   # 卡片数据（如 card_data.json）
├── docs/                   # GitHub Pages 部署根目录
│   ├── index.html          # 卡片展示页面
│   ├── generated/
│   │   └── cards/          # 生成的金句卡片图片
│   ├── cover-editor.html   # ✅ 封面图编辑页面（支持在线预览 + 下载）
│   └── images.json         # 背景图文件列表
├── images/                 # 所有封面图背景图像（路径为 images/*.png）
├── templates/              # 模板 HTML 片段
│   └── cover.html          # 单页封面图模板（配合 Puppeteer 批量生成）
├── scripts/                # 生成脚本
│   ├── generate-card.js    # 批量生成金句卡片
│   └── generate-cover.js   # 批量生成封面图
├── cover.css               # 卡片与封面图通用样式
└── README.md
```

---

## 🧪 封面图在线编辑器（无需本地运行）

📍 地址：

👉 [在线使用 cover-editor.html](https://sunling.github.io/flashcard-for-inspiration-planet/docs/cover-editor.html)

你可以：

- 填写关键词与引导问题
- 选择背景图（来自 `images/` 目录）
- 一键预览并下载封面图 `.png`

📌 注意：为支持 GitHub Pages 部署，封面图路径使用 `images/xxx.png`，**不要加上 `docs/` 前缀**。

---

## 🛠 本地生成卡片/封面图

### 安装依赖（首次）

```bash
npm install
```

### 运行脚本生成卡片与封面图

```bash
npm run gen:cards
npm run gen:cover
```

结果将输出至 `docs/generated/cards/` 或 `docs/generated/covers/` 中。

---

## 📄 如何新增封面图背景

1. 将 `.png` 图片放入 `/images/` 文件夹
2. 运行：

```bash
npm run generate-images-json
```

将自动更新 `docs/images.json` 文件，供在线编辑器使用。

---

## 🔥 Todo

- [x] 支持关键词 + 问题生成封面图
- [x] 支持 html2canvas 截图下载
- [ ] 支持切换不同主题封面图（如启发时刻、会议总结等）
- [ ] 添加移动端适配样式

---

欢迎使用 & 提建议！💫
