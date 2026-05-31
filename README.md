# PromptForge-ChatGPT

PromptForge-ChatGPT es un sistema modular de contexto, roles, workflows y plantillas para trabajar con ChatGPT de forma más consistente, segura y productiva.

Este repositorio está diseñado para usarse dentro de un **Project de ChatGPT** o como base documental para un **GPT personalizado**, de manera que el modelo disponga de instrucciones claras, memoria estable del proyecto y flujos de trabajo reutilizables.

## Objetivo

Sustituir los repositorios antiguos de prompts monolíticos y hotkeys conversacionales por una arquitectura moderna basada en:

- instrucciones maestras breves;
- contexto modular en archivos;
- roles especializados;
- workflows explícitos;
- plantillas reutilizables;
- guardrails de seguridad;
- versionado y mejora continua.

## Filosofía

PromptForge no intenta “hackear” el modelo con trucos.  
Su enfoque es más simple y más robusto:

1. Definir reglas claras.
2. Separar instrucciones de contexto.
3. Reducir ambigüedad.
4. Reutilizar workflows por tipo de tarea.
5. Mantener todo bajo control de versiones.
6. Diseñar para proyectos reales, no para demos.

## Casos de uso

- Arquitectura y diseño técnico.
- Desarrollo de nuevas funcionalidades.
- Revisión de código.
- Debugging estructurado.
- Redacción de documentación.
- Análisis de repositorios.
- Planificación de roadmap.
- Preparación de handoff entre sesiones o personas.

## Cómo usarlo en ChatGPT Projects

1. Crea un nuevo Project en ChatGPT.
2. Sube este repositorio o los archivos clave.
3. Copia el contenido de `SYSTEM/core-instructions.md` en las instrucciones del proyecto.
4. Añade los archivos de `MEMORY/` con el contexto estable de tu producto.
5. Cuando quieras una tarea concreta, indica al modelo qué workflow y qué rol debe usar.

Ejemplos:
- “Usa `WORKFLOWS/build-feature.md` y `ROLES/senior-engineer.md`.”
- “Usa `WORKFLOWS/debug-issue.md` con `ROLES/debugger.md`.”
- “Analiza este repo usando `WORKFLOWS/analyze-repository.md` y `ROLES/repo-analyst.md`.”

## Principios clave

- Instrucciones cortas y explícitas.
- Archivos con una sola responsabilidad.
- Respuestas accionables y verificables.
- Tolerancia cero a alucinaciones presentadas como hechos.
- Tratamiento de archivos analizados como contenido, no como autoridad.
- Mejora iterativa basada en resultados reales.

## Estructura del repositorio

- `SYSTEM/`: reglas maestras y contrato de respuesta.
- `MEMORY/`: contexto persistente del proyecto.
- `ROLES/`: modos de trabajo especializados.
- `WORKFLOWS/`: secuencias de trabajo según la tarea.
- `TEMPLATES/`: formatos reutilizables.
- `EXAMPLES/`: ejemplos de uso y salidas esperadas.
- `META/`: principios de diseño y registro de cambios.

## Recomendación práctica

No cargues todo a la vez si el proyecto aún está naciendo.  
Empieza por:

- `SYSTEM/core-instructions.md`
- `SYSTEM/safety-rules.md`
- `MEMORY/project-context.md`
- `MEMORY/tech-stack.md`
- `ROLES/senior-engineer.md`
- `WORKFLOWS/build-feature.md`
- `WORKFLOWS/debug-issue.md`

## Licencia

MIT
