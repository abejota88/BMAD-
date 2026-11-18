# 0 · Contexto del proyecto

**Cuándo:** la primera vez que se trabaja un proyecto con este método, y cada vez que cambian comandos, convenciones o el stack.
**Agentes:** `analyst` (modo documentar lo existente) y `tech-writer`.
**Produce:** `CLAUDE.md` del proyecto (o actualiza el existente) usando `plantillas/contexto-del-proyecto.md`.

## Pasos
1. Leer README, `package.json` / `requirements.txt`, CI, scripts y estructura de carpetas.
2. Verificar cada comando corriéndolo (instalar, probar, lint, build). Anotar solo los que funcionan.
3. Registrar convenciones que difieren de lo habitual, políticas (qué no se toca, cómo se publica) y trampas conocidas.
4. Indicar dónde viven en el proyecto el backlog, las historias y los documentos de diseño.
5. Mantenerlo corto: lo que un agente necesita para no equivocarse, no un manual.

**Salida:** el contexto revisado por el coordinador y mergeado en el proyecto.
