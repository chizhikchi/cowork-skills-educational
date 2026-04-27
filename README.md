# Claude Code Skills — Educación

Skills para [Claude Code](https://claude.ai/code) orientadas a equipos docentes. Claude Cowork es una versión de Claude Code pensada para el knowledge work: agéntica, con skills por defecto y conectores, funciona con cualquier carpeta. En esta sesión la usamos con Obsidian, Markdown y GitHub.

> **Nota:** Las skills personalizadas de este repositorio se importan en **Claude Code**, no en Cowork. Cowork dispone de sus propias skills preinstaladas, pero de momento no admite la importación de skills externas.

## Skills disponibles

| Skill | Descripción |
|-------|-------------|
| [didactic-syllabus](skills/didactic-syllabus/SKILL.md) | Genera temarios estructurados con unidades, objetivos y distribución horaria |
| [activities-and-rubric](skills/activities-and-rubric/SKILL.md) | Diseña actividades didácticas con su rúbrica de evaluación |
| [student-corrector](skills/student-corrector/SKILL.md) | Evalúa respuestas de alumnos y genera feedback constructivo |
| [interactive-lesson](skills/interactive-lesson/SKILL.md) | Convierte un `.md` en una página web interactiva lista para Vercel |
| [exam-generator](skills/exam-generator/SKILL.md) | Crea exámenes y autoevaluaciones a partir del temario |

## Uso

Copia la carpeta de la skill que necesites en tu directorio de skills de Claude Code, o carga el fichero `SKILL.md` directamente en tu sesión.

## Flujo de trabajo

```
Obsidian (.md) → Cowork (skills preinstaladas) → materiales → Claude Code (skills personalizadas) → GitHub → Vercel
```
