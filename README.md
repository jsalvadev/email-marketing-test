# Prueba Técnica – Email Developer  
**Vueling Club · Destinos de verano**

---

## Planteamiento

Estructura basada en tablas anidadas con estilos inline, estándar de compatibilidad en email HTML. Layout organizado en módulos independientes y comentados (header, hero, módulos de contenido y footer), con contenedor fijo de 600px para desktop.

Tipografía **Akshar (Google Fonts)** con fallback a Arial/Helvetica.

Se validó el HTML en https://validator.w3.org/ para asegurar el correcto cierre de etiquetas y estructura semántica válida.

---

## Técnica responsive

Primero se desarrolló la versión desktop y posteriormente se implementaron media queries con clases utilitarias para mobile.

- Breakpoint principal en `620px`
- Columnas apiladas con `display: block`
- Imágenes al `width: 100%` en mobile
- Header adaptado en versión móvil
- Hero y módulo Endesa con imágenes distintas para desktop y mobile (no solo redimensionadas, sino adaptadas)

---

## Issues de compatibilidad encontrados y corregidos

Testeado con **Testi.at**

- **Fondos en clientes legacy** → uso de `bgcolor` como fallback además del `background-color` inline
- **Imágenes cortadas en Outlook** → eliminado `line-height` en `<td>` contenedores
- **Gaps entre imágenes** → `display: block` en `<img>`
- **Gmail y @import** → movido al final del `<style>`
- **CTAs rotos en Outlook** → patrón bulletproof button (background y padding en `<td>`)
- **Fallback de imágenes en desarrollo** → `onerror` apuntando a placehold.co

---

## Screenshots

### Testi.at – Desktop
![Testi.at Desktop](./screenshots/testi.at%20(desktop).png)

### Testi.at – Mobile
![Testi.at Mobile](./screenshots/testi.at%20(mobile).png)

### Web – Desktop
![Web Desktop](./screenshots/web%20(desktop).png)

### Web – Mobile
![Web Mobile](./screenshots/web%20(mobile).png)

---

## Qué mejoraría con más tiempo

- Subir imágenes a CDN y eliminar fallbacks de desarrollo
- Soporte para dark mode
- Testing en más clientes (Outlook desktop, Apple Mail, Yahoo, etc.)
- Añadir UTMs en todos los CTAs para tracking
- Optimización adicional de imágenes (<200kb).  
  Herramienta habitual: https://squoosh.app/

---

*Desarrollado por Salvador Jesús · 03/2026*
