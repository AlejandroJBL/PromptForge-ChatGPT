# EXAMPLE: ARCHITECTURE REVIEW

## Input del usuario

Usa `ROLES/architect.md` y `WORKFLOWS/analyze-repository.md`.

Revisa esta estructura de proyecto y dime si tiene sentido o si debería reorganizarse:
- src/components
- src/pages
- src/lib
- src/utils
- src/hooks
- src/features
- api
- scripts

## Output esperado

### Tipo de repositorio
Aplicación web con separación parcial entre frontend, utilidades y backend ligero o funciones auxiliares.

### Propósito aparente
La estructura busca separar interfaz, lógica reutilizable y áreas funcionales, pero hay señales de posible solapamiento entre `components`, `features`, `lib` y `utils`.

### Hallazgos principales
- `features` es una buena base para organización por dominio.
- `components` puede mezclarse con `features` si no se define bien qué contiene cada carpeta.
- `lib` y `utils` suelen acabar duplicando propósito si no hay criterio claro.
- La presencia de `api` y `scripts` fuera de `src` puede tener sentido si su responsabilidad está bien delimitada.

### Riesgos
- Solapamiento entre carpetas genéricas.
- Dificultad para decidir dónde colocar nuevos archivos.
- Crecimiento caótico del proyecto si no se fija una convención.

### Recomendaciones priorizadas
1. Definir qué vive en `features` y qué vive en `components`.
2. Reservar `components` para piezas verdaderamente compartidas.
3. Unificar criterio entre `lib` y `utils`.
4. Documentar estas reglas en `MEMORY/coding-standards.md`.

### Propuesta de rediseño
Mantener una estructura centrada en dominio:
- `features/` para módulos funcionales;
- `components/shared/` para UI reutilizable;
- `lib/` para integraciones o servicios base;
- `utils/` solo para helpers puros y pequeños;
- `api/` y `scripts/` fuera de `src` si no forman parte del bundle del frontend.
