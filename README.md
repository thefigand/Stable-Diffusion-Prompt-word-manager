# SD Prompt Gallery

A lightweight, single-file local web app for managing Stable Diffusion prompts and their corresponding generated images. All data is stored as real files on your disk — no cloud, no server, no database.

---

## Features

- **Prompt + Image Pairing** — Store prompts alongside their generated images for easy reference
- **Negative Prompts & Notes** — Record negative prompts, model names, samplers, CFG scale, resolution, and any other parameters
- **Tag System** — Organize entries with custom tags (e.g., character, landscape, anime) for quick filtering
- **Full-text Search** — Search across titles, prompts, tags, and notes instantly
- **Lightbox Preview** — Click any image to view it full-screen with prompt details
- **One-click Copy** — Copy prompts to clipboard for immediate use in Stable Diffusion
- **Local File Storage** — Images and metadata are saved as actual files in a folder you choose, not in browser storage
- **No Compression** — Original image files are preserved at full quality
- **Persistent Access** — The app remembers your chosen folder; reconnect with a single click on next launch

## How It Works

```
your_chosen_folder/
└── sd_gallery_data/
    ├── index.json        ← All prompt metadata (titles, prompts, tags, notes)
    └── images/           ← Original image files
        ├── e1a2b3c.jpg
        ├── e4d5e6f.png
        └── ...
```

The app uses the **File System Access API** to read and write directly to your local disk. This means:

- Data survives browser cache clearing, reinstalls, and OS migrations
- You can back up or sync the folder using any file sync tool (OneDrive, Dropbox, etc.)
- There is no size limit — store as many high-resolution images as your disk allows

## Quick Start

1. Download `SD Prompt Gallery.html`
2. Open it in **Chrome** or **Edge** (required for File System Access API support)
3. Select a folder on your computer for data storage
4. Start adding prompts and images!

> **Note:** Firefox and Safari are not supported due to lack of File System Access API.

## Browser Requirements

| Browser | Support |
|---------|---------|
| Chrome  | ✅ Full |
| Edge    | ✅ Full |
| Firefox | ❌ Not supported |
| Safari  | ❌ Not supported |

## Why Not localStorage?

Earlier versions stored data in `localStorage`, which has a ~5-10MB limit and is lost when browser data is cleared. This version stores everything as real files on disk, giving you full ownership and unlimited capacity.

## Technical Details

- **Single HTML file** — No build tools, no dependencies, no installation
- **File System Access API** — Direct read/write to local folders
- **IndexedDB** — Persists the folder handle across sessions (one-click reconnect)
- **Pure vanilla JS** — No frameworks, no bundlers
- **Dark theme UI** — Designed for comfortable long-session browsing

## License

[Apache License 2.0](LICENSE)

## Contributing

Issues and pull requests are welcome! If you have feature ideas or find bugs, feel free to open an issue.

---

# SD Prompt Gallery（中文说明）

一个轻量级的单文件本地网页应用，用于管理 Stable Diffusion 的提示词（Prompt）及其对应的生成图片。所有数据以真实文件的形式保存在你的磁盘上 —— 无需联网、无需服务器、无需数据库。

## 功能特性

- **提示词与图片配对** — 将提示词与生成的图片关联存储，方便随时查阅
- **负面提示词与备注** — 记录负面提示词、模型名称、采样器、CFG Scale、分辨率等所有生成参数
- **标签系统** — 使用自定义标签（如：人物、风景、二次元）对记录进行分类和快速筛选
- **全文搜索** — 在标题、提示词、标签和备注中即时搜索
- **灯箱预览** — 点击任意图片可全屏查看，并显示完整提示词信息
- **一键复制** — 一键将提示词复制到剪贴板，直接粘贴到 Stable Diffusion 中使用
- **本地文件夹存储** — 图片和元数据以真实文件保存在你选择的文件夹中，而非浏览器存储
- **无损保存** — 原始图片文件完整保留，不做任何压缩
- **持久化访问** — 应用会记住你选择的文件夹，下次打开只需点一下即可恢复

## 存储结构

```
你选择的文件夹/
└── sd_gallery_data/
    ├── index.json        ← 所有提示词元数据（标题、提示词、标签、备注等）
    └── images/           ← 图片原文件
        ├── e1a2b3c.jpg
        ├── e4d5e6f.png
        └── ...
```

应用使用 **File System Access API** 直接读写本地磁盘文件，这意味着：

- 清除浏览器缓存、重装浏览器甚至重装系统都不会丢失数据（只要文件夹还在）
- 可以使用任何文件同步工具备份或同步（OneDrive、Dropbox、坚果云等）
- 没有容量限制 —— 磁盘多大就能存多少

## 快速开始

1. 下载 `SD Prompt Gallery.html` 文件
2. 使用 **Chrome** 或 **Edge** 浏览器打开
3. 首次打开时选择一个本地文件夹用于存储数据
4. 开始添加提示词和图片！

> **注意：** 由于 Firefox 和 Safari 不支持 File System Access API，请使用 Chrome 或 Edge。

## 浏览器兼容性

| 浏览器  | 支持情况     |
|---------|-------------|
| Chrome  | ✅ 完全支持   |
| Edge    | ✅ 完全支持   |
| Firefox | ❌ 不支持     |
| Safari  | ❌ 不支持     |

## 为什么不用 localStorage？

早期版本使用 `localStorage` 存储数据，但它有约 5-10MB 的容量上限，且清除浏览器数据时会一并丢失。当前版本将所有数据以真实文件保存到磁盘，容量无限且数据完全由你掌控。

## 技术细节

- **单 HTML 文件** — 无需构建工具、无依赖、无需安装
- **File System Access API** — 直接读写本地文件夹
- **IndexedDB** — 持久化保存文件夹句柄（下次打开一键恢复）
- **纯原生 JavaScript** — 无框架、无打包工具
- **暗色主题 UI** — 适合长时间浏览的舒适界面

## 开源协议

[Apache License 2.0](LICENSE)

## 参与贡献

欢迎提交 Issue 和 Pull Request！如果你有功能建议或发现 Bug，请随时提出。
