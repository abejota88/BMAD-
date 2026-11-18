# Flujo rápido

**Cuándo:** un bug, un ajuste o una mejora chica: se explica en pocas líneas, toca pocos archivos y no cambia la arquitectura ni el modelo de datos de forma importante. Para una edición trivial que el PO va a revisar igual (un texto, un typo), no hace falta el método.
**Agentes:** `quick-dev`, `dev` (revisión), `test-architect` (control).

## Pasos
1. `quick-dev` escribe la especificación rápida (`plantillas/especificacion-rapida.md`), implementa con pruebas y se autorrevisa.
2. Si en el camino descubre que el cambio es grande, **para** y el coordinador lo pasa al camino estándar.
3. `dev` en modo revisar, en una instancia nueva, revisa el diff.
4. `test-architect` corre la suite y da el veredicto.
5. El coordinador presenta el resultado al PO.
