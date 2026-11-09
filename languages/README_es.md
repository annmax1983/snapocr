# VKT SnapOCR — Captura a texto (OCR local)

[English](../README.md) | [中文](README_zh.md) | Español | [Deutsch](README_de.md) | [日本語](README_ja.md) | [Français](README_fr.md)

Selecciona cualquier zona de una página web y extrae el texto con un clic. El OCR se ejecuta **100% en tu dispositivo** (Tesseract.js WASM): las capturas nunca salen de tu equipo. Sin registro ni subidas.

> Chrome / Edge / Firefox · Manifest V3 · Sin rastreo ni recogida de datos

## Por qué SnapOCR

- **Privacidad real**: todo el reconocimiento ocurre en local. Nunca se sube nada.
- **Funciona sin conexión**: los paquetes de inglés y chino simplificado van incluidos. Los otros 7 idiomas son parte de Pro: se descargan una vez y luego funcionan offline.
- **Permisos mínimos**: sin acceso permanente a `<all_urls>`: la capa de selección solo se inyecta al invocarla (activeTab).
- **Práctico, sin relleno**: seleccionar → reconocer → copiar. Eso es todo.

## Funciones

- **OCR por áreas**: menú contextual o botón de la barra → arrastra para seleccionar → ventana de resultado.
- **Resultado editable**: corrige pequeños errores del OCR antes de copiar.
- **Historial**: la versión gratuita guarda los últimos 10 registros; Pro guarda 200.
- **Exportación TXT** (Pro).
- **Idiomas de interfaz**: Español / English / 简体中文 / 日本語 / Deutsch / Français.

## Gratis vs Pro

| Función | Free | Pro ($14.99 de por vida) |
| --- | --- | --- |
| Capturas por día | 20 al día, se reinicia a medianoche | Ilimitadas |
| Reconocimiento sin conexión (EN / 简体中文) | ✅ | ✅ |
| Los otros 7 idiomas (繁中/JA/KO/RU/FR/DE/ES) | — | ✅ |
| Historial | últimos 10 | 200 |
| Exportación TXT | — | ✅ |

Compra y gestión de licencias: <https://annmax1983.com>

## Permisos

| Permiso | Uso |
| --- | --- |
| `activeTab` + `scripting` | Inyectar la capa de selección solo al invocar SnapOCR |
| `contextMenus` | Entrada del menú contextual |
| `storage` / `unlimitedStorage` | Ajustes, historial, caché de paquetes de idioma |
| `clipboardWrite` | Copiar el texto reconocido |
| Host `api.annmax1983.com` | Solo activación/validación de licencia (Pro) |

## Privacidad

- Las capturas y el reconocimiento nunca salen del navegador.
- Las solicitudes de red se limitan a la descarga única de paquetes de idioma no incluidos y a la validación de licencia de usuarios Pro.

## Aviso sobre el código fuente

> ⚠️ **Este repositorio es solo para presentar el proyecto: el código fuente completo no se publica aquí.** Solo contiene la documentación de uso, las notas de versión y la información de soporte de la extensión.

> 📥 **Descárgala e instálala únicamente desde las tiendas oficiales de navegadores:** Chrome Web Store · Microsoft Edge Add-ons · Complementos de Firefox (AMO). Desde aquí no se distribuye ningún instalador sin conexión.

---

## Licencia

Copyright © 2026 VKT SnapOCR. All rights reserved.

Este software es propietario y de código cerrado. Sin autorización previa por escrito del autor, queda estrictamente prohibido descompilar, aplicar ingeniería inversa, crackear, modificar, reempaquetar, redistribuir o revender el programa (total o parcialmente).

---

## Contacto

- Sitio web oficial: <https://www.annmax1983.com/extensions/snapocr>
- Apoyar al autor: <https://ko-fi.com/annmax?ref=snapocr>
- Comentarios: <mailto:support@annmax1983.com>
