# Invitación — Lucía & Lucas

Invitación de boda web (una sola página, sin dependencias). Importada desde el diseño de Claude Design `Invitacion Lucia y Lucas.dc.html` y convertida a HTML + JavaScript estándar para que funcione abriendo el archivo directamente en el navegador.

- **Fecha:** Viernes 7 de Agosto de 2026 — Durazno, Uruguay
- **Estilo:** minimalista blanco y negro (fuentes EB Garamond, Bodoni Moda, Pinyon Script).
- **En línea:** http://www.LucasYLucia.somee.com/
- **Cómo verla:** abrí `index.html` en cualquier navegador (doble clic). También podés subirla a cualquier hosting estático (Netlify, GitHub Pages, Vercel).

<p align="center">
  <img src="screenshots/portada.png" alt="Portada de la invitación" width="360">
</p>

## Contenido

| Archivo | Descripción |
|---|---|
| `index.html` | La invitación completa (portada, invitación, monograma LL, detalles + regalo en dos columnas, cronograma, acciones). |
| `couple-1.jpg` | Foto de la portada (blanco y negro por CSS). |

## Secciones

1. **Portada** — foto de la pareja con la fecha `07 / 08 / 26` en tipografía Bodoni.
2. **Invitación** — texto en itálica.
3. **Monograma** — las iniciales `LL` superpuestas en Pinyon Script.
4. **Detalles + Regalo** — dos columnas: datos del festejo con teléfonos de WhatsApp (Lucía / Lucas), y datos de la cuenta OCA Blue con botón *Copiar datos*.
5. **Cronograma** — línea de tiempo horizontal: 11 AM Ceremonia Civil · 12 PM Brindis · 17 PM Ceremonia Religiosa, cada uno con enlace a Google Maps.
6. **Acciones** — *Agregar al calendario* (Google Calendar) y la firma `Lucía & Lucas`.

## Funciona sin runtime

El diseño original usaba el runtime de Claude Design (`support.js`, `{{ }}`, `<sc-if>`, `<image-slot>`). Aquí se reimplementó en JavaScript puro:

- **Botón "Copiar datos"** de la cuenta OCA Blue.
- **"Agregar al calendario"** genera el evento de Google Calendar.
- **Animación de aparición** al hacer scroll.
- Enlaces de WhatsApp para confirmar con Lucía / Lucas y enlaces a Google Maps.

> Nota: el diseño trae una cuenta regresiva opcional (prop `showCountdown`), pero viene **desactivada por defecto**, así que no se incluye en esta versión estática. Si la querés, avisame y la agrego.

## ⚠️ Sobre la foto

La foto se descargó desde el diseño a través del MCP de Claude Design, que **limita cada archivo a 256 KiB**, por lo que llegó **recortada** (incompleta) y puede que no se vea completa.

**Para arreglarlo:** reemplazá `couple-1.jpg` por la foto original en alta resolución (mismo nombre de archivo). El diseño usa `object-fit: cover`, así que cualquier proporción se acomoda sola. Idealmente vertical (~1024×1536).
