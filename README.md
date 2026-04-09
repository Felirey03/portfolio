<h1 align="center">
  👨‍💻 Felipe Reynoso – Developer Portfolio
</h1>

<p align="center">
  Plataforma estática, repositorio de proyectos y blog central para mis operaciones continuas en el mundo del desarrollo de software (Backend, Python y Odoo Integration).
</p>

<p align="center">
  <a href="https://www.felipereynoso.site/"><b>🌐 Ver el sitio en producción</b></a>
</p>

---

## 🧱 Arquitectura y Mentalidad Técnica

Lejos de instalar plantillas estandarizadas o sistemas masivos, este proyecto fue creado desde sus cimientos y optimizado minuciosamente buscando tres pilares esenciales: **minimalismo**, **cero fricción al escalar** y **rendimiento superlativo (SSG)**.

Este repositorio no aloja simplemente "una landing page estática"; funciona como **su propia base de datos** empleando de forma íntegra `Content Collections` validadas lógicamente bajo esquemas de integridad de datos (`Zod`).

## 🛠️ Stack y Tecnologías Empleadas

- **Astro (`astro.build`)**: Motor y Generador Estático de Sitios.
- **TypeScript y Zod (`z`)**: Asegurando validación férrea (Type-Safety) en todo el ecosistema de *frontmatter* en tiempo de compilación para eludir completamente los fallos de inyección *runtime*.
- **Arquitectura de Base de Datos Base**: Markdown puro (Separación limpia del CMS entre `/blog/` y `/projects/`).
- **Interfaces Fluidas**: CSS Variable (`:root`) Vanilla CSS implementando Responsive Layout y patrones estables de UI. 

## 🚀 Despliegue Local (Run it yourself)

El proyecto recae sobre dependencias livianas de Node (NPM). Para levantar la instancia productiva de prueba de red local en tu computadora:

1. Clona este repositorio
```bash
git clone https://github.com/Felirey03/portfolio.git
cd portfolio
```
2. Instala dependencias del paquete
```bash
npm install
```
3. Levanta el servidor local de desarrollo
```bash
npm run dev
```

El servidor local normalmente correrá sobre la dirección por defecto del puerto 4321, accesible en entorno puro: `http://localhost:4321/`

---

> El código es Open Source y se encuentra disponible bajo licencia. Si eres técnico informático o reclutador de Sistemas, siéntete libre de husmear en el árbol de *Layouts* y la estructura modular `[...id].astro` del enrutador dinámico. 📂.
