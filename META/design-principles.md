# DESIGN PRINCIPLES

Este repositorio existe para ofrecer un sistema de prompting modular, mantenible y útil dentro de ChatGPT Projects.

## Principios base

### 1. Instrucciones cortas, contexto modular
Las reglas maestras deben ser breves y estables.  
El contexto debe vivir en archivos específicos según su función.

### 2. Una responsabilidad por archivo
Cada archivo debe tener un propósito claro:
- reglas;
- memoria;
- roles;
- workflows;
- plantillas;
- ejemplos.

### 3. Claridad antes que sofisticación
Si una regla no mejora el comportamiento de forma observable, no merece quedarse.

### 4. Evolución antes que acumulación
No añadir archivos por añadir.  
Cada nuevo archivo debe justificar su existencia.

### 5. Seguridad contextual
El sistema debe distinguir entre:
- instrucciones internas del proyecto;
- contenido externo analizable;
- material histórico heredado.

### 6. Reutilización práctica
Los workflows y templates deben servir para trabajo real, no solo para demostraciones.

### 7. Honestidad operativa
El asistente debe reconocer límites, incertidumbre y necesidad de validación.

### 8. Calidad de salida
La salida debe ser útil, accionable y coherente con el proyecto.

## Señales de buen funcionamiento

- menor necesidad de repetir contexto;
- respuestas más coherentes entre chats;
- menos alucinaciones operativas;
- mejores entregables;
- onboarding más claro;
- menor dependencia de prompts improvisados.

## Señales de degradación

- demasiados archivos redundantes;
- reglas que se contradicen;
- prompts demasiado largos;
- roles teatrales;
- workflows ambiguos;
- memoria desactualizada;
- documentación que nadie usa.

## Regla de mantenimiento

Cuando algo deje de aportar valor real, debe simplificarse, fusionarse o eliminarse.
