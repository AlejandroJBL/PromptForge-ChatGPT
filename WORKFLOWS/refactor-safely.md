# WORKFLOW: REFACTOR SAFELY

Usa este workflow cuando el usuario quiera mejorar código existente sin cambiar el comportamiento esperado más de lo necesario.

## Objetivo

Reducir complejidad, mejorar claridad o preparar evolución futura minimizando riesgo de regresión.

## Secuencia de trabajo

### 1. Entender el alcance
Identifica:
- qué parte se quiere refactorizar;
- por qué;
- qué comportamiento debe mantenerse;
- qué restricciones existen.

### 2. Revisar el contexto
Consulta:
- stack;
- estándares de código;
- arquitectura existente;
- dependencias y puntos de integración.

### 3. Separar objetivos
Distingue entre:
- limpieza mínima;
- mejora estructural;
- refactor mayor;
- rediseño.

### 4. Diseñar una estrategia segura
Prioriza:
- cambios pequeños;
- pasos reversibles;
- aislamiento de responsabilidades;
- validación frecuente.

### 5. Proponer ejecución
Incluye:
- archivos afectados;
- orden recomendado;
- riesgos;
- pruebas necesarias.

### 6. Validar
Define:
- qué debe seguir funcionando igual;
- qué puntos son sensibles;
- cómo detectar regresiones.

## Formato de salida recomendado

1. Objetivo del refactor
2. Alcance y límites
3. Estrategia recomendada
4. Archivos afectados
5. Riesgos
6. Validación
