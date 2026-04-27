---
name: actividades-y-rubrica
description: Generate didactic activities (individual or group) along with their evaluation rubric in Obsidian Markdown. Use when the user asks to create activities, exercises, tasks, or practice assignments for students, with or without associated evaluation criteria.
---

# Skill: Activities and Rubric

Design activities aligned with learning objectives and generate analytic rubrics ready to use.

## Workflow

1. **Read the context** — obtain the teaching unit, level, learning objectives, and available time (from the active file or by asking the user).
2. **Design the activity** — define type (individual/group), format (written, oral, project…), required resources, and steps for the student.
3. **Build the rubric** — create a table with criteria, performance levels, and clear descriptors.
4. **Generate the document** — write in Markdown with frontmatter and save with `obsidian create`.

## Activity structure

```markdown
---
title: <Título de la actividad>
unidad: <Unidad didáctica>
tipo: individual | grupal
duracion: <tiempo estimado>
tags:
  - actividad
  - <asignatura>
date: <YYYY-MM-DD>
---

# <Título de la actividad>

## Descripción
<Qué van a hacer los alumnos y para qué.>

## Objetivos
- …

## Instrucciones para el alumno
1. …
2. …

## Recursos necesarios
- …

## Criterios de entrega
- Formato: …
- Fecha límite: …
```

## Analytic rubric structure

```markdown
## Rúbrica de evaluación

| Criterio | Excelente (4) | Bien (3) | En proceso (2) | Insuficiente (1) |
|----------|---------------|----------|----------------|-----------------|
| <Criterio 1> | … | … | … | … |
| <Criterio 2> | … | … | … | … |
| <Criterio 3> | … | … | … | … |

**Puntuación total:** /16 — Aprobado: ≥ 8
```

## Activity types by cognitive level

| Type | When to use |
|------|-------------|
| Comprehension quiz | Verify reading or listening |
| Concept map | Organize and relate concepts |
| Case study | Apply knowledge to real situations |
| Structured debate | Evaluate argumentation and critical thinking |
| Collaborative project | Synthesis and group creation |
| Evidence portfolio | Continuous assessment over time |

## Useful Obsidian commands

```bash
# Create the activity note
obsidian create name="Actividad <título>" content="<content>" silent

# Link the activity to its unit
obsidian append file="Unidad <N>" content="\n- [[Actividad <título>]]"
```

## Notes on good rubrics

- Each descriptor must be observable and measurable — avoid "participates actively" without a clear criterion.
- Share the rubric with students **before** the activity, not just when grading.
- 3 to 5 criteria is sufficient; more criteria dilute the focus.
