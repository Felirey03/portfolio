# Reglas y Estructura del Proyecto — Landing Page / Portfolio

Este archivo sirve como referencia estructural para cualquier agente que trabaje en este repositorio, evitando búsquedas de archivos repetitivas y optimizando el consumo de tokens de contexto.

---

## 🛠️ Stack Tecnológico
- **Framework**: Astro (Generación estática y SSR listo).
- **Estilos**: CSS Nativo / Vanilla CSS (`src/styles/global.css`).
- **Lógica**: JavaScript / TypeScript.
- **Gestor de Paquetes**: pnpm.

---

## 📁 Arquitectura de Directorios

### 📄 Páginas (`src/pages/`)
- [index.astro](file:///home/felipe/Documentos/landingpage/src/pages/index.astro): Página principal (Hero con Terminal, Proyectos destacados, posts recientes del Blog).
- [servicios.astro](file:///home/felipe/Documentos/landingpage/src/pages/servicios.astro): Página independiente de servicios técnicos (Bots y Agentes, Módulos Odoo, Apps Web, Soporte).
- `blog/`: Rutas dinámicas para la lectura de posts.
- `projects/`: Rutas dinámicas para la lectura de proyectos detallados.

### 🧩 Componentes (`src/components/`)
- [Services.astro](file:///home/felipe/Documentos/landingpage/src/components/Services.astro): Componente de servicios (usado para vistas incrustadas/secciones en home si es necesario). **Nota**: Mantener en sincronía con `servicios.astro`.
- [ProjectCard.astro](file:///home/felipe/Documentos/landingpage/src/components/ProjectCard.astro): Tarjeta reutilizable para proyectos.
- [TerminalHero.astro](file:///home/felipe/Documentos/landingpage/src/components/TerminalHero.astro): Bloque visual interactivo que simula una consola de comandos en la sección Home.
- [ImageGallery.astro](file:///home/felipe/Documentos/landingpage/src/components/ImageGallery.astro): Galería de imágenes para proyectos.

### 🍱 Layouts (`src/layouts/`)
- [BaseLayout.astro](file:///home/felipe/Documentos/landingpage/src/layouts/BaseLayout.astro): Layout global (Header, Footer, Script de control de Tema Dark/Light e importación de estilos globales).

### 💅 Estilos (`src/styles/`)
- [global.css](file:///home/felipe/Documentos/landingpage/src/styles/global.css): Archivo único de estilos CSS nativos. No se usa Tailwind CSS.

### ✍️ Contenido Coleccionado (`src/content/`)
- `blog/`: Archivos Markdown (.md) para artículos.
- `projects/`: Archivos Markdown (.md) para casos de estudio/proyectos del portafolio.
- [content.config.ts](file:///home/felipe/Documentos/landingpage/src/content.config.ts): Definición de los schemas de Astro Content Collections.

---

## 📝 Guías de Integración y Reglas

### 1. Modificación y Adición de Servicios
- **Sincronización**: Al editar o añadir un servicio, modificar SIEMPRE tanto la página [servicios.astro](file:///home/felipe/Documentos/landingpage/src/pages/servicios.astro) como el componente [Services.astro](file:///home/felipe/Documentos/landingpage/src/components/Services.astro).
- **Tarjetas en servicios.astro**: Usan los atributos `data-index="NN"` (ej. `data-index="01"`) y opcionalmente la clase `.featured` en el elemento `<article class="service-card">` para destacar visualmente.

### 2. Estilos CSS
- Todos los estilos deben ser añadidos o modificados en [global.css](file:///home/felipe/Documentos/landingpage/src/styles/global.css) utilizando variables de CSS (`var(--text)`, `var(--accent)`, `var(--bg)`, etc.) para asegurar el soporte correcto de temas claro/oscuro.
