My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?
## Solución
```
dastruker-academy@webshell:~/drop-in$ ls
flag.py
dastruker-academy@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

dastruker-academy@webshell:~/drop-in$ git status
On branch main
nothing to commit, working tree clean

dastruker-academy@webshell:~/drop-in$ git config user.name "pico"   
dastruker-academy@webshell:~/drop-in$ git config user.email "pico@gmail.com"     
dastruker-academy@webshell:~/drop-in$ git branch -a
  feature/part-1
  feature/part-2
  feature/part-3
* main
  
  
  dastruker-academy@webshell:~/drop-in$ git merge feature/part-1
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
dastruker-academy@webshell:~/drop-in$ git merge feature/part-2
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
dastruker-academy@webshell:~/drop-in$ git merge feature/part-3
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
dastruker-academy@webshell:~/drop-in$ nano flag.py 
dastruker-academy@webshell:~/drop-in$ git merge feature/part-3
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
dastruker-academy@webshell:~/drop-in$ nano flag.py 
dastruker-academy@webshell:~/drop-in$ 
dastruker-academy@webshell:~/drop-in$ git add flag.py
dastruker-academy@webshell:~/drop-in$ git commit -m "Merge feature/part-2"
[main 73c29f6] Merge feature/part-2
dastruker-academy@webshell:~/drop-in$ git merge feature/part-3
Auto-merging flag.py
CONFLICT (content): Merge conflict in flag.py
Automatic merge failed; fix conflicts and then commit the result.
dastruker-academy@webshell:~/drop-in$ nano flag.py


dastruker-academy@webshell:~/drop-in$ python flag.py 
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_4c24302f}
```

## Notas Adicionales
Branches y commits