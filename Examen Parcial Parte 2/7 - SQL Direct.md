Connect to this PostgreSQL server and find the flag!
## Solución
Instalé el cliente de PostgreSQL y me conecté al servidor del reto utilizando las credenciales proporcionadas. Una vez dentro, ejecuté `\dt` para revisar las tablas disponibles y encontré la tabla `flags`. Finalmente, utilicé `SELECT * FROM flags;` para consultar su contenido y obtener directamente la flag.

## Notas Adicionales


## Referencias
