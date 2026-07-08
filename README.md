# Genyus Academy — Landing (Curso 26-27)

Landing page de captación para **Genyus Academy** y **Genyus Lab**, con el cuadrante de horarios de la **Opción A** (escenario de lanzamiento) y un formulario de inscripción integrado.

Construida sobre el **Genyus School Design System** (colores, tipografías Helotypo / Nobel Uno / Anton, gradientes de marca) y pensada para integrarse en un sitio mayor.

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
2. **Nuestro método** — tres pilares (mentalidad emprendedora, habilidades para la vida, comunicar ideas).
3. **Academy y Lab** — los dos itinerarios (extraescolar semanal vs. mentorías quincenales premium).
4. **Metodología** — clases en directo de 90 min, grupos reducidos, progresión por curso.
5. **Grupos G1–G6** — un grupo por etapa, de 5.º Primaria a 4.º ESO.
6. **Horario · Opción A** — Academy (3 grupos) + Lab (2 grupos quincenales alternos).
7. **Por qué desde 5.º Primaria** — criterio pedagógico de edad mínima.
8. **Ecosistema** — South Summit, Startup OLÉ, Future Minds Fest.
9. **Inscripción** — conmutador de dos pestañas:
   - **Más info** → formulario embebido de Fillout.
   - **Reservar plaza** → formulario propio con lógica condicional y validación.

---

## 📝 Formulario "Reservar plaza"

Formulario en 5 bloques según el dossier pedagógico:

1. Datos del alumno/a (nombre, fecha de nacimiento → calcula edad, curso, colegio, localidad, provincia).
2. Datos del tutor legal (nombre, teléfono, email, facturación).
3. Programa + **horario asignado automáticamente** según curso/programa + casilla de conformidad.
4. **Candidatura a Genyus Lab** (bloque condicional: solo aparece al elegir Lab).
5. Autorizaciones (autonomía digital + protección del menor).

Incluye validación de campos y el límite de edad 13–17 para Lab.

### ⚠️ Conectar los envíos

- **Fillout ("Más info"):** conéctalo a Slack desde el propio panel de Fillout (Integrate → Slack) o vía Zapier/Make/webhook. No requiere código.
- **Formulario propio ("Reservar plaza"):** actualmente valida y muestra un mensaje de éxito, **pero no envía los datos a ningún servidor**. Para recibir los envíos (email, Slack, base de datos…) hay que conectar el `handleSubmit` a un backend o webhook. Alternativa sin código: usar el embed de Fillout para ambas pestañas.

---

## 🎨 Personalización

- **Fotografías:** son imágenes de stock (Unsplash) como *placeholder*. Sustitúyelas por fotos reales de Genyus.
- **ID de Fillout:** cámbialo en el `data-fillout-id` si usas otro formulario.
- **Textos, colores y horarios:** editables en el archivo fuente `Landing Genyus Academy.dc.html` (versión de trabajo) antes de re-empaquetar.

---

## 📂 Contenido del repositorio

```
index.html      → Landing autocontenida (lista para publicar)
README.md       → Este archivo
assets/logos/   → Logotipos de marca (SVG) para referencia
```

---

*Genyus School · Movimiento Future Minds · Aprender es una aventura.*
