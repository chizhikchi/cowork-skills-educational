---
name: temario-didactico
description: Generate a structured didactic syllabus (temario) from a topic, subject, or existing content. Produces learning units, thematic blocks, learning objectives, and time distribution in Obsidian Markdown. Use when the user asks to create a syllabus, course program, lesson plan, or didactic sequence.
---

# Skill: Didactic Syllabus (Temario)

Generate structured syllabi ready to use in Obsidian, export to Word, or publish on the web.

## Workflow

1. **Gather context** — ask for (or read from the active file) the topic/subject, educational level, total course duration, and desired output format.
2. **Define the structure** — divide content into units or thematic blocks with estimated duration.
3. **Develop each unit** — add learning objectives (using Bloom's taxonomy verbs), key contents, and methodological suggestions.
4. **Generate the document** — write the syllabus in Obsidian Flavored Markdown with frontmatter, hierarchical headings, and a summary table at the top.
5. **Save** — use `obsidian create` to create the note in the vault with appropriate properties.

## Syllabus structure

```markdown
---
title: Temario — <Asignatura>
nivel: <ESO / Bachillerato / FP / Universidad / Formación continua>
duracion_horas: <N>
tags:
  - temario
  - <asignatura>
date: <YYYY-MM-DD>
---

# Temario: <Asignatura>

## Resumen

| Unidad | Título | Horas |
|--------|--------|-------|
| 1 | … | … |
| 2 | … | … |

---

## Unidad 1 · <Título>

**Duración:** X horas

### Objetivos de aprendizaje
- Identificar …
- Analizar …
- Aplicar …

### Contenidos
1. …
2. …

### Metodología y recursos
- …
```

## Bloom's taxonomy — verbs by level

| Level | Suggested verbs |
|-------|----------------|
| Remember | identificar, listar, nombrar, definir |
| Understand | explicar, resumir, clasificar, interpretar |
| Apply | usar, resolver, demostrar, calcular |
| Analyze | comparar, diferenciar, examinar, descomponer |
| Evaluate | justificar, criticar, valorar, seleccionar |
| Create | diseñar, elaborar, proponer, construir |

> Use higher-level verbs (analyze, evaluate, create) for advanced objectives.

## Useful Obsidian commands

```bash
# Create the syllabus note
obsidian create name="Temario <Asignatura> <Año>" content="<content>" silent

# Append a new unit to an existing note
obsidian append file="Temario <Asignatura>" content="<nueva unidad>"

# Search existing syllabi
obsidian search query="tag:#temario"
```

## Example invocation

> "Crea un temario para un curso de introducción a la programación para adultos sin experiencia técnica, 40 horas totales."

Respond with the complete note in Markdown, ready to paste or create with `obsidian create`.
