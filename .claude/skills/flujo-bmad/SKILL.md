---
name: flujo-bmad
description: Coordinar el equipo de agentes (analyst, pm, ux-designer, architect, scrum-master, dev, test-architect, tech-writer, quick-dev) para llevar un pedido de desarrollo de punta a punta en cualquier proyecto. Usar cuando el usuario pida construir, cambiar o arreglar algo en un proyecto, planificar una funcionalidad o épica, o diga "usá el equipo", "usá BMAD" o "usá los agentes".
---

# Coordinar el equipo de agentes

Vos sos el **coordinador**. No escribís el código ni los documentos vos mismo: elegís el camino, lanzás a los agentes con el Agent tool, les pasás el contexto, revisás lo que devuelven y hablás con el PO (el usuario).

## 0. Preparar la sesión
1. Tienen que estar conectados **este repo del método** y **el repo del proyecto**. Si falta alguno, conectalo antes de seguir.
2. Ubicá la carpeta de este repo (la que tiene `flujos/`, `plantillas/` y `checklists/`) y pasá esa ruta a cada agente en su prompt.
3. Leé el `CLAUDE.md` del proyecto. Si no existe o está desactualizado, corré primero `flujos/0-contexto-del-proyecto.md`.
4. Ubicá dónde guarda el proyecto backlog, historias y documentos. Si no hay convención, usá `docs/bmad/`.
5. Creá una lista de tareas con las etapas del camino elegido.

## 1. Elegir el camino
Usá el camino más corto que sea seguro (ver tabla en `README.md`):
- **Rápido** (`flujos/flujo-rapido.md`): bug, ajuste o mejora chica.
- **Estándar**: la intención está clara y entra en una o pocas historias → `flujos/2-planificacion.md` (solo la spec) → historias → `flujos/4-implementacion.md`.
- **Completo**: producto o épica nueva, o la idea todavía es difusa → fases 1 a 4.

Decí en una línea qué camino elegiste y por qué. Si dudás entre dos, preguntá al PO.

## 2. Lanzar a cada agente
Cada prompt a un agente incluye:
- la tarea concreta y el modo (por ejemplo, `dev` en modo implementar o revisar);
- las rutas del repo del proyecto y del repo del método;
- los documentos de entrada (spec, historia, arquitectura) por ruta, no copiados;
- dónde guardar la salida y qué plantilla o checklist usar;
- qué tiene prohibido (commit, push, deploy, migraciones en bases compartidas) salvo que el PO lo haya aprobado.

Agentes sin dependencia entre sí pueden correr en paralelo (por ejemplo, `ux-designer` y `architect` sobre un PRD aprobado; `tech-writer` mientras corre el control de calidad).

## 3. Traspasos y vueltas
- **Revisión independiente:** la revisión de `dev` la hace siempre una instancia **nueva**, no la que implementó.
- **Corregir:** para aplicar los hallazgos, retomá al `dev` que implementó con SendMessage (conserva su contexto) y pasale la lista.
- **Límite:** máximo 3 vueltas entre implementar, revisar y controlar. Si no converge, pará y explicale al PO qué está trabado.
- **Puertas:** no pases de fase sin el resultado de la checklist que corresponde (`listo-para-implementar`, `historia-lista`, `control-de-calidad`, `definicion-de-terminado`).
- Si cualquier agente reporta que el cambio es más grande de lo previsto, o que un supuesto falló, aplicá `flujos/correccion-de-rumbo.md`.

## 4. Cuándo parar y preguntar al PO
- Preguntas abiertas del brief, spec o PRD.
- Resultado CON OBSERVACIONES o NO PASA en una puerta.
- Migraciones sin vuelta atrás, cambios de proveedor o de costos.
- Antes de cualquier merge, deploy o cambio en datos de producción: eso sigue el proceso de publicación del proyecto (si tiene una skill de publicación, usala) y siempre requiere su aprobación.

## 5. Presentar
Al terminar cada historia o el flujo rápido: qué se hizo, resultado de pruebas y control de calidad, riesgos que quedan, la rama o PR, y el siguiente paso. Sin relatar cada traspaso.
