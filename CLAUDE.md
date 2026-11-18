# Repo del método de trabajo (adaptación de BMAD)

Este repo no tiene código de producto. Tiene el método de trabajo que se usa en todos los proyectos: agentes, flujos, plantillas y checklists. El código vive en los repos de cada proyecto (MisMeds, RentHub, Turnomator).

## Cuando este repo está conectado a una sesión junto con un proyecto
- Los agentes de `.claude/agents/` y la skill `flujo-bmad` de `.claude/skills/` quedan disponibles. Para coordinar el trabajo, seguí esa skill.
- Los artefactos de cada proyecto (brief, PRD, arquitectura, historias, estado del sprint) se guardan **en el repo del proyecto**, no acá. Si el proyecto ya tiene backlog, stories o docs, se respetan sus convenciones; si no, se usa `docs/bmad/` dentro del proyecto.
- Las plantillas y checklists se leen desde este repo: `plantillas/` y `checklists/`.

## Cuando se trabaja sobre este repo
- `original/v6.12/` es una copia sin modificar de BMAD Method 6.12.4 (licencia MIT). No se edita: sirve de referencia y para comparar al actualizar. Para actualizarla, reemplazá la carpeta entera por la nueva versión y anotá el commit en `original/v6.12/VERSION` (o creá una carpeta nueva por versión).
- Lo que se usa en la práctica es la adaptación en español: `.claude/`, `flujos/`, `plantillas/` y `checklists/`. Si cambiás un flujo, revisá que los agentes, la skill y las plantillas sigan siendo coherentes.
- Este repo no es un producto oficial de BMad Code, LLC. No uses "BMad" como nombre de producto (ver `NOTICE.md`).
