The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. Can you extract all the information from this strange file?
## Solución
Descargué flag2of2-final.pdf. Con el comando file vi que en realidad empieza como PNG, es un archivo políglota: válido como PNG y como PDF al mismo tiempo. Abierto como imagen (renombrándolo a .png) mostraba la primera parte de la flag: "academy{f1u3n7_". Abierto como PDF (o con pdftotext) mostraba la segunda parte: "1n_pn9_&_pdf_becdff18}". Uniendo ambas:

academy{f1u3n7_1n_pn9_&_pdf_becdff18}
## Notas Adicionales
- Comandos: file flag2of2-final.pdf ; cp flag2of2-final.pdf a.png (ver imagen) ; pdftotext flag2of2-final.pdf -
## Referencias
