# VKT SnapOCR — 截图取字（本地 OCR）

[English](../README.md) | 中文 | [Español](README_es.md) | [Deutsch](README_de.md) | [日本語](README_ja.md) | [Français](README_fr.md)

框选网页任意区域，一键提取图中文字。OCR **100% 在本机完成**（Tesseract.js WASM），截图永不上传、无需注册登录。

> Chrome / Edge / Firefox · Manifest V3 · 无追踪、不收集数据

## 为什么选 SnapOCR

- **真正隐私**：识别全程本地完成，任何内容都不上传。
- **离线可用**：英文、简体中文语言包内置。另外 7 种语言属 Pro，下载一次后离线可用。
- **权限最小化**：不申请常驻 `<all_urls>` 权限——仅在你发起识别时注入选区层（activeTab）。
- **实用不花哨**：框选 → 识别 → 复制，就这三步。

## 功能

- **框选识别**：右键菜单或工具栏按钮发起，拖拽框选 → 结果窗口出现文字。
- **结果可编辑**：复制前可先修正识别小误差。
- **识别历史**：免费版保留最近 10 条；Pro 版 200 条。
- **导出 TXT**（Pro）。
- **界面语言**：简体中文 / English / 日本語 / Deutsch / Español / Français。

## 免费版 vs Pro

| 功能 | Free | Pro（$14.99 终身） |
| --- | --- | --- |
| 每日识别次数 | 每天 20 次，零点重置 | 无限制 |
| 离线识别（英/简中） | ✅ | ✅ |
| 另外 7 种语言（繁中/日/韩/俄/法/德/西） | — | ✅ |
| 识别历史 | 最近 10 条 | 200 条 |
| 导出 TXT | — | ✅ |

购买与授权管理：<https://annmax1983.com>

## 权限说明

| 权限 | 用途 |
| --- | --- |
| `activeTab` + `scripting` | 仅在你发起识别时向当前标签页注入选区层 |
| `contextMenus` | 右键菜单「SnapOCR：提取选区文字」 |
| `storage` / `unlimitedStorage` | 设置、历史记录、语言包缓存 |
| `clipboardWrite` | 复制识别结果 |
| 主机权限 `api.annmax1983.com` | 仅用于 Pro 授权激活/校验 |

## 隐私

- 截图与识别全程不离开浏览器。
- 网络请求仅限：非内置语言包的一次性下载、Pro 用户的授权校验。

## 源码说明

> ⚠️ **本仓库仅用于项目展示，不发布完整源码。** 这里只有扩展的使用说明、更新日志与支持信息。

> 📥 **请前往官方浏览器商店下载安装：** Chrome Web Store · Microsoft Edge Add-ons · Firefox 附加组件（AMO）。本仓库不提供离线安装包，也不向终端用户分发源码包。

---

## 许可证

Copyright © 2026 VKT SnapOCR. All rights reserved.

本软件为闭源专有软件。未经作者书面授权，严禁反编译、逆向工程、破解、修改、重新打包、再分发或转售本软件（含全部或部分）。

---

## 联系

- 官网：<https://www.annmax1983.com/extensions/snapocr>
- 支持作者：<https://ko-fi.com/annmax?ref=snapocr>
- 问题反馈：<mailto:support@annmax1983.com>
