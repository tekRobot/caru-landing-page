# Landing page — Grupo Textil CARU

Landing page estática (HTML/CSS puro, sin build step, sin frameworks ni CDNs de JS) para
Grupo Textil CARU, negocio de venta de telas. Es el primer entregable de un proyecto más
amplio; no incluye e-commerce, backend ni CMS — es una demo de dirección de marca/UX.

## Estado actual

Solo está construida la propuesta **Cálido Artesanal** (terracota/crema + café — cercano,
hecho a mano, textil mexicano), aprobada por el cliente. El `index.html` de la raíz es
por ahora una copia funcional de esa propuesta, para que la URL genérica de Vercel muestre
algo completo de inmediato.

Cuando se construyan las otras 2 direcciones visuales (Oscuro Editorial, Minimalista
Luminoso), el `index.html` de la raíz se convertirá en un selector real entre las 3.

## Contenido placeholder

**Todo el contenido de contacto, sucursales y redes sociales es ficticio**, marcado así
explícitamente en el código (`design/propuesta-2-calido-artesanal/index.html`). El cliente
proveerá más adelante los datos y las imágenes formales del catálogo real.

## Estructura

```
index.html                                    # copia funcional de la propuesta Cálido Artesanal
design/
  propuesta-2-calido-artesanal/
    index.html
    styles.css
    assets/
      hero-warm.jpg
  CREDITS.md                                  # créditos de imágenes (Unsplash License)
```

## Pensado para cambiar barato

- **Paleta y tipografía**: todas las variables viven en el bloque `:root` de
  `design/propuesta-2-calido-artesanal/styles.css`. Cambiar la marca es editar ese bloque,
  no buscar valores repetidos por todo el archivo.
- **Logo**: hoy es un wordmark de texto (`<span class="logo-wordmark">CARU</span>` en el
  `<header>`). Para poner un logo real, reemplázalo por un `<img>` — el comentario junto al
  `<span>` explica cómo.
- **Foto del hero**: se referencia en una sola línea (`<img class="hero-image"
  src="assets/hero-warm.jpg">`). Reemplazar el archivo o cambiar el `src` es el único paso.
- **Secciones**: cada una está delimitada con comentarios `<!-- Sección: ... -->` /
  `<!-- /Sección: ... -->` en el HTML, sin dependencias de spacing entre secciones vecinas
  (nada de márgenes negativos ni posicionamiento absoluto que cruce secciones), para poder
  agregar, quitar o reordenar sin romper el resto.

## Navegación

Los 5 links del menú (`Catálogo`, `Dónde encontrarnos`, `Conócenos`, `Contacto`, `Redes
sociales`) son anclas reales (`#catalogo`, `#donde`, `#conocenos`, `#contacto`, `#redes`)
dentro de la sección de accesos rápidos de la misma página — clickeables desde ya, aunque
todavía no llevan a contenido final.

## Ver en local

Abre `index.html` (o `design/propuesta-2-calido-artesanal/index.html`) directamente en el
navegador. No requiere servidor ni build.

## Despliegue en Vercel

1. Repo ya inicializado en Git localmente.
2. Push a un repositorio vacío en GitHub.
3. En vercel.com: Add New → Project → Import Git Repository → seleccionar este repo →
   Framework Preset **"Other"**, sin build command, directorio raíz por defecto → Deploy.
4. Cada push a la rama principal redespliega automáticamente.

## Créditos de imágenes

Ver `design/CREDITS.md`.
