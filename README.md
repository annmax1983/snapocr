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

## Development

```powershell
npm install
npm run build      # assembles publish/
```

Load in Chrome/Edge: `chrome://extensions` → Developer mode → Load unpacked → select `publish/`.

Package for the stores: `Compress-Archive -Path publish/* -DestinationPath snapocr.zip -Force`

Regenerate store screenshots (needs Chrome or Edge installed):

```powershell
powershell -ExecutionPolicy Bypass -File scripts/capture_screenshots.ps1
```

### Directory structure

```
SnapOCR/
├── manifest.json          # MV3
├── background.js          # Service worker: on-demand injection, capture, crop, result window
├── content.js / .css      # Selection overlay (injected on demand, no <all_urls>)
├── license.js             # Creem licence (shared annmax template)
├── popup/                 # Capture trigger, language, history, licence modal
├── result/                # OCR run + progress + edit/copy/export
├── _locales/              # 6 UI languages
├── icons/                 # Extension icons (scripts/make_icons.py)
├── assets/                # Shared footer link icons
├── index.html             # Product landing page
├── privacy-policy.html    # Privacy policy (EN / 中文)
├── promo.html             # 1400×560 store promo tile source
├── store-listing/         # Store copy: en / zh_CN / ja / de / es / fr
├── screenshots/           # 1280×800 store shots + 440×280 / 1400×560 promos
│   └── _src/              # HTML templates rendered by scripts/capture_screenshots.ps1
├── languages/             # Translated READMEs (zh / es / de / ja / fr)
└── scripts/
    ├── build.js           # Assemble publish/ (runtime + bundled language packs)
    ├── make_icons.py      # Stdlib-only icon generator
    └── capture_screenshots.ps1  # Headless Chrome renderer for store shots
```

A Firefox build (native `background.scripts` + `browser_specific_settings.gecko`) is maintained in a separate repository.

## Contact

- Official website: <https://www.annmax1983.com/extensions/snapocr>
- Support the author: <https://ko-fi.com/annmax?ref=snapocr>
- Issues & feedback: <mailto:support@annmax1983.com>
