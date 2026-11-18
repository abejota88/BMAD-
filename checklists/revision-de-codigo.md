# Revisión de código

Revisar en este orden. Cada hallazgo: archivo y línea, problema, caso concreto donde falla, severidad (bloqueante / importante / menor).

1. **Correctitud:** lógica, casos borde, nulos, concurrencia, manejo de errores.
2. **Criterios de aceptación:** ¿se cumplen todos? ¿hay algo implementado que no se pidió?
3. **Seguridad y datos:** autorización, validación de entradas, secretos, inyección, migraciones, pérdida de datos.
4. **Pruebas:** ¿cubren los criterios y los casos borde? ¿prueban algo real?
5. **Arquitectura:** ¿respeta las decisiones y patrones del proyecto?
6. **Mantenibilidad:** duplicación, nombres, complejidad innecesaria.
7. **Estilo:** solo si no lo cubre el linter.

Veredicto: **aprobar** o **pedir cambios**.
