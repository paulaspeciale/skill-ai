# Skill `usable-design`

## ¿Qué es?

Una skill para Claude basada en las ideas de *The Design of Everyday Things* (Don Norman, edición revisada de 2013). No es un resumen del libro: convierte sus principios de psicología y diseño en un método de trabajo para que Claude ayude a crear cosas fáciles de descubrir, entender y usar.

## ¿Para qué sirve?

Ayuda a **diseñar, revisar o arreglar** cualquier cosa con la que la gente interactúa:

- Apps, sitios web, formularios, onboarding, dashboards y pantallas de ajustes
- Mensajes de error, confirmaciones, undo y feedback
- CLIs, APIs y herramientas para desarrolladores
- Productos físicos, señalética y servicios

## ¿Cuándo se activa?

Cuando pides una revisión de usabilidad o UX, o preguntas por qué los usuarios se confunden, se equivocan o no encuentran una función. También cuando mencionas affordances, signifiers, mapeo, modelos mentales o "puertas de Norman", o quieres simplificar un flujo o producto. Se activa aunque no digas "UX", por ejemplo con "¿por qué la gente hace clic en el botón equivocado?".

## Cómo trabaja

Tiene tres modos:

1. **Revisar** un diseño existente: entiende la actividad y el contexto, recorre los siete pasos de la acción, comprueba los principios y los riesgos de error, y entrega un informe priorizado.
2. **Diseñar** algo nuevo: cuestiona el encargo, define primero el modelo conceptual, aplica los principios a cada interacción, planifica los errores y propone cómo probarlo con unas cinco personas.
3. **Diagnosticar** un problema concreto: ubica en qué paso de la acción falla, distingue si es un slip o un mistake y propone el cambio de diseño más pequeño que elimine la causa.

## Ideas centrales

- Si la gente falla, el problema es del diseño, no de la persona.
- Se diseña para cómo se comportan realmente las personas: distraídas, interrumpidas y con hábitos.
- Cuanto más muestre la interfaz, menos hay que recordar (conocimiento en el mundo).
- Hay que resolver el problema real, no solo el que se pidió.

**Los siete principios:** discoverability, feedback, modelo conceptual, affordances, signifiers, mapeos y restricciones.

**Errores:** distingue slips (se quiso una cosa y se hizo otra) de mistakes (el objetivo o el plan era incorrecto). Prefiere prevenir, luego detectar y luego recuperar, y favorece el undo sobre los diálogos "¿Estás seguro?".

## Estructura de archivos

```
usable-design/
├── SKILL.md                      Método, principios, síntomas y guía de consejo (en inglés)
├── references/
│   ├── core-concepts.md          Affordances, signifiers, mapeo, feedback, restricciones, memoria
│   ├── action-cycle-and-emotion.md   Siete pasos, golfos, niveles emocionales, indefensión aprendida
│   ├── errors-and-resilience.md  Slips y mistakes, undo, forcing functions, queso suizo
│   ├── process-and-business.md   Proceso centrado en las personas, doble diamante, feature creep, estándares
│   ├── review-template.md        Plantilla de informe y checklist de auditoría
│   └── worked-examples.md        15 ejemplos de antes y después (software y herramientas dev)
└── evals/                        3 casos de prueba
```

`SKILL.md` queda siempre en contexto cuando la skill se activa; los archivos de `references/` solo se leen según lo que necesite la tarea.

## Ejemplos de uso

- "Revisa esta pantalla de registro: la gente abandona en la contraseña."
- "Mis usuarios borran el proyecto equivocado, ¿cómo lo hago más seguro?"
- "Mi CLI de deploy provoca despliegues accidentales a producción, ¿qué cambio?"
- "Haz este flujo menos confuso."

## Notas

- El contenido está reformulado con palabras y ejemplos propios, sin citas largas del libro.
- Los principios son heurísticas sólidas, no sustituyen observar a usuarios reales; la skill recomienda probar con unas cinco personas.
- Se probó cualitativamente con 3 casos reales; no se midió con métricas.
