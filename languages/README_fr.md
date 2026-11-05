# VKT SnapOCR — Capture d'écran vers texte (OCR locale)

[English](../README.md) | [中文](README_zh.md) | [Español](README_es.md) | [Deutsch](README_de.md) | [日本語](README_ja.md) | Français

Sélectionnez n'importe quelle zone d'une page web et extrayez son texte en un clic. L'OCR s'exécute **100 % sur votre appareil** (Tesseract.js WASM) — les captures ne quittent jamais votre machine. Sans inscription ni téléversement.

> Chrome / Edge / Firefox · Manifest V3 · Sans pistage ni collecte de données

## Pourquoi SnapOCR

- **Confidentialité réelle** : toute la reconnaissance est locale. Rien n'est téléversé, jamais.
- **Fonctionne hors ligne** : les packs anglais et chinois simplifié sont inclus. Les 7 autres langues font partie de Pro — un téléchargement, puis elles fonctionnent hors ligne.
- **Permissions minimales** : pas d'accès permanent à `<all_urls>` — la couche de sélection n'est injectée qu'à la demande (activeTab).
- **Pratique, sans superflu** : sélectionner → reconnaître → copier. C'est tout.

## Fonctionnalités

- **OCR par zone** : menu contextuel ou bouton de la barre d'outils → glissez pour sélectionner → fenêtre de résultat.
- **Résultat modifiable** : corrigez les petites erreurs d'OCR avant de copier.
- **Historique** : la version gratuite conserve les 10 derniers enregistrements ; Pro en conserve 200.
- **Export TXT** (Pro).
- **Langues de l'interface** : Français / English / 简体中文 / 日本語 / Deutsch / Español.

## Gratuit vs Pro

| Fonctionnalité | Free | Pro ($14.99 à vie) |
| --- | --- | --- |
| Captures par jour | 20/jour, réinitialisation à minuit | Illimitées |
| Reconnaissance hors ligne (EN / 简体中文) | ✅ | ✅ |
| Les 7 autres langues (繁中/JA/KO/RU/FR/DE/ES) | — | ✅ |
| Historique | 10 derniers | 200 |
| Export TXT | — | ✅ |

Achat et gestion de licence : <https://annmax1983.com>

## Permissions

| Permission | Usage |
| --- | --- |
| `activeTab` + `scripting` | Injecter la couche de sélection dans l'onglet courant à la demande |
| `contextMenus` | Entrée de menu contextuel |
| `storage` / `unlimitedStorage` | Réglages, historique, cache des packs de langue |
| `clipboardWrite` | Copier le texte reconnu |
| Hôte `api.annmax1983.com` | Activation/validation de licence uniquement (Pro) |

## Confidentialité

- Les captures et la reconnaissance ne quittent jamais le navigateur.
- Les requêtes réseau se limitent au téléchargement unique des packs de langue non inclus et à la validation de licence pour les utilisateurs Pro.

## Développement

```powershell
npm install
npm run build      # génère publish/
```

Chargement dans Chrome/Edge : `chrome://extensions` → Mode développeur → « Charger l'extension non empaquetée » → sélectionner `publish/`.

Paquet pour les stores : `Compress-Archive -Path publish/* -DestinationPath snapocr.zip -Force`

La version Firefox est maintenue dans un dépôt séparé (`background.scripts` + `browser_specific_settings.gecko`).

## Contact

- Site officiel : <https://www.annmax1983.com/extensions/snapocr>
- Soutenir l'auteur : <https://ko-fi.com/annmax?ref=snapocr>
- Retours : <mailto:support@annmax1983.com>
