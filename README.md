# jgalanm

Portafolio profesional de **Jorge Andrés Galán Mena** en inteligencia artificial aplicada, gestión del conocimiento y sistemas inteligentes.

**Sitio publicado:** <https://jgalanm07.github.io/jgalanm/>

## Estructura

- `index.html` — single-page completo (HTML + CSS embebido, sin dependencias más allá de Google Fonts).
- `assets/profile/` — retrato.
- `assets/projects/` — capturas de los cinco proyectos destacados.
- `.nojekyll` — desactiva el procesamiento Jekyll de GitHub Pages.

## Publicar

1. Push a `main` del repositorio `jgalanm07/jgalanm`.
2. En GitHub: **Settings → Pages → Source: Deploy from a branch → Branch `main` / Folder `/ (root)`**.
3. URL pública: <https://jgalanm07.github.io/jgalanm/> (tarda 1–2 min la primera vez).

## QA local

```powershell
# Servir el sitio sin abrir con file:// (rompe rutas relativas)
python -m http.server 8000
# Visitar http://localhost:8000

# Auditoría Lighthouse desde CLI
npx --yes lighthouse http://localhost:8000 --view
```

## Sistema de diseño

| Token | Valor |
|---|---|
| Fondo | `#ffffff` |
| Tinta | `#0d0d0e` |
| Acento | `#1c3d5a` (marino) |
| Display | Playfair Display |
| Cuerpo | Source Serif 4 |
| Mono | JetBrains Mono |

Para cambiar acento o tipografías, editar las variables CSS en `:root` (líneas iniciales de `<style>` en `index.html`).

## Origen del diseño

Maquetado en **Claude Design** (handoff bundle 2026-05-12) y portado a HTML estático listo para GitHub Pages. El bundle original y la conversación de diseño se conservan en `../../Sugerencias/` del workspace local.
