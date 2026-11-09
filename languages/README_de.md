# VKT SnapOCR — Screenshot zu Text (lokale OCR)

[English](../README.md) | [中文](README_zh.md) | [Español](README_es.md) | Deutsch | [日本語](README_ja.md) | [Français](README_fr.md)

Markieren Sie einen beliebigen Bereich einer Webseite und extrahieren Sie den Text mit einem Klick. Die OCR läuft **100 % auf Ihrem Gerät** (Tesseract.js WASM) — Screenshots verlassen niemals Ihren Rechner. Keine Anmeldung, kein Upload.

> Chrome / Edge / Firefox · Manifest V3 · Kein Tracking, keine Datenerfassung

## Warum SnapOCR

- **Wirklich privat**: Die gesamte Erkennung läuft lokal. Es wird nichts hochgeladen.
- **Offline nutzbar**: Englisch- und Chinesisch-Sprachpakete sind enthalten. Die 7 weiteren Sprachen sind Teil von Pro — einmal geladen, laufen sie offline.
- **Minimale Berechtigungen**: Kein dauerhafter `<all_urls>`-Zugriff — das Auswahl-Overlay wird nur bei Bedarf injiziert (activeTab).
- **Praktisch ohne Ballast**: Auswählen → Erkennen → Kopieren. Das ist alles.

## Funktionen

- **Bereichs-OCR**: Rechtsklick-Menü oder Symbolleisten-Button → Bereich ziehen → Ergebnisfenster.
- **Ergebnis bearbeitbar**: Kleinere OCR-Fehler vor dem Kopieren direkt korrigieren.
- **Erkennungsverlauf**: Kostenlos die letzten 10 Einträge; Pro 200 Einträge.
- **TXT-Export** (Pro).
- **Oberflächensprachen**: Deutsch / English / 简体中文 / 日本語 / Español / Français.

## Kostenlos vs Pro

| Funktion | Free | Pro ($14.99 lebenslang) |
| --- | --- | --- |
| Aufnahmen pro Tag | 20/Tag, Reset um Mitternacht | Unbegrenzt |
| Offline-Erkennung (EN / 简体中文) | ✅ | ✅ |
| 7 weitere Sprachen (繁中/JP/KR/RU/FR/DE/ES) | — | ✅ |
| Erkennungsverlauf | letzte 10 | 200 |
| TXT-Export | — | ✅ |

Kauf & Lizenzverwaltung: <https://annmax1983.com>

## Berechtigungen

| Berechtigung | Zweck |
| --- | --- |
| `activeTab` + `scripting` | Auswahl-Overlay nur bei Bedarf in den aktuellen Tab injizieren |
| `contextMenus` | Kontextmenü-Eintrag |
| `storage` / `unlimitedStorage` | Einstellungen, Verlauf, Sprachpaket-Cache |
| `clipboardWrite` | Erkannten Text kopieren |
| Host `api.annmax1983.com` | Nur Lizenzaktivierung/-prüfung (Pro) |

## Datenschutz

- Screenshots und Erkennung verlassen den Browser nie.
- Netzwerkanfragen beschränken sich auf den einmaligen Download nicht enthaltener Sprachpakete und die Lizenzprüfung für Pro-Nutzer.

## Hinweis zum Quellcode

> ⚠️ **Dieses Repository dient ausschließlich der Projektpräsentation — der vollständige Quellcode wird hier nicht veröffentlicht.** Es enthält nur die Nutzungsdokumentation, die Release-Notizen und Support-Informationen zur Erweiterung.

> 📥 **Installation ausschließlich über die offiziellen Browser-Stores:** Chrome Web Store · Microsoft Edge Add-ons · Firefox-Add-ons (AMO). Von hier werden keine Offline-Installer verteilt.

---

## Lizenz

Copyright © 2026 VKT SnapOCR. All rights reserved.

Diese Software ist proprietär und quellgeschlossen. Ohne vorherige schriftliche Genehmigung des Autors ist das Dekompilieren, Reverse-Engineering, Knacken, Verändern, Neuverpacken, Weiterverbreiten oder Weiterverkaufen der Software (ganz oder teilweise) streng untersagt.

---

## Kontakt

- Offizielle Website: <https://www.annmax1983.com/extensions/snapocr>
- Autor unterstützen: <https://ko-fi.com/annmax?ref=snapocr>
- Feedback: <mailto:support@annmax1983.com>
