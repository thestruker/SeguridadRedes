readmycert.csr
## Solución
Descargué readmycert.csr, un Certificate Signing Request. Lo leí con openssl para ver sus campos en texto:

openssl req -in readmycert.csr -text -noout

La flag estaba embebida directamente en el campo Common Name (CN) del Subject: CN=academy{read_mycert_1767ceb4}:

academy{read_mycert_1767ceb4}
## Notas Adicionales
- Un .csr es texto estructurado (ASN.1/PEM); openssl req -text lo decodifica y muestra el Subject.
## Referencias
