---
name: generador-examenes
description: Generate exams, tests, or self-assessments in Markdown from an Obsidian syllabus or note. Produces multiple-choice, true/false, short answer, and essay questions, with an optional answer key. Use when the user asks to create an exam, test, quiz, questionnaire, or assessment from existing didactic content.
---

# Skill: Exam Generator

Create balanced assessment tests aligned with syllabus objectives, ready to use or export.

## Workflow

1. **Read the syllabus or content** — obtain the Obsidian note with the content to assess (active file, note name, or pasted text).
2. **Define parameters** — number of questions, question types, cognitive level, and whether to include an answer key.
3. **Distribute questions** — cover all units/sections proportionally to their time weight.
4. **Generate the exam** — produce two files: the student exam and the teacher's answer key.
5. **Save** — create both notes in Obsidian with `obsidian create`.

## Generation parameters

| Parameter | Options |
|-----------|---------|
| Question types | Multiple choice, T/F, short answer, essay |
| Cognitive level | Remember, Understand, Apply, Analyze, Evaluate, Create |
| Number of questions | Free (default: 10–20) |
| Answer key | Yes / No |
| Estimated time | Calculated automatically |

## Student exam structure

```markdown
---
title: Examen — <Asignatura> · <Unidad o tema>
nivel: <nivel educativo>
duracion: <N minutos>
tags:
  - examen
  - <asignatura>
date: <YYYY-MM-DD>
---

# Examen: <Asignatura>

**Tiempo:** <N> minutos · **Puntuación total:** <N> puntos

---

## Parte A · Opción múltiple (N puntos)
*Marca la respuesta correcta.*

**1.** <Pregunta>

a) <Opción>
b) <Opción>
c) <Opción>
d) <Opción>

---

## Parte B · Verdadero o Falso (N puntos)
*Escribe V o F y, si es falso, corrígelo en una frase.*

**N.** <Afirmación>

---

## Parte C · Respuesta corta (N puntos)
*Responde en 2–3 frases.*

**N.** <Pregunta>

---

## Parte D · Desarrollo (N puntos)
*Responde con detalle. Se valorará la estructura y los ejemplos.*

**N.** <Pregunta>
```

## Answer key structure

```markdown
---
title: CLAVE — Examen <Asignatura> · <Unidad>
tags:
  - clave
  - examen
---

# Clave de corrección

## Parte A
1. b) — <brief justification>
2. …

## Parte B
N. F — <correction>

## Parte C
N. Expected answer: … (variations accepted if they mention <key concepts>)

## Parte D
N. Criteria: <list of key points the answer must include>; partial credit if the student mentions at least <N> of them.
```

## Obsidian commands

```bash
# Create the exam note
obsidian create name="Examen <Asignatura> <fecha>" content="<content>" silent

# Create the answer key (teacher access only)
obsidian create name="CLAVE Examen <Asignatura> <fecha>" content="<key>" silent
```

## Balance recommendations

- **Multiple choice:** fast to grade, covers a lot of content — risk of guessing.
- **T/F with justification:** eliminates chance and adds diagnostic value.
- **Short answer:** assesses real understanding at low grading cost.
- **Essay:** essential for higher levels (analyze, evaluate, create) — limit to 1–2 questions.

> To generate **self-assessments** (students grade themselves), include the answer key at the end of the same document in a collapsed callout: `> [!faq]- Ver respuestas`.
