Decrypt my super sick RSA. (c, n, e=65537)
## Solución
Descargué los valores con c, n y e=65537. El módulo n es de solo ~270 bits, muy por debajo de lo seguro (2048+), así que se puede factorizar. Lo pasé por FactorDB y salieron los dos primos p y q. Con ellos calculé phi=(p-1)(q-1), d = inverso de e módulo phi y descifré m = c^d mod n. En esta instancia de CyLab los bytes salen en orden inverso, así que invertí la cadena para obtener el formato normal:

academy{sma11_N_n0_g0od_a3ac7152}
## Notas Adicionales
- n de 270 bits se factoriza en segundos (FactorDB / ECM / Pollard rho).
- Detalle: el texto descifrado venía al revés (termina en }ymedaca), por eso se invierte.
## Referencias
