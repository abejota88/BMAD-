# 4 · Implementación (ciclo de construcción)

**Cuándo:** hay historias listas. Se repite una vez por historia.
**Agentes:** `scrum-master`, `dev`, `test-architect`, `tech-writer`.

## Ciclo por historia
1. **Preparar** (`scrum-master`): completar la historia hasta que pase `checklists/historia-lista.md`. Debe poder implementarse sin leer nada más.
2. **Pruebas de aceptación primero** (`test-architect`, opcional): si la historia es de riesgo, escribir antes las pruebas que la definen.
3. **Implementar** (`dev`, modo implementar): aclarar la intención, planear, implementar con pruebas y correr la suite.
4. **Revisar** (`dev`, modo revisar, **en una instancia nueva** que no vio la implementación): `checklists/revision-de-codigo.md`. Si hay hallazgos bloqueantes o importantes, vuelven al paso 3. Máximo 3 vueltas; si no converge, se escala al PO.
5. **Control de calidad** (`test-architect`): `checklists/control-de-calidad.md`. Veredicto PASA, CON OBSERVACIONES o NO PASA. NO PASA vuelve al paso 3.
6. **Documentar** (`tech-writer`): si cambió algo visible o de configuración.
7. **Presentar** (coordinador): resumen al PO con lo hecho, pruebas, riesgos y la rama o PR. Se marca la historia como terminada solo si pasa `checklists/definicion-de-terminado.md`.

Publicar (merge, deploy, migraciones) sigue el proceso propio de cada proyecto y requiere aprobación explícita del PO.

## Al cerrar una épica
**Retrospectiva** (`scrum-master`, `plantillas/retrospectiva.md`): qué salió bien, qué no, acciones concretas y qué cambia para la próxima épica. Si aparecieron problemas grandes, pasar a Corrección de rumbo.
