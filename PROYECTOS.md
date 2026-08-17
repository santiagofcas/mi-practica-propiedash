# Proyectos de práctica (para seguir después del onboarding)

Ya terminaste el recorrido y tu primera tarjeta. Estos proyectos son para **seguir
practicando** el stack real de Propiedash, sin tocar producción. Se hacen con **tus propias
cuentas gratis** de cada herramienta (no las de la empresa): así aprendes las herramientas
de verdad sin ningún riesgo. En la graduación, solo cambias tus cuentas por las reales de
Propiedash.

Cada proyecto es un escalón más, y todos son cosas que Propiedash de verdad tiene. **Tu guía
los construye contigo y te explica cada parte:** tú aprendes viendo y entendiendo. Cuando
algo necesite crear una cuenta, tu guía te abre la página; tú solo escribes tus datos.

Van en dos fases, y **lo importante es la Fase 2** (el stack real: Next.js, Vercel, Supabase,
Resend). La Fase 1 (frontend) es solo un **calentamiento corto** para agarrarle la mano al
flujo de git y deploy: haz 1 o 2 proyectos y pásate rápido a la Fase 2. Todo el que pasa por
aquí tiene que entender la Fase 2, ahí está el stack de verdad de Propiedash.

---

## Fase 1 — Calentamiento de frontend (haz 1 o 2, no te quedes aquí)

Un calentamiento rápido para agarrar el flujo de git y deploy. Haz 1 o 2 y pásate a la Fase
2. Todo en HTML/CSS/JS, en **tu propio repo de práctica** (tu guía te lo creó), publicado con
GitHub Pages. Cada proyecto es un PR (que tú mismo fusionas). Cuando se fusiona a `main`,
queda **en vivo** en tu URL: `https://tu-usuario.github.io/tu-repo/...` (eso es un **deploy**,
publicar en la web, como propiedash.com).

1. **Tu tarjeta de propiedad** (ya la hiciste). Una tarjeta con la marca de Propiedash.
2. **Página de resultados.** 6 tarjetas en cuadrícula, como `/buscar`. Aprendes: reutilizar
   un componente y acomodar en grid responsivo.
3. **Ficha de propiedad.** La página completa de UNA propiedad (foto, specs, descripción,
   agente, ubicación). Aprendes: estructura de página y jerarquía visual.
4. **Perfil de agente (un Dashtag).** Encabezado del agente + sus propiedades debajo.
5. **Favoritos y filtro (tu primer JavaScript).** Un corazón para marcar favoritos y un
   filtro Venta/Alquiler. Aprendes: reaccionar a clics y cambiar la página en vivo.
6. **Cambio de moneda USD ↔ Bs (tasa BCV).** Un botón que convierte todos los precios.

---

## Fase 2 — El stack de verdad (LO IMPORTANTE, con TUS cuentas gratis)

Aquí armas un **mini-Propiedash** con las mismas herramientas que usamos: Next.js, Vercel,
Supabase, Resend. Todo en **tu propio repo** (crea uno nuevo, ej. `mi-propiedash`) y con
**tus cuentas gratis**. Nada de esto toca Propiedash real.

Tu guía te instala lo que falte (Node, etc.) y te abre las páginas para crear cada cuenta.
El **paso a paso detallado de cada proyecto** (comandos exactos, dónde va cada llave, y los
tropiezos a evitar) lo tiene tu guía en `referencia/FASE-2-STACK.md` del paquete de
onboarding. Tú solo pídele "sigamos con el proyecto 7" y él te lleva.

7. **Next.js: tu app de verdad.**
   - Con tu guía, crea una app con `create-next-app` (el framework de Propiedash) y pásate
     de HTML estático a Next.js. Corre `npm run dev` y ve tu página de resultados, ahora en
     una app real, en `localhost:3000`.
   - Aprendes: qué es un framework, páginas y componentes, correr un servidor de desarrollo.

8. **Vercel: deploy real.**
   - Crea tu cuenta gratis de **Vercel** (con tu GitHub). Sube tu app a un repo nuevo tuyo y
     conéctalo a Vercel. Cada `push` se publica solo, en una URL real.
   - Aprendes: deploy de verdad, el mismo que usa propiedash.com. (Vercel > GitHub Pages para
     apps: aquí ya es "lo real".)

9. **Supabase: la base de datos.**
   - Crea tu proyecto gratis de **Supabase**. Haz una tabla `propiedades` con unas columnas
     (título, precio, zona, habitaciones...). Mete 3–4 filas a mano.
   - Haz que tu app **lea las propiedades desde la base** (no escritas a mano en el código).
   - Aprendes: qué es una tabla y una consulta, y por qué existen los clientes de Supabase y
     el RLS (que controla quién ve qué). Es el corazón del backend de Propiedash.

10. **Supabase Auth: login.**
    - Agrega **iniciar sesión** a tu mini-app (correo o Google). Que solo un usuario con
      sesión pueda ver cierta página.
    - Aprendes: autenticación, sesiones, y por qué el cliente correcto de Supabase importa.

11. **Resend: correos de verdad.**
    - Crea tu cuenta gratis de **Resend** y consigue una API key. Cuando alguien "contacta"
      una propiedad en tu app, **envía un correo** con Resend.
    - Aprendes: correo transaccional, exactamente lo que usa Propiedash para sus notificaciones.
    - Ojo de seguridad: la API key va en variables de entorno (`.env.local`), NUNCA en el
      código ni en el repo. (Lo mismo aplica a todas las llaves.)

12. **Formularios (react-hook-form + zod).**
    - Un formulario de "publicar propiedad" que **valida** los datos antes de guardarlos en
      tu tabla de Supabase (precio numérico, título obligatorio, etc.).
    - Aprendes: formularios y validación como los hace Propiedash.

### Estírate (opcional)
- Sube fotos de la propiedad a **Supabase Storage**.
- Un mapa con la ubicación (como el `/buscar` de Propiedash).
- Modo claro/oscuro.

---

## Cierre

Cuando termines la Fase 2 ya construiste un **mini-Propiedash sobre el stack real**
(Next.js + Supabase + Vercel + Resend), tocando cada pieza con tus propias manos, sin haber
tocado producción ni una vez. En ese punto entiendes de verdad cómo funciona todo.

La graduación es simple: cambias tus cuentas de práctica por las **reales de Propiedash**
(la organización de GitHub, la Supabase de desarrollo, el Vercel del equipo, la key de
Resend), que te da Andrés. El primer PR real (agregar una pregunta al FAQ) va a sentirse
fácil, porque ya hiciste algo más grande tú solo.
