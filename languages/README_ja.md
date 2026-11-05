# VKT SnapOCR — スクリーンショットからテキスト抽出（ローカル OCR）

[English](../README.md) | [中文](README_zh.md) | [Español](README_es.md) | [Deutsch](README_de.md) | 日本語 | [Français](README_fr.md)

Webページの好きな範囲をドラッグして、ワンクリックでテキストを抽出。OCR は**100% 端末内で処理**（Tesseract.js WASM）され、スクリーンショットが外に出ることはありません。登録不要。

> Chrome / Edge / Firefox · Manifest V3 · トラッキングなし・データ収集なし

## SnapOCR が選ばれる理由

- **本当のプライバシー**：認識はすべてローカル処理。何もアップロードしません。
- **オフライン対応**：英語と簡体字中国語の言語パックを同梱。残り 7 言語は Pro の機能で、初回ダウンロード後オフラインで利用可能。
- **最小権限**：常駐の `<all_urls>` 権限なし。起動時だけ選択オーバーレイを注入（activeTab）。
- **無駄のない設計**：選択 → 認識 → コピー。これだけです。

## 機能

- **範囲 OCR**：右クリックメニュー、またはツールバーボタンで開始。
- **結果は編集可能**：コピー前にその場で修正できます。
- **認識履歴**：無料版は直近 10 件、Pro 版は 200 件。
- **TXT 書き出し**（Pro）。
- **UI 言語**：日本語 / English / 简体中文 / Deutsch / Español / Français。

## 無料版 vs Pro

| 機能 | Free | Pro（$14.99 買い切り） |
| --- | --- | --- |
| 1 日の認識回数 | 1 日 20 回（0 時にリセット） | 無制限 |
| オフライン認識（英/簡体字中国語） | ✅ | ✅ |
| 残り 7 言語（繁中/日/韓/露/仏/独/西） | — | ✅ |
| 認識履歴 | 直近 10 件 | 200 件 |
| TXT 書き出し | — | ✅ |

購入・ライセンス管理：<https://annmax1983.com>

## 権限について

| 権限 | 用途 |
| --- | --- |
| `activeTab` + `scripting` | 起動時に現在のタブへ選択オーバーレイを注入 |
| `contextMenus` | 右クリックメニュー項目 |
| `storage` / `unlimitedStorage` | 設定・履歴・言語パックのキャッシュ |
| `clipboardWrite` | 認識結果のコピー |
| ホスト権限 `api.annmax1983.com` | Pro ライセンスの認証のみ |

## プライバシー

- スクリーンショットと認識処理はブラウザの外に出ません。
- 通信は同梱外言語パックの初回ダウンロードと Pro ユーザーのライセンス検証のみ。

## 開発

```powershell
npm install
npm run build      # publish/ を生成
```

Chrome / Edge での読み込み：`chrome://extensions` → デベロッパーモード → 「パッケージ化されていない拡張機能を読み込む」→ `publish/` を選択。

ストア用パッケージ：`Compress-Archive -Path publish/* -DestinationPath snapocr.zip -Force`

Firefox ビルドは別リポジトリで保守しています（`background.scripts` + `browser_specific_settings.gecko`）。

## お問い合わせ

- 公式サイト：<https://www.annmax1983.com/extensions/snapocr>
- 作者を支援：<https://ko-fi.com/annmax?ref=snapocr>
- フィードバック：<mailto:support@annmax1983.com>
