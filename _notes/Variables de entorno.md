---
title: "Variables de entorno"
---
# Variables privadas
- Existen variables a las que no deben acceder el cliente. Por ejemplo una key.
- Para ocultar esas variables, deben estar ocultas en un archivo: `env.local` ubicado en la carpeta raíz.
- Las variables de React deben iniciar con `REACT_APP_`.

## Ejemplo
- Una variable `REACT_APP_NOT_SECRET_CODE` se expondrá en JS como `process.env.REACT_APP_NOT_SECRET_CODE`.

Fuente:
https://create-react-app.dev/docs/adding-custom-environment-variables/