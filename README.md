# FÚTBOL LAB · Web animada (Tema 07)

Academia digital de fútbol ficticia en la que el movimiento forma parte del diseño. HTML y CSS puro, mobile first, sin JavaScript.

- **Web publicada:** https://manucarletti07-oss.github.io/futbol-lab-web-animada/
- **Repositorio:** https://github.com/manucarletti07-oss/futbol-lab-web-animada
- **Portfolio:** https://manucarletti07-oss.github.io/

## Páginas

| Archivo | Contenido |
|---|---|
| `index.html` | Portada animada, servicios, pizarra táctica, ejercicios e instalaciones destacados y logotipos en tarjetas 3D |
| `entrenamientos.html` | Catálogo de 12 ejercicios con filtro, desplegables, favoritos y prisma 3D |
| `instalaciones.html` | Seis instalaciones (campo, campo cubierto, gimnasio, sala táctica, vestuarios, recuperación) en tarjetas que giran en 3D |
| `movimiento.html` | Guía de movimiento: carácter, tokens, tabla de animaciones, decisiones, grabaciones y capturas |

## Estructura

```
css/estilos.css       diseño, responsive y estados (sin movimiento)
css/animaciones.css   tokens de movimiento, transiciones, @keyframes y movimiento reducido
img/                  26 SVG: logotipos de la marca + ilustraciones con su mismo estilo
grabaciones/          5 vídeos MP4 de menos de 15 s (uno con movimiento reducido)
capturas/             móvil (360 px), tableta (768 px), ordenador (1280 px) y una por página
```

## Letras

Bebas Neue (títulos) y Barlow (texto), cargadas desde Google Fonts con un `<link>` en cada página.

## Técnicas utilizadas

Transiciones con `:hover` (dentro de `@media (hover: hover)`), `:focus-visible` y `:active` · menú móvil animado · microinteracciones (icono hamburguesa → X, favorito con latido, tooltip, desplegable, filtro, interruptor de pausa, brillo de botones) · contadores con `@property` · skeleton de carga · `@starting-style` · barra de progreso con `animation-timeline: scroll()` · `@keyframes` · transformaciones 3D (tarjetas que giran, prisma) · aparición al hacer scroll con `animation-timeline: view()` dentro de `@supports` · `@view-transition` entre páginas · `prefers-reduced-motion` · pausa global de los bucles.

## Cómo probarla

**Primero descomprimir el ZIP** (clic derecho → Extraer todo). Si se abre `index.html` directamente desde dentro del ZIP, el navegador no encuentra las carpetas `img/` ni `css/` y no se ven imágenes ni funcionan los enlaces. Después, abrir `index.html` de la carpeta extraída. Para el movimiento reducido: DevTools → Rendering → *Emulate CSS media feature prefers-reduced-motion* → `reduce`.
