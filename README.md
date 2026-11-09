# VKT SnapOCR — Screenshot to Text (Local OCR)

[English](README.md) | [中文](languages/README_zh.md) | [Español](languages/README_es.md) | [Deutsch](languages/README_de.md) | [日本語](languages/README_ja.md) | [Français](languages/README_fr.md)

Select any area of a webpage and extract the text in it with one click. OCR runs **100% on your device** (Tesseract.js WASM) — screenshots never leave your machine, no sign-up, no upload.

> Chrome / Edge / Firefox · Manifest V3 · No tracking, no data collection

## Why SnapOCR

- **Truly private**: all recognition happens locally. Nothing is uploaded, ever.
- **Works offline**: English & Simplified Chinese language packs are bundled. Pro adds 7 more languages that download once, then work offline.
- **Minimal permissions**: no permanent `<all_urls>` access — the selection overlay is injected only when you invoke it (activeTab).
- **Practical, no bloat**: select → recognize → copy. That's the whole product.

## Features

- **Area OCR**: right-click menu or toolbar button → drag to select → text lands in the result window.
- **Editable result**: fix OCR slips inline before copying.
- **Recognition history**: Free keeps the latest 10 records; Pro keeps 200.
- **TXT export** (Pro).
- **UI languages**: English / 简体中文 / 日本語 / Deutsch / Español / Français.

## Free vs Pro

| Feature | Free | Pro ($14.99 lifetime) |
| --- | --- | --- |
| Daily captures | 20 / day, resets at midnight | Unlimited |
| Offline recognition (EN / 简体中文) | ✅ | ✅ |
| 7 more languages (繁中/日/韩/俄/法/德/西) | — | ✅ |
| Recognition history | last 10 | 200 |
| TXT export | — | ✅ |

Purchase & license management: <https://annmax1983.com>

## Permissions

| Permission | Why |
| --- | --- |
| `activeTab` + `scripting` | Inject the selection overlay into the current tab when you invoke SnapOCR |
| `contextMenus` | "SnapOCR: Extract text from selection" menu entry |
| `storage` / `unlimitedStorage` | Settings, history, cached language packs |
| `clipboardWrite` | Copy recognized text |
| Host: `api.annmax1983.com` | License activation/validation only (Pro users) |

## Privacy

- Screenshots and recognition never leave your browser.
- Network requests are limited to: one-time download of the 7 Pro language packs, and license validation for Pro users.

## Supported Browsers

| Browser | Status | Notes |
|---------|--------|-------|
| Google Chrome | ✅ Fully supported | Manifest V3 |
| Microsoft Edge | ✅ Fully supported | Manifest V3 |
| Mozilla Firefox | ✅ Fully supported | Manifest V3, Firefox 121+ (desktop) |
| Any Chromium-based browser (Brave, Opera, Vivaldi…) | ✅ Supported | Manifest V3 |

> **Firefox differences:**
> - SnapOCR uses no Chrome-only permissions — `activeTab`, `contextMenus`, `storage`, `unlimitedStorage`, `scripting`, `clipboardWrite` and the licence host all work on Firefox, so recognition, history, TXT export and the licence behave exactly as on Chrome and Edge.
> - The Firefox build keeps a persistent `background.scripts` page instead of the Chromium `service_worker`, and adds `browser_specific_settings.gecko` for AMO.
> - Everything else — area selection, editable result, one-click copy, bundled language packs, Free quota and Pro features — is identical across browsers.

---

## Source Code Notice

> ⚠️ **This repository is for project showcase only — the full source code is not published here.** It contains the user documentation, release notes and support information for the extension.

> 📥 **Download and install only from the official browser stores:** Chrome Web Store · Microsoft Edge Add-ons · Firefox Add-ons (AMO). No offline installation package is distributed from this repository.

---

## License

Copyright © 2026 VKT SnapOCR. All rights reserved.

This software is proprietary and closed-source. Without prior written authorization from the author, decompiling, reverse-engineering, cracking, modifying, repackaging, redistributing or reselling the program (in whole or in part) is strictly prohibited.

---

## Contact

- Official website: <https://www.annmax1983.com/extensions/snapocr>
- Support the author: <https://ko-fi.com/annmax?ref=snapocr>
- Issues & feedback: <mailto:support@annmax1983.com>
