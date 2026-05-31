# EXAMPLE: BUILD FEATURE

## Input del usuario

Usa `WORKFLOWS/build-feature.md` y `ROLES/senior-engineer.md`.

Quiero añadir una funcionalidad para exportar a PDF el informe final del diagnóstico.  
El proyecto usa React en frontend y un backend con generación de informes.  
Necesito una solución realista, no una idea abstracta.

## Output esperado

### Objetivo
Añadir exportación a PDF del informe final del diagnóstico sin romper el flujo actual de visualización y descarga existente.

### Supuestos y restricciones
- El informe ya existe en formato visual o estructurado dentro del sistema.
- El stack actual debe respetarse.
- Se prefiere una solución incremental frente a una reescritura del módulo de informes.

### Diseño propuesto
La solución recomendada es generar el PDF en backend a partir de una representación estructurada del informe, en lugar de renderizar el DOM del frontend de forma frágil.  
El frontend solo desencadena la acción, muestra el estado y descarga el resultado.

### Archivos afectados
- módulo de generación de informes en backend;
- endpoint de exportación;
- componente frontend del informe;
- capa de cliente API.

### Plan de implementación
1. Confirmar el formato de datos del informe.
2. Crear o adaptar una función de render a PDF en backend.
3. Exponer un endpoint de descarga.
4. Añadir botón y estados de carga en frontend.
5. Validar con informes reales y casos incompletos.

### Validación
- El PDF se genera sin errores con un informe completo.
- El PDF se descarga correctamente.
- Si faltan datos, el sistema responde con error controlado.
- El flujo actual del informe no se rompe.

### Riesgos
- Dependencia del formato real del informe.
- Diferencias entre vista HTML y salida PDF.
- Posibles tiempos de generación altos si el informe es pesado.
