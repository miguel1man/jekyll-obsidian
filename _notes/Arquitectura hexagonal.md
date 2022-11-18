También conocida como patrón **puertos y adaptadores**.

## Capas de la arquitectura hexagonal
1. Infraestructura: DB, axios, fetch, etc
2. Aplicación (Casos de uso): Crear un usuario, publicar un post, etc.
3. Dominio (Entidades o modelos): User, post, etc.

- La infraestructura hace llamadas al caso de uso, el cual conecta con el dominio. 
- La lógica de dominio solamente se puedellamar a sí misma. User solamente pued llamar a user ID o user name. 

https://medium.com/@edusalguero/arquitectura-hexagonal-59834bb44b7f