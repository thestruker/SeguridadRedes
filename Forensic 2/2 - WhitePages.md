I stopped using YellowPages and moved onto WhitePages... but the page they gave me is all blank!
## Solución
Descargué whitepages.txt, que parecía estar en blanco. Al revisar los bytes vi que en realidad usaba dos tipos de espacio en blanco distintos: el espacio normal (0x20) y el espacio em (U+2003). Eso es esteganografía de espacios: cada tipo representa un bit (0 o 1). Agrupé los bits de 8 en 8 y los convertí a ASCII, obteniendo el texto oculto con la flag:

academy{not_all_spaces_are_created_equal_743510e5f5459071ed7d4109b7832a8e}
## Notas Adicionales
- em-space (U+2003) = 0 y espacio normal (0x20) = 1; decodificando el binario sale la flag.
## Referencias
