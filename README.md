# jgalanm

Portafolio profesional bilingüe de **Jorge Andrés Galán Mena** en inteligencia artificial aplicada, gestión del conocimiento y sistemas inteligentes.

**Sitio publicado:**
- EN (default) — <https://jgalanm07.github.io/jgalanm/>
- ES — <https://jgalanm07.github.io/jgalanm/es/>

## Estructura

- `index.html` — versión en inglés (default; incluye detección suave de idioma del navegador).
- `es/index.html` — versión en español.
- `assets/profile/` — retrato (compartido).
- `assets/projects/` — capturas de los cinco proyectos destacados.
- `assets/cv/cv.pdf` — currículum descargable desde el hero.
- `.nojekyll` — desactiva el procesamiento Jekyll de GitHub Pages.

Ambos archivos comparten los mismos `assets/`. Las rutas en `es/index.html` son `../assets/...`.

## i18n

- **Idioma por defecto:** inglés (raíz `/`).
- **Detección de navegador:** en la primera visita, si `navigator.language` empieza por `es` y no hay preferencia guardada, redirige a `/es/` con `location.replace` (no contamina el back button).
- **Persistencia:** `localStorage['jg-lang']` recuerda la elección manual. Hacer clic en el switcher la actualiza.
- **SEO:** `<link rel="alternate" hreflang>` cruzados (en, es, x-default). Cada página tiene `canonical` hacia sí misma.

## Publicar

1. Push a `main` del repositorio `jgalanm07/jgalanm`.
2. En GitHub: **Settings → Pages → Source: Deploy from a branch → Branch `main` / Folder `/ (root)`**.
3. URLs públicas:
   - EN: <https://jgalanm07.github.io/jgalanm/>
   - ES: <https://jgalanm07.github.io/jgalanm/es/>

## QA local

```powershell
# Servir el sitio sin abrir con file:// (rompe rutas relativas)
python -m http.server 8000
# Visitar:
#   http://localhost:8000/      → EN
#   http://localhost:8000/es/   → ES

# Auditoría Lighthouse desde CLI (correr en ambas URLs)
npx --yes lighthouse http://localhost:8000/ --view
npx --yes lighthouse http://localhost:8000/es/ --view
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

Para cambiar acento o tipografías, editar las variables CSS en `:root` de cada archivo (mismas en ambos).

## Origen del diseño

Maquetado en **Claude Design** (handoff bundle 2026-05-12) y portado a HTML estático listo para GitHub Pages. La traducción al inglés se produjo con un workflow multi-agente (3 traductores en paralelo con ángulos estilísticos distintos → síntesis → verificación adversarial → fix automático).
