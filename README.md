# 🌍 flashcard-for-inspiration-planet

一个用于生成【启发星球】金句卡片的自动化图文工具  
支持批量生成高质量截图 + 自动发布到 GitHub Pages，用于公众号、小红书等图文发布平台。

<p align="center" alt="demo">
  <img src="screenshots/demo.png" alt="金句卡片示例" width="400"/>
</p>


---

## 🔥 在线预览

👉 页面地址：  
[https://sunling.github.io/flashcard-for-inspiration-planet/](https://sunling.github.io/flashcard-for-inspiration-planet/)

👉 在线编辑器：  
[https://sunling.github.io/flashcard-for-inspiration-planet/editor.html](https://sunling.github.io/flashcard-for-inspiration-planet/editor.html)

---

## 📁 项目结构

```
flashcard-for-inspiration-planet/
├── data.json                 # 金句数据源，每条包含 title, quote, id, episode 等字段
├── template.html             # 卡片 HTML 模板，支持变量替换
├── card.css                  # 卡片统一样式，供 template/editor 共用
├── generate.js               # 核心生成脚本：截图 + 发布 + 图文更新
├── screenshots/              # 所有生成截图会先保存到这里
├── docs/
│   ├── index.html            # 自动生成的展示页（由 generate.js 生成）
│   ├── editor.html           # 可视化金句编辑器，可在线预览与下载
│   ├── images.json           # 自动生成的图片列表，供 editor 使用
│   ├── images/               # 存放卡片插图，图片名称需与 id 匹配
│   └── generated_cards/      # 自动生成的卡片截图（最终用于展示）
```

---

## ✨ 功能亮点

- 🖼 卡片截图高清，自动裁边，支持高倍分辨率
- ⏱ 日期 & 会议时间根据集数自动推算
- 🔁 已生成的图片自动跳过，避免重复计算
- 🧠 支持批量生成、可视化编辑与本地下载
- 🌐 自动生成展示页面，托管在 GitHub Pages

---

## 🚀 使用说明

### 1. 安装依赖

```bash
npm install puppeteer
```

> 🧠 mac 用户需手动指定 Chrome 路径，已在 generate.js 中设定

---

### 2. 准备数据和图片

- 在 `data.json` 中填写每一张卡片信息
- 确保每条数据的 `id` 对应 `docs/images/` 中的图片

---

### 3. 生成卡片

```bash
node generate.js
```

完成以下步骤：
- ⏳ 渲染并截图 `.card` 元素（每张一张）
- 📁 自动复制新图至 `docs/generated_cards/`
- 🌐 自动生成 `index.html` 和 `images.json`
- ✅ GitHub Pages 页面即时可用！

---

## 🧑‍💻 在线编辑器

在浏览器中访问：

```
https://sunling.github.io/flashcard-for-inspiration-planet/editor.html
```

支持：
- 填写字段实时预览
- 更换图片插图
- 下载 PNG 截图

---

## 🧡 由谁创造

由 [Ling Sun](https://sunling.github.io) 设计并持续维护  
欢迎复用、提问或提出改进建议 ✨
