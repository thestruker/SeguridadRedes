Our flag printing service has started glitching!
1

ASCII is one of the most common encodings used in programming

2

We know that the glitch output is valid Python, somehow!

3

Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

## Solución
```
MSI:/mnt/host/c/Users/adomi/Downloads# nc saturn.picoctf.net 53358
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'

PS C:\Users\adomi> py
Python 3.14.0 (tags/v3.14.0:ebf955d, Oct  7 2025, 10:15:03) [MSC v.1944 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> print("picoCTF{gl17ch_m3_n07_" + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) \+ chr(0x65) + "}")
picoCTF{gl17ch_m3_n07_a4392d2e}
```

## Notas Adicionales
Sustituir el codigo que regresa por un print para que lo realice python de alguna manera

## Referencias
