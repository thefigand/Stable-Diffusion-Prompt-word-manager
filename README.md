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
