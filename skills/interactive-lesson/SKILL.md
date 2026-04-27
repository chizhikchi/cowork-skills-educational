---
name: leccion-interactiva
description: Convert an Obsidian Markdown note into an interactive web page (HTML/CSS/JS): step-by-step lesson, comprehension questions with immediate feedback, progress bar, and clean design. Use when the user asks to convert content to web, create an interactive lesson, generate an HTML page from a .md file, or publish didactic material on Vercel or GitHub Pages.
---

# Skill: Interactive Lesson

Transform an Obsidian `.md` file into a self-contained web page (single HTML file) that students can use in a browser without installing anything.

## Workflow

1. **Read the content** — obtain the lesson `.md` (active file or specified path).
2. **Identify the structure** — extract title, sections/slides, and questions (marked with `?` or in a special block).
3. **Generate the HTML** — produce a self-contained `index.html` file with inline CSS and JS.
4. **Validate** — verify the HTML is valid, works without a server, and has no external dependencies.
5. **Save** — write the file to the project folder with a descriptive name.

## Input Markdown structure

```markdown
---
title: Título de la lección
---

# Introducción
Texto de la primera sección…

---

# Concepto clave
Explicación…

## Pregunta de comprensión

? ¿Cuál es la idea principal de esta sección?
- [ ] Opción incorrecta
- [x] Opción correcta
- [ ] Otra opción incorrecta

---

# Conclusión
Cierre y resumen…
```

Use `---` to separate slides/steps. Use `?` at the start of a paragraph to mark questions. Mark correct answers with `- [x]`.

## Features of the generated page

- **Step-by-step navigation** — Previous / Next buttons between sections.
- **Questions with immediate feedback** — correct/incorrect response without reloading.
- **Progress bar** — completion percentage visible at all times.
- **Responsive design** — works on mobile and desktop.
- **No external dependencies** — does not require internet, CDN, or a server.
- **Self-contained** — a single `.html` file ready to open or upload to Vercel/GitHub Pages.

## Common customization requests

The user can request adjustments in natural language after seeing the result:

- `"Pon las preguntas al final de cada sección"` → move question blocks to end of each slide.
- `"Usa los colores de marca: #1a237e y #fff"` → update CSS variables.
- `"Añade una pantalla de resultados al terminar"` → add final slide with score.
- `"Quita la barra de progreso"` → remove the element and its JS logic.
- `"Añade el logo de la organización"` → insert base64 image in the header.

## Generated HTML structure

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title><!-- lesson title --></title>
  <style>
    /* design variables, layout, progress bar, question styles */
  </style>
</head>
<body>
  <header>
    <div id="progress-bar"></div>
    <h1><!-- title --></h1>
  </header>
  <main>
    <!-- slides generated dynamically -->
  </main>
  <nav>
    <button id="prev">← Anterior</button>
    <span id="counter">1 / N</span>
    <button id="next">Siguiente →</button>
  </nav>
  <script>
    /* navigation and question logic */
  </script>
</body>
</html>
```

## Quick deployment

```bash
# Push to GitHub and deploy on Vercel (run from Claude Code)
git add index.html
git commit -m "add interactive lesson"
git push

# Vercel detects the push and deploys automatically
```

> The generated HTML file is sufficient for GitHub Pages with no additional configuration. For Vercel, connect the repository once and every push deploys automatically.
