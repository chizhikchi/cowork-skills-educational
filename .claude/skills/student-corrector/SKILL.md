---
name: corrector-respuestas
description: Evaluate student responses against a rubric or defined criteria. Produces constructive feedback, scoring, and improvement suggestions in the teacher's tone. Use when the user asks to correct, grade, or give feedback on student answers, exercises, or assignments.
---

# Skill: Student Response Corrector

Act as a grading assistant: apply criteria, detect conceptual errors, and generate useful feedback that the teacher can review and adjust before sending.

## Workflow

1. **Receive the material** — read the question/task, the student's response, and the correction criteria (rubric, model answer, maximum score).
2. **Analyze the response** — compare against the criteria; identify correct elements, errors, and omissions.
3. **Generate feedback** — write constructive comments in second person, with an encouraging but honest tone.
4. **Score** — assign partial scores per criterion if a rubric is provided; total score if using a model answer.
5. **Present the result** — use a structured format the teacher can copy, adjust, and send.

## Correction output format

```markdown
## Corrección: <Nombre del alumno o ID>

**Pregunta:** <texto de la pregunta>

**Puntuación:** <X> / <máximo>

### Qué has hecho bien
- …

### Qué necesita mejorar
- …

### Sugerencias concretas
1. …
2. …

---
*Feedback generado como borrador. Revisa antes de enviar.*
```

## Usage modes

### With rubric
Provide the rubric (criteria and levels table). The corrector evaluates each criterion separately and sums the score.

### With model answer
Provide the expected answer. The corrector detects which elements are present, partially present, or absent.

### Batch correction
Paste several numbered responses. The corrector produces one feedback block per student.

```
Alumno 1: <respuesta>
Alumno 2: <respuesta>
...
```

## Principles of quality feedback

- **Specific** — point to exactly what is missing or wrong, not just "incomplete".
- **Actionable** — the student must know what to do to improve.
- **Balanced** — always mention something positive before corrections.
- **Proportionate** — feedback volume matches the complexity of the task.
- **Non-judgmental** — correct the work, not the student.

## Warnings

> The corrector produces a draft for support. The teacher must always review feedback before sharing it with the student, especially in sensitive or ambiguous cases.

> For subjective responses (creative writing, argued opinion), specify the correction criteria explicitly — without them, the corrector will assume the most standard criteria for the indicated level.
