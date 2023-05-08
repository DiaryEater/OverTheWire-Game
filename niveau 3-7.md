# Bandit Niveau 3 → Niveau 4
```sh
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe [le MDP]
bandit3@bandit:~/inhere$ exit
```
`cd [répértoire]:` commande très utile pour naviguer dans les répertoires;<br>
`ls -a:` pour afficher tous les fichiers dans le répertoire courant, y compris les fichiers cachés;<br>
`cat .hidden:` afficher le contenu du fichier ".hidden" dans le répertoire courant

# Bandit Niveau 4 → Niveau 5
```sh
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  inhere  .profile
bandit4@bandit:~$ cd inhere
bandit4@bandit:~/inhere$ ls -a
.  ..  -file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ ls -file00
`ls: invalid option -- 'e'
Try 'ls --help' for more information.`
bandit4@bandit:~/inhere$ cat -- -file00
ŰBηb<QȠ+ViO1[5{ bandit4@bandit:~/inhere$ cat -- -file06
'cwk^jM;,co9 bandit4@bandit:~/inhere$ cat -- -file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR [le MDP]
bandit4@bandit:~/inhere$ exit
```
il faut trouver le bon fichier en commençant de '-file00' à '-file09'.<br>
`cat --` est utilisée pour indiquer à la commande `cat` que les arguments qui suivent doivent être traités comme des noms de fichiers et non pas comme des options de commande

# Bandit Niveau 5 → Niveau 6
```sh
bandit5@bandit:~/inhere$ ls -l
total 80
drwxr-x--- 2 root bandit5 4096 Apr 23 18:04 maybehere00
drwxr-x--- 2 root bandit5 4096 Apr 23 18:04 maybehere01
...........
drwxr-x--- 2 root bandit5 4096 Apr 23 18:04 maybehere18
drwxr-x--- 2 root bandit5 4096 Apr 23 18:04 maybehere19
bandit5@bandit:~/inhere$ find . -readable -size 1033c ! -executable
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU [le MDP]
bandit5@bandit:~/inhere$ exit
```
`ls -l:` pour afficher une liste de fichiers et de répertoires dans un répertoire donné, avec des informations détaillées telles que les permissions, la taille, la date de dernière modification, etc <br>
`find:` pour rechercher des fichiers et des répertoires dans une arborescence de fichiers à partir d'un point de départ spécifié

# Bandit Niveau 6 → Niveau 7
```sh
bandit6@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  .profile
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c
... 
/var/lib/dpkg/info/bandit7.password  (on copicolle celui-ci parmi beaucoup d'autre)
...
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S [le MDP]
bandit6@bandit:~$ exit
```
Petit rappel : `ls -a:` pour afficher tous les fichiers dans le répertoire courant, y compris les fichiers cachés
