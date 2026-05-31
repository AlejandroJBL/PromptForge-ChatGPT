# EXAMPLE: DEBUG SESSION

## Input del usuario

Usa `WORKFLOWS/debug-issue.md` y `ROLES/debugger.md`.

En producción, al enviar el formulario de contacto, el usuario ve “Failed to fetch”.  
En local no pasa.  
Quiero diagnóstico y plan de corrección.

## Output esperado

### Problema observado
En producción, el envío del formulario falla con el mensaje “Failed to fetch”, mientras que en local el comportamiento es correcto.

### Hechos confirmados
- El error ocurre solo en producción.
- El fallo aparece al enviar el formulario.
- En local el flujo funciona.

### Hipótesis priorizadas
1. Problema de CORS en el endpoint de producción.
2. Variable de entorno distinta o mal configurada en producción.
3. URL de API incorrecta en el build desplegado.
4. Error del backend sin respuesta visible en cliente.

### Causa raíz más probable
La causa más probable es una diferencia de configuración entre local y producción, especialmente en URL de API o CORS, porque el mismo flujo funciona localmente.

### Solución propuesta
1. Verificar la URL real usada por el frontend en producción.
2. Revisar variables de entorno del despliegue.
3. Comprobar logs del backend.
4. Validar cabeceras CORS y método permitido.
5. Mejorar el manejo de errores del frontend para exponer mejor el fallo real.

### Validación
- Probar envío desde producción tras la corrección.
- Confirmar respuesta HTTP válida.
- Verificar que el usuario recibe feedback correcto.
- Confirmar que local y producción usan configuración coherente.
