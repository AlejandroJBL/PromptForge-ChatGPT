# CODING STANDARDS

Este archivo define cómo debe proponer, escribir o modificar código el asistente.

## Principios generales

- Prioriza claridad sobre cleverness.
- Prefiere código mantenible a trucos compactos.
- Minimiza efectos secundarios.
- Haz explícitas las decisiones importantes.
- Reduce ambigüedad en nombres y estructuras.

## Reglas de implementación

- No cambies más de lo necesario.
- Mantén el alcance de la modificación bajo control.
- Si hay una solución incremental razonable, priorízala.
- Si una refactorización mayor es recomendable, sepárala del arreglo inmediato.
- No mezcles corrección, rediseño y optimización sin avisar.

## Nombres

- Usa nombres descriptivos.
- Evita abreviaturas opacas.
- Mantén consistencia con el naming existente si es suficientemente bueno.
- Si el naming actual es malo, propón mejora, pero no renombres en masa sin motivo.

## Estructura

- Una responsabilidad principal por módulo o archivo, cuando sea razonable.
- Separa utilidades, lógica de dominio y presentación.
- Evita archivos gigantes si el sistema ya permite modularidad.
- No fragmentes artificialmente un archivo si eso empeora la comprensión.

## Errores

- No silencies errores importantes.
- Los mensajes de error deben ayudar a diagnosticar.
- Si una operación puede fallar, la propuesta debe contemplarlo.
- Diferencia errores esperables de errores inesperados.

## Logs

- Los logs deben servir para depurar, no para contaminar.
- No añadas logs verbosos permanentes sin necesidad.
- Si propones logs temporales de diagnóstico, indícalo claramente.

## Dependencias

- No añadas dependencias por comodidad menor.
- Justifica nuevas librerías por impacto real en calidad, velocidad o mantenibilidad.
- Si algo puede resolverse bien con el stack actual, evita ampliar superficie técnica.

## Comentarios

- No comentes lo obvio.
- Usa comentarios para explicar intención, decisiones o riesgos.
- Prefiere código claro antes que código oscuro comentado.

## Entrega de código

Cuando el usuario lo prefiera:
- entrega archivos completos;
- indica la ruta exacta del archivo;
- evita fragmentos ambiguos;
- deja claro si el contenido sustituye todo el archivo o solo una parte.

## Validación

Toda propuesta de cambio debe incluir, cuando aplique:
- cómo probarla;
- qué comportamiento se espera;
- qué podría romperse;
- cómo revertir o aislar el cambio si falla.

## Regla para el asistente

No escribas código como demostración abstracta si el usuario necesita una solución aplicable.  
Prioriza código realista, integrado y coherente con el contexto del proyecto.
