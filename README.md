# NoteVault · Demo Vault

> 在线示例：[https://zhsmm.github.io/notevault-demo/](https://zhsmm.github.io/notevault-demo/)
>
> 这个仓库是一个**示例 vault**，用来展示 [NoteVault](https://github.com/ZhSMM/notevault) 能做什么。
> Notes are auto-built and deployed via GitHub Actions on every push.

## 📂 内容

- **欢迎使用 NoteVault** — 入门导览
- **学习路线** — Rust 学习路径示例
- **P2 链接网络 Showcase** — wikilink / 块引用 / 反向链接演示
- **P4 间隔重复 Showcase** — FSRS 闪卡演示
- **渲染能力 Showcase** — Shiki 高亮 + Mermaid 图表 + 表格
- **Transclusion Demo** — `![[note]]` 嵌入演示
- **topics/rust/** — 所有权 / 借用 / 生命周期 / trait 四个 Rust 概念笔记
- **journals/** — 日记格式

## 🚀 怎么用

### 在浏览器看

直接访问 [https://zhsmm.github.io/notevault-demo/](https://zhsmm.github.io/notevault-demo/)。

### 在本地 NoteVault 打开

1. 下载 [NoteVault](https://github.com/ZhSMM/notevault/releases)
2. 启动后选 "Open vault"
3. 把这个仓库的根目录作为 vault 路径
4. 就能像编辑普通文件一样写笔记

### 自己改 + 重新部署

1. **Fork** 这个仓库
2. 修改 `.md` 文件
3. push → GitHub Actions 自动重新 build + 部署
4. 几分钟后看你的 Pages 站点

## 🛠️ 技术

- 笔记格式：Markdown + YAML frontmatter + wikilink `[[X]]` + 块引用 `((blk_xxx))` + 闪卡标记 `#card` / `#cloze`
- SSG：[notevault 仓库](https://github.com/ZhSMM/notevault) 里的 `scripts/static-build.mjs`（markdown-it + Shiki + Mermaid + fuse.js 搜索）
- 自动部署：GitHub Actions → GitHub Pages
- 模板仓库结构：

```
sample-vault/
├── .github/workflows/publish.yml   ← 自动部署 workflow
├── 欢迎使用 NoteVault.md             ← 笔记
├── topics/rust/所有权.md             ← 嵌套目录支持
├── journals/2026-07-12.md           ← 日记
└── CNAME                            ← （可选）自定义域名
```

## 📝 自己写笔记

- 加 `.md` 文件（YAML frontmatter 可选但推荐）
- 用 `[[双向链接]]` 互相串联
- 闪卡：`- 问题？ #card\n  答案`
- 嵌入：`![[另一篇笔记]]` 或 `![[另一篇笔记#章节]]`

## 📄 License

笔记内容 MIT，代码归 [ZhSMM/notevault](https://github.com/ZhSMM/notevault) 所有。
