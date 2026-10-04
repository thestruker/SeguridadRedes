Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. As an aspiring cookie detective, your mission is to uncover this delectable secret. Can you outsmart Cookie Monster and find the hidden recipe?
## Solución
Para resolver este reto de la categoría Web / Cookies, donde el valor almacenado en las galletas de la sesión del navegador se encontraba codificado, se realizó un proceso de decodificación en dos etapas (URL Encoding y Base64).

1. Extraje el valor almacenado en la cookie del navegador, el cual presentaba caracteres codificados para transmisión URL:
    

```
YWNhZGVteXtjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzXzIyRTgzQzg1fQ%3D%3D
```

2. Decodifiqué la secuencia de escape URL reemplazando `%3D%3D` por su equivalente ASCII `==`, obteniendo la cadena limpia en Base64:
    
3. Decodifiqué la cadena Base64 para revelar el contenido original en texto plano.
    
4. La flag obtenida al decodificar la cookie es:
    

`academy{c00k1e_m0nster_l0ves_c00kies_22E83C85}`

## Notas Adicionales


## Referencias
