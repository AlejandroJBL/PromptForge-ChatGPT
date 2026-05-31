# WORKFLOW: DEBUG ISSUE

Usa este workflow cuando el usuario quiera diagnosticar y resolver un error, bug o comportamiento inesperado.

## Objetivo

Encontrar la causa raíz más probable y proponer una corrección segura y verificable.

## Secuencia de trabajo

### 1. Capturar el problema
Recoge:
- síntoma observado;
- mensaje de error;
- contexto;
- pasos para reproducir;
- archivos implicados;
- momento desde el que ocurre.

### 2. Separar hechos de hipótesis
Distingue entre:
- lo que está confirmado;
- lo que es probable;
- lo que aún no puede saberse.

### 3. Formular hipótesis
Propón una lista priorizada de causas probables.

### 4. Diseñar comprobaciones
Indica qué revisar primero:
- logs;
- configuración;
- flujo de datos;
- dependencias;
- estados no inicializados;
- cambios recientes.

### 5. Proponer corrección
La propuesta debe incluir:
- causa raíz más probable;
- cambio recomendado;
- impacto esperado;
- riesgos de regresión.

### 6. Validar
Define cómo comprobar que el problema queda resuelto y qué no debe romperse.

## Formato de salida recomendado

1. Problema observado
2. Hechos confirmados
3. Hipótesis priorizadas
4. Causa raíz más probable
5. Solución propuesta
6. Validación
7. Riesgos
