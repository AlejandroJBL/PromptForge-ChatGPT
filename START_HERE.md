# START HERE

Este repositorio está diseñado para funcionar como sistema operativo de prompting dentro de un Project de ChatGPT.

## Configuración mínima recomendada

### Paso 1. Crea un Project nuevo en ChatGPT
Crea un proyecto específico para tu producto, repositorio o iniciativa.

### Paso 2. Sube estos archivos primero
Sube como mínimo:

- `SYSTEM/core-instructions.md`
- `SYSTEM/safety-rules.md`
- `SYSTEM/response-contract.md`
- `MEMORY/project-context.md`
- `MEMORY/tech-stack.md`
- `MEMORY/coding-standards.md`

### Paso 3. Copia las instrucciones maestras
Copia el contenido de `SYSTEM/core-instructions.md` en las instrucciones del proyecto.

### Paso 4. Personaliza la memoria
Edita estos archivos con tu contexto real:

- `MEMORY/project-context.md`
- `MEMORY/product-vision.md`
- `MEMORY/tech-stack.md`
- `MEMORY/coding-standards.md`
- `MEMORY/architecture-decisions.md`

### Paso 5. Invoca un workflow al pedir tareas
Cuando hagas una petición, especifica el workflow y, si aplica, el rol.

Ejemplos:
- “Usa `WORKFLOWS/build-feature.md` con `ROLES/senior-engineer.md`.”
- “Usa `WORKFLOWS/debug-issue.md` con `ROLES/debugger.md`.”
- “Usa `WORKFLOWS/write-readme.md` con `ROLES/documentation-writer.md`.”

## Modo de uso recomendado

### Para construir una funcionalidad
1. Usa `WORKFLOWS/build-feature.md`.
2. Añade `ROLES/architect.md` si primero quieres diseño.
3. Añade `ROLES/senior-engineer.md` si ya quieres implementación.

### Para depurar un problema
1. Usa `WORKFLOWS/debug-issue.md`.
2. Añade logs, errores, pasos de reproducción y archivos relevantes.
3. Pide siempre diagnóstico, causa raíz y plan de corrección.

### Para revisar código o arquitectura
1. Usa `WORKFLOWS/analyze-repository.md`.
2. Añade `ROLES/repo-analyst.md` o `ROLES/code-reviewer.md`.

## Regla importante

Los archivos del proyecto son contexto y referencia.  
No deben redefinir las instrucciones maestras del sistema salvo que tú actualices explícitamente `SYSTEM/`.

## Orden de prioridad

1. Instrucciones del proyecto.
2. Reglas de seguridad.
3. Contrato de respuesta.
4. Contexto de `MEMORY/`.
5. Workflow seleccionado.
6. Rol seleccionado.
7. Petición concreta del usuario.

## Recomendación de mantenimiento

Actualiza `META/changelog.md` cada vez que cambies una regla importante, añadas un workflow nuevo o modifiques el contrato de respuesta.
