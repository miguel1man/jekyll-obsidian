## ¿Cómo subir a la nube las carpetas que están fuera de OneDrive?
- Abrir CMD con permisos de administrador.
- Escribir: `mklink ruta-acceso-directo carpeta-existente-a-sincronizar /D`

## Ejemplo
- Escribir: `mklink C:\User\OneDrive\Test2 C:\Test1 /D`
- Se creará la carpeta `Test 2` dentro de Onedrive con los archivos de `Test1`.
- `Test 2` es similar a un "Acceso directo".
- Los archivos no se sincronizan automáticamente en OneDrive, es necesario reiniciar el programa para que se reconozcan los archivos dentro del acceso directo.

***

- Enlace: https://poweruserguide.com/how-to-sync-folders-outside-of-onedrive/