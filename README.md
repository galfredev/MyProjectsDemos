# GalfreDev — Portfolio de Proyectos

[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-^5-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind-^3-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Vitest](https://img.shields.io/badge/Tests-Vitest-6E9F18?logo=vitest&logoColor=white)](https://vitest.dev/)
[![Playwright](https://img.shields.io/badge/E2E-Playwright-2EAD33?logo=microsoft-playwright&logoColor=white)](https://playwright.dev/)
[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-222?logo=github)](https://pages.github.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](#licencia)

> Creación de proyectos de dificultad variada con su respectiva demostración y explicación.  
> Objetivo: mostrar variedad técnica, buenas prácticas y un look minimalista (a mi estilo).

---

## 🗂️ Índice
- [Proyectos](#-proyectos)
- [Detalles y checklist por proyecto](#-detalles-y-checklist-por-proyecto)
- [Stack, convenciones y estructura](#-stack-convenciones-y-estructura)
- [Cómo correr cualquier proyecto localmente](#-cómo-correr-cualquier-proyecto-localmente)
- [Atribución](#-atribución)
- [Licencia](#licencia)

---

## 🚀 Proyectos

> Convención de nombres de repos: `galfredev-<slug>`.  
> Los links de **Demo** asumen GitHub Pages en `<usuario>.github.io/<repo>`.

| # | Proyecto | Categoría | Dificultad | Demo | Código | Highlights |
|---|---|---|---|---|---|---|
| 01 | Blurry Loading | UI/Animación | ⭐ | https://galfredev.github.io/galfredev-blurry-loading/ | https://github.com/GalfreDev/galfredev-blurry-loading | Timing/FPS, `prefers-reduced-motion` |
| 02 | Custom Range Slider | Componentes/UX | ⭐ | https://galfredev.github.io/galfredev-range-slider/ | https://github.com/GalfreDev/galfredev-range-slider | Estilo accesible de input nativo |
| 03 | Expanding Cards | UI/Animación | ⭐⭐ | https://galfredev.github.io/galfredev-expanding-cards/ | https://github.com/GalfreDev/galfredev-expanding-cards | Teclado/ARIA, dark mode, tests |
| 04 | Scroll Animation | UI/Animación | ⭐⭐ | https://galfredev.github.io/galfredev-scroll-animation/ | https://github.com/GalfreDev/galfredev-scroll-animation | IntersectionObserver, rendimiento |
| 05 | Rotating Navigation | UI/Animación | ⭐⭐ | https://galfredev.github.io/galfredev-rotating-navigation/ | https://github.com/GalfreDev/galfredev-rotating-navigation | Micro-interacciones, orden de foco |
| 06 | Toast Notification | Componentes/UX | ⭐⭐ | https://galfredev.github.io/galfredev-toast/ | https://github.com/GalfreDev/galfredev-toast | Colas, variantes, `aria-live` |
| 07 | Live User Filter | Datos/Estado | ⭐⭐ | https://galfredev.github.io/galfredev-live-filter/ | https://github.com/GalfreDev/galfredev-live-filter | Debounce, “no results” accesible |
| 08 | Password Generator | Componentes/UX | ⭐⭐⭐ | https://galfredev.github.io/galfredev-password-generator/ | https://github.com/GalfreDev/galfredev-password-generator | Entropía/medidor, copy seguro |
| 09 | Drag & Drop | Componentes/UX | ⭐⭐⭐ | https://galfredev.github.io/galfredev-drag-drop/ | https://github.com/GalfreDev/galfredev-drag-drop | DnD con teclado (roving tabindex) |
| 10 | **Drawing App (Canvas)** | UI/Canvas | ⭐⭐⭐ | https://galfredev.github.io/galfredev-drawing-app/ | https://github.com/GalfreDev/galfredev-drawing-app | **HTML Canvas**, presión/anchos, **undo/redo**, export PNG |
| 11 | Notes App | Datos/Estado | ⭐⭐⭐ | https://galfredev.github.io/galfredev-notes/ | https://github.com/GalfreDev/galfredev-notes | CRUD localStorage, export/import |
| 12 | Verify Account UI (OTP) | Componentes/UX | ⭐⭐⭐ | https://galfredev.github.io/galfredev-verify-otp/ | https://github.com/GalfreDev/galfredev-verify-otp | Auto-advance, paste múltiple, validación |
| 13 | GitHub Profiles | Datos/APIs | ⭐⭐⭐⭐ | https://galfredev.github.io/galfredev-github-profiles/ | https://github.com/GalfreDev/galfredev-github-profiles | Rate limiting, cache, skeletons |
| 14 | Movie App | Datos/APIs | ⭐⭐⭐⭐ | https://galfredev.github.io/galfredev-movie-app/ | https://github.com/GalfreDev/galfredev-movie-app | Paginación, estados, e2e |
| 15 | Pokedex | Datos/APIs | ⭐⭐⭐⭐ | https://galfredev.github.io/galfredev-pokedex/ | https://github.com/GalfreDev/galfredev-pokedex | PokeAPI, imágenes, cache/filters |

---

## 🧱 Stack, convenciones y estructura

**Tecnologías**
- **Core:** Vite + **TypeScript**, **TailwindCSS**
- **Calidad:** ESLint, Prettier, Husky + lint-staged (opcional)
- **Testing:** Vitest + @testing-library/dom (+ **Playwright** en apps con API)
- **A11y:** axe (vía Playwright) y chequeos manuales
- **CI/CD:** GitHub Actions → build + deploy a Pages

**Convenciones**
- Prefijo de repos: `galfredev-…`
- Commits: Conventional Commits (ej. `feat(ui): add keyboard nav`)
- Versionado: semver básico si corresponde

**Sugerencia de estructura (por repo)**
```
├─ public/
├─ src/
│  ├─ assets/
│  ├─ lib/            # utils
│  ├─ components/
│  ├─ styles/
│  └─ main.ts
├─ tests/             # unit
├─ e2e/               # playwright (si aplica)
├─ index.html
├─ package.json
├─ tsconfig.json
├─ tailwind.config.cjs
├─ .eslintrc.cjs
└─ .github/workflows/pages.yml
```

---

## 🧪 Cómo correr cualquier proyecto localmente

```bash
git clone https://github.com/GalfreDev/<repo>
cd <repo>
pnpm i
pnpm dev
```

> Requiere **Node 20+** y **pnpm** (o npm/yarn adaptando scripts).

---

## Licencia

Este repo y los proyectos asociados se publican bajo **MIT**.  
© Valentino Galfré (GalfreDev). Ver [LICENSE](./LICENSE).
