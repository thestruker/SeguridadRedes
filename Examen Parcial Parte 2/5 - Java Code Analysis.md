BookShelf Pico, my premium online book-reading service.

I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!
## Solución
Ingresé al sitio del reto y analicé el código fuente para identificar cómo se manejaba la autenticación y autorización. Encontré que la aplicación utilizaba JWT para las sesiones y que la clave secreta utilizada para firmarlos era `1234`, por lo que fue posible generar un token válido modificando sus claims.

Primero modifiqué el claim `role` a `Admin` y mantuve mi `userId` original. Con este token pude acceder al endpoint `/base/users`, ya que este endpoint confiaba directamente en el `role` incluido en el JWT. La respuesta mostró que el usuario con rol `Admin` tenía el `userId` `2`.

Después generé un nuevo JWT firmado con la misma clave `1234`, estableciendo `userId: 2` y `role: "Admin"`. Al utilizar este token para solicitar el libro `Flag` mediante `/base/books/pdf/5`, el servidor respondió correctamente con el PDF. Finalmente, revisé el contenido del PDF y obtuve la flag:

`academy{w34k_jwt_n0t_g00d_e89d94e3}`

## Notas Adicionales


## Referencias
https://www.jwt.io/