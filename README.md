# Plantilla de proyecto

Esqueleto de un proyecto que se trabaja con Claude siguiendo la metodología de la empresa. Los comandos vienen del plugin `metodo` (repositorio `metodologia-workspace`) y se actualizan sin tocar los datos de este proyecto.

## Crear un proyecto nuevo (una persona, una sola vez)

1. En GitHub, abre `plantilla-workspace`, pulsa "Use this template" y crea un repositorio privado con el nombre del proyecto.
2. Clónalo y ábrelo en Claude Code.
3. Llena `CLAUDE.md` (nombre y resumen), `contexto/proyecto.md` y `gobernanza/roles.md`.
4. En Notion, dentro de "Proyectos", duplica la página "Plantilla de proyecto" y ponle el nombre del proyecto. Agrega los nombres del equipo al campo Responsable y las áreas al campo Área, en las dos bases.
5. Copia en `CLAUDE.md`, sección Notion, las direcciones `collection://` de las bases Tareas y Entregables del proyecto. Claude las entrega si le pides "busca las bases de datos de la página <nombre> en Notion".
6. Sube los cambios y avisa al equipo.

## Sumarse a un proyecto (cada persona)

1. Clona el repositorio del proyecto.
2. Abre la carpeta en Claude Code y acepta confiar en ella. Se ofrecerá instalar el plugin `metodo`: acéptalo.
3. Conecta Notion en tu Claude, en el mismo espacio de trabajo del equipo.
4. Escribe `/metodo:inicio`. La primera vez te hará tres preguntas para crear tu perfil.
5. Al terminar, `/metodo:cierre` sube tu perfil.

Si el plugin no aparece, instálalo a mano dentro de la sesión:

```
/plugin marketplace add deviwieai/metodologia-workspace
/plugin install metodo@metodologia-workspace
```

## Día a día

| Momento | Comando | Qué hace |
|---|---|---|
| Al empezar | `/metodo:inicio` | Baja los cambios del equipo y muestra dónde quedaste y tus tareas |
| Al detectar un error de la IA | `/metodo:error` | Lo registra en un minuto |
| Al terminar | `/metodo:cierre` | Escribe tu bitácora, actualiza tus tareas y sube todo |

## Dónde va cada cosa

| Qué | Dónde | Quién lo escribe |
|---|---|---|
| Tareas y pendientes | Notion, base Tareas | Todos |
| Entregables finales | Notion, base Entregables | Responsable del área |
| Trabajo y borradores | `areas/<área>/` | Responsable del área |
| Bitácora y perfil | `equipo/<persona>/` | Solo su dueño |
| Decisiones | `contexto/decisiones.md` | Todos, agregando al final |
| Errores de uso de IA | `registro/errores.csv` | Todos, con `/metodo:error` |
| Contexto y roles | `contexto/proyecto.md`, `gobernanza/roles.md`, `CLAUDE.md` | Quien administra el proyecto |
| Preferencias personales | `CLAUDE.local.md` | Su dueño; no se sube |

## Cómo gastar menos tokens

- Una tarea por sesión. Al cambiar de tema, cierra y abre una sesión nueva.
- Usa el modelo intermedio por defecto. El más potente, solo para diseño o problemas difíciles.
- Desactiva los conectores que este proyecto no usa.
- No pidas "lee todo el proyecto". Indica el archivo o el área.
- El traspaso entre sesiones lo hacen la bitácora y las tareas; no hace falta alargar una conversación para "no perder el hilo".

## Actualizar la metodología

Dentro de una sesión:

```
/plugin marketplace update metodologia-workspace
```

Para recibir las versiones nuevas automáticamente: `/plugin` → Marketplaces → `metodologia-workspace` → Enable auto-update.

## Si Git muestra un conflicto

Los comandos se detienen y dejan tu trabajo guardado en tu equipo. No uses opciones de fuerza. Avisa a la persona con cuyo cambio chocaste y resuélvanlo juntos; después vuelve a ejecutar `/metodo:cierre`.
