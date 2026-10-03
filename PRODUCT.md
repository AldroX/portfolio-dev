# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

**Primary:** Reclutadores, hiring managers, y potenciales clientes que evalúan a Alejandro para oportunidades laborales o proyectos. Llegan al portafolio desde LinkedIn, GitHub, redes sociales, o postulaciones laborales.

**Secondary:** Colegas y pares de la industria que referencian o validan el perfil.

El usuario viene a decidir si Alejandro es la persona adecuada para un rol o proyecto. Su situación es de evaluación rápida: escanean en busca de señales de competencia técnica, calidad de trabajo, y ajuste cultural.

## Product Purpose

Un portafolio profesional personal que muestra quién es Alejandro, qué tecnologías domina, su experiencia y proyectos, y cómo contactarlo. El objetivo es convertir visitantes (reclutadores, clientes) en leads de contratación o colaboración.

El éxito se mide por: la tasa de visitantes que llegan al formulario de contacto, descargan el CV, o inician una conversación.

## Positioning

Un portafolio que se siente como un producto — no como una página estática. Donde otros portfolios son currículums con HTML, este es una experiencia de marca personal con animaciones de nivel, diseño cuidado, y ejecución que demuestra las capacidades técnicas que anuncia. Es la prueba viva de lo que Alejandro sabe hacer.

## Operating Context

- El sitio se visualiza en desktop y mobile (responsive)
- El visitante típicamente llega con poco tiempo y escanea visualmente antes de leer
- Se accede desde el navegador, sin necesidad de login o cuenta
- El CV descargable es un PDF
- Los links a GitHub, LinkedIn, y redes sociales son la ruta de validación secundaria
- El modo oscuro/claro está disponible y persiste entre visitas

## Capabilities and Constraints

### Confirmado
- Landing page tipo portafolio con secciones: Hero/Sobre mí, Skills/Tecnologías, Experiencia/Proyectos, Proyectos Personales, Contacto/Redes, Descargar CV
- Toggle de modo oscuro/claro con persistencia (localStorage)
- Animaciones con Framer Motion (scroll, hover, transiciones)
- Componentes accesibles con Radix UI + shadcn/ui
- Deploy a GitHub Pages
- Stack: Astro 5 + React 18 + TypeScript + Tailwind CSS v4

### Sin decidir / abierto
- Marca personal / nickname (pendiente de definir)
- Foto personal (debe proporcionarla Alejandro)
- Contenido real de proyectos, experiencia, skills (debe proporcionarlo Alejandro)
- Dominio personalizado
- Blog / artículos técnicos (no incluido por ahora)
- Analytics / tracking

## Brand Commitments

- **Nombre:** Marca personal / nickname (por definir)
- **Voz:** Profesional pero accesible — comunica confianza técnica sin ser rebuscado
- **Estilo:** Moderno, limpio, con animaciones sutiles que demuestran calidad de ejecución
- **Diferenciador:** El portafolio mismo es la demostración de skill — no solo dice lo que Alejandro sabe, lo muestra en cómo está construido
- Se hereda la calidad visual del theme base (astro-genai-startup-theme) con componentes shadcn/ui, Radix UI, y Framer Motion

## Evidence on Hand

- Código fuente del theme base en `C:\Users\Alejandro\astro-genai-startup-theme`
- Proyecto destino en `C:\Users\Alejandro\portfolio-dev`
- Componentes pre-construidos: Hero, Features, Pricing, Testimonials, FAQ, Newsletter, Footer, ThemeToggle
- Stack completo: Astro 5 + React 18 + shadcn/ui + Framer Motion + Tailwind CSS v4 + Radix UI + Lucide Icons
- GitHub Actions workflow para deploy a GitHub Pages
- TODO.md con ~95% del template completado

**Ausente:** Alejandro debe proveer contenido real: nombre, foto, bio, skills list, proyectos, experiencia laboral, CV PDF, enlaces a redes.

## Product Principles

1. **El portafolio es la prueba.** Cada decisión de diseño debe demostrar competencia técnica. Si no se nota el esfuerzo, no está bien.

2. **Primero el reclutador.** Optimizar para escaneo rápido: jerarquía visual clara, secciones distintas, llamados a la acción evidentes (Contacto, CV). El visitante decide en segundos si sigue scrolleando.

3. **Animaciones con propósito, no decoración.** Cada transición y hover state debe mejorar la comprensión o la experiencia, no distraer. Nada se mueve sin razón.

4. **Consistencia sobre creatividad.** Un solo sistema visual coherente (tipografía, espaciado, color) en todas las secciones. El modo oscuro y claro deben sentirse igual de cuidados.

5. **Cero fricción para contactar.** El camino desde "me interesa" hasta "enviar mensaje o descargar CV" debe ser directo, sin vueltas.

## Accessibility & Inclusion

- Soporte de modo oscuro/claro (respetando preferencia del sistema)
- Componentes accesibles via Radix UI (teclado, ARIA, screen readers)
- Contraste suficiente en ambos modos
- Navegación por teclado en componentes interactivos
- No se estableció un estándar WCAG específico; apuntar a WCAG 2.1 AA como mínimo de calidad