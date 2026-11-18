# 3 · Solución

**Cuándo:** hay requisitos (spec o PRD, y UX si existe) y hay que decidir cómo construir. También cuando partes construidas por separado corren riesgo de quedar inconsistentes.
**Agentes:** `architect`, `test-architect`, `pm`, `scrum-master`.

## Pasos
1. **Arquitectura** (`architect`, `plantillas/arquitectura.md`): decisiones que varias historias o agentes deben respetar. Cada decisión relevante como ADR (`plantillas/adr.md`).
2. **Diseño de pruebas** (`test-architect`, `plantillas/plan-de-pruebas.md`): riesgos, niveles de prueba y qué se automatiza.
3. **Épicas e historias** (`pm`, `plantillas/epica.md`, `plantillas/historia.md`): partir spec/PRD y arquitectura en historias con criterios de aceptación. Cada historia debe entrar en una sesión de construcción (orientativo: unas 500 líneas de código sin contar pruebas, en pocos archivos).
4. **Listo para implementar** (`scrum-master` con `architect` y `pm`): correr `checklists/listo-para-implementar.md`. Resultado: **PASA**, **CON OBSERVACIONES** o **NO PASA**.

## Salida
Con PASA (o CON OBSERVACIONES aceptadas por el PO), el `scrum-master` crea el estado del sprint (`plantillas/estado-del-sprint.md`) y empieza la Implementación. Con NO PASA, se vuelve al paso que falló.
