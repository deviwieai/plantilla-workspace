# [NOMBRE DEL PROYECTO]

[Qué es este proyecto en 2 o 3 líneas: cliente, qué se le entrega y objetivo actual.]

## Mapa

- `contexto/proyecto.md`: cliente, objetivos, alcance, glosario y marca. Léelo solo si la tarea lo requiere.
- `contexto/detalle/`: material de referencia por tema. Lee solo el archivo que la tarea necesite; el índice está al final de `contexto/proyecto.md`.
- `contexto/decisiones.md`: decisiones tomadas. Solo se agregan líneas al final.
- `contexto/entrada/`: material en bruto sin procesar. No lo leas salvo con `/metodo:contexto`.
- `gobernanza/roles.md`: quién responde por cada área.
- `equipo/<persona>/`: perfil y bitácora de cada persona.
- `registro/errores.csv`: registro de errores de uso de IA.
- `areas/<área>/`: el trabajo del proyecto.
- `plantillas/`: formatos de documentos del proyecto.
- `informes/`: auditorías e informes.

## Notion

- Tareas: [collection://...]
- Entregables: [collection://...]

Las tareas viven solo en Notion; no se copian al repositorio. El responsable es un campo de selección con el nombre de la persona.

## Reglas

1. Una tarea por sesión. Se abre con `/metodo:inicio` y se cierra con `/metodo:cierre`.
2. Bitácoras, registros e informes son históricos: no los leas completos salvo que se pida.
3. Antes de modificar un área que no es de la persona, revisa `gobernanza/roles.md` y avísale.
4. `CLAUDE.md`, `contexto/proyecto.md` y `gobernanza/` solo los cambia la persona designada en `gobernanza/roles.md`.
5. Nunca escribas claves, contraseñas ni datos personales de clientes en el repositorio.
6. Todo dato o cifra que vaya a un entregable se verifica contra su fuente. Si no se pudo verificar, se dice.
7. Los errores de uso de IA se registran con `/metodo:error`, sin buscar culpables.
8. Respuestas breves y en español.
