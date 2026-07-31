# alex.dev — Portfolio personal

Portfolio personal de Alejandro Yero, Ingeniero en Ciencias Informáticas con enfoque full-stack y particular afinidad por el frontend. Construido con [Astro](https://astro.build) y [Tailwind CSS](https://tailwindcss.com), con animaciones sutiles de [Framer Motion](https://www.framer.com/motion/).

## Características

- **Diseño responsive** — Adaptado a todos los dispositivos
- **Modo oscuro/claridad** — Toggle con persistencia en `localStorage` y detección de preferencia del sistema
- **Animaciones de reveals** — Entradas escalonadas con `IntersectionObserver`, respetuoso con `prefers-reduced-motion`
- **Sin JavaScript cliente** — El DOM se renderiza en el servidor; el JS es solo para interacciones decorativas

## Tecnologías

| Categoría      | Tecnología          |
| -------------- | ------------------- |
| Framework      | Astro 5             |
| Estilos        | Tailwind CSS 4      |
| Animaciones    | Framer Motion       |
| Tipado         | TypeScript          |
| Utils          | clsx + tailwind-merge |

## Estructura del proyecto

```text
public/              # Assets estáticos (favicon, imágenes de proyectos, CV)
src/
├── components/      # Componentes UI reutilizables (Hero, About, Skills, Experience, Projects)
├── icons/           # Iconos SVG como componentes Astro
├── layouts/         # Layout de página (Header, Footer, Main)
├── lib/             # Utilidades (cn para merge de clases)
├── pages/           # Rutas (index.astro)
└── styles/          # CSS global (Tailwind directives)
```

Los alias `@components/*`, `@layouts/*` e `@icons/*` están configurados en `tsconfig.json` y funcionan gracias al plugin de TypeScript de Astro.

## Comandos

Desde la raíz del proyecto:

| Comando            | Acción                                      |
| :----------------- | :------------------------------------------ |
| `pnpm dev`         | Inicia el servidor de desarrollo en `localhost:4321` |
| `pnpm build`       | Genera el sitio estático en `./dist/`       |
| `pnpm preview`     | Previsualiza el build localmente            |

## Desarrollo

```sh
# 1. Clona el repositorio
git clone <url-del-repo>
cd portfolio-dev

# 2. Instala dependencias
pnpm install

# 3. Inicia el servidor de desarrollo
pnpm dev
```

Abre [http://localhost:4321](http://localhost:4321) para ver el resultado.

## Deployment

El sitio está listo para desplegarse como sitio estático en cualquier host (Vercel, Netlify, Cloudflare Pages, etc.). Astro genera HTML estático por defecto.

```sh
pnpm build
```
