# Bandit Niveau 15 → Niveau 16
```sh
bandit15@bandit:~$ ls
bandit15@bandit:~$ cat /etc/bandit_pass/bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
..........
..........
____________
read R BLOCK (Juste une affiche Prédéfinie, au dessous, vous écrivez le code actuel et vous obtenez le prochain MDP ci-après)
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1  [le MDP]
bandit15@bandit:~$ exit
```
`cat /etc/bandit_pass/bandit[0 → 34]:` affiche le MDP actuel;<br>
`openssl s_client -connect:` pour se connecter à un serveur distant en utilisant le protocole SSL

# Bandit Niveau 16 → Niveau 17
```sh
bandit16@bandit:~$ ls
bandit16@bandit:~$ nmap localhost -p 31000-32000
..............
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown (il faut faire le test un à un avec chaque PORT jusqu'à objectif voulu)
31790/tcp open  unknown
31960/tcp open  unknown

bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
.............

(ce sera le 'voulu' quand au bout ça affiche ça)
    Start Time: 1683509322
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
(ici on écrit le MDP actuel) (et on aura une clé Privé ainsi :
Correct!
-----BEGIN RSA PRIVATE KEY----- (on copie tout (Ctrl + C), d'ici ...)
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
...........
..........
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY----- (jusqe là)

closed
bandit16@bandit:~$ mkdir /tmp/bandit35
bandit16@bandit:~$ cd /tmp/bandit35
bandit16@bandit:/tmp/bandit35$ ls
bandit16@bandit:/tmp/bandit35$ nano sshkey.private
Unable to create directory /home/bandit16/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit16@bandit:/tmp/bandit35$ ls
sshkey.private
bandit16@bandit:/tmp/bandit35$ chmod 400 sshkey.private
bandit16@bandit:/tmp/bandit35$ ls
sshkey.private
bandit16@bandit:/tmp/bandit35$ ls -hal
total 1.2M
drwxrwxr-x   2 bandit16 bandit16 4.0K May  8 01:34 .
drwxrwx-wt 175 root     root     1.2M May  8 01:36 ..
-r--------   1 bandit16 bandit16 1.7K May  8 01:34 sshkey.private
bandit16@bandit:/tmp/bandit35$ ssh -i sshkey.private bandit17@bandit.labs.overthewire.org -p 2220
...........

..........
bandit17@bandit:~$
```
`bandit16@bandit:/tmp/bandit35$ nano sshkey.private :` cette ligne nous mènera vers une autre page, et dedans on colle la clé privé que nous venons de copier tout à l'heurre;<br>
`nano:` un éditeur de texte en ligne de commande qui permet de modifier des fichiers texte;<br>
`ls -hal:` permet d'afficher les fichiers et les répertoires dans un format lisible par l'homme et de manière détaillée, en incluant les permissions, les propriétaires, les dates de modification, la taille des fichiers, etc;<br>
`nmap -A`(Network Mapper): pour effectuer une analyse de port détaillée d'un hôte distant;<br>
