# Genyus Academy — Landing (Curso 26-27)

Landing page de captación para **Genyus Academy** y **Genyus Lab**, con el cuadrante de horarios de la **Opción A** (escenario de lanzamiento) y dos formularios de inscripción (Fillout) integrados.

Construida sobre el **Genyus School Design System** (colores, tipografías Helotypo / Nobel Uno / Anton, gradientes de marca) y pensada para integrarse en un sitio mayor — **sin header ni footer propios** y con un margen superior para el header del sitio anfitrión.

---

## 🚀 Puesta en marcha

El archivo **`index.html` es autocontenido**: incluye todo (estilos, tipografías, imágenes e íconos) en un único archivo. No necesita build ni servidor.

- **Abrir en local:** haz doble clic en `index.html`.
- **Publicar en GitHub Pages:**
  1. Sube este repositorio a GitHub.
  2. Settings → Pages → Source: `Deploy from a branch` → rama `main`, carpeta `/root`.
  3. Tu landing quedará en `https://<usuario>.github.io/<repo>/`.

> El único recurso externo es el embed de **Fillout** (formulario "Más info"), que se carga desde `server.fillout.com`. Requiere conexión a internet.

---

## 🧭 Estructura de la página

1. **Hero** — propuesta de valor y CTA principal.
2. **Barra de premio** — "Premio Mejor Proyecto de Educación de España 2025".
3. **Nuestro método** — tres pilares (mentalidad emprendedora, habilidades para la vida, comunicar ideas).
4. **Academy y Lab** — los dos itinerarios, cada uno con su **precio** (80 €/mes y 100 €/mes) y CTA.
5. **Metodología** — clases en directo de 90 min, grupos reducidos, progresión por curso.
6. **Grupos** — un grupo por etapa, de 5.º EP a 4.º ESO.
7. **Horario · Opción A** — Academy (3 grupos) + Lab (2 grupos quincenales alternos).
8. **Por qué desde 5.º Primaria** — criterio pedagógico (9-10 años).
9. **Ecosistema** — South Summit, Startup OLÉ, Future Minds Fest, con foto real de cada evento.
10. **Inscripción** — conmutador de dos pestañas (**Reservar plaza** es la vista por defecto):
    - **Reservar plaza** → formulario embebido de Fillout (id `vSuEqLXPYWus`).
    - **Más info** → formulario embebido de Fillout (id `wYMXyRAywkus`).

Totalmente responsive: breakpoints de tablet (≤1024px / ≤860px) y móvil (≤640px) ajustan grids, tamaños de texto y paddings.

---

## 📝 Formularios de inscripción

Ambas pestañas usan formularios **Fillout** embebidos (`data-fillout-id`, con `data-fillout-dynamic-resize` para que se ajusten a su alto real sin scroll interno):

- **Reservar plaza** → `vSuEqLXPYWus`
- **Más info** → `wYMXyRAywkus`

### ⚠️ Conectar los envíos a Slack

No requiere código: desde el panel de cada formulario en Fillout → **Integrate → Slack** → conecta tu workspace, elige el canal y mapea los campos. También puedes usar Zapier/Make o un webhook si necesitas lógica adicional.

Para cambiar de formulario, sustituye el valor de `data-fillout-id` por el id de tu nuevo formulario en Fillout.

---

## 🎨 Personalización

- **Fotografías:** ya son fotos reales de Genyus (alumnos en clase, sesión en Google Meet, y las 3 fotos de eventos). Puedes sustituirlas por otras en `assets/hero/` y `assets/events/` manteniendo el mismo nombre de archivo, o editando la ruta en el HTML.
- **ID de Fillout:** cámbialo en el atributo `data-fillout-id` de cada panel si usas otro formulario.
- **Textos, colores, precios y horarios:** editables directamente en `index.html` (busca la sección correspondiente por su comentario `<!-- ===== -->`).

---

## 📂 Contenido del repositorio

```
index.html          → Landing autocontenida (lista para publicar / Framer)
README.md           → Este archivo
assets/logos/       → Logotipos de marca (SVG) para referencia
assets/hero/        → Fotos del hero y de la sección de metodología (comprimidas)
assets/events/      → Fotos de South Summit, Startup OLÉ y Future Minds Fest (comprimidas)
```

---

*Genyus School · Movimiento Future Minds · Aprender es una aventura.*
