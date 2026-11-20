Can you get the flag? Download this binary. Here's the test drive instructions. (gdbme)
## Solución
El reto es una práctica de GDB: el binario gdbme calcula e imprime la bandera, pero el flujo normal nunca llega a esa parte (hay un salto que la evita). Siguiendo las instrucciones del enunciado, abrí el binario en gdb, puse un breakpoint en *(main+99), ejecuté, y con jump *(main+104) forcé al programa a continuar justo en el bloque que imprime la flag. En lote quedó así: gdb -batch -ex 'break *(main+99)' -ex run -ex 'jump *(main+104)' ./gdbme:

academy{d3bugg3r_dr1v3_ff5329f1}
## Notas Adicionales
- Con GDB se puede alterar el flujo de ejecución (jump) para saltar validaciones o llegar a código que normalmente no se alcanza.
- Comando: break *(main+99); run; jump *(main+104).
## Referencias
