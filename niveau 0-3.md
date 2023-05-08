# Bandit Niveau 0
Pour Commencer un jeu, bien sûr qu'il y a y toujours un commencement. A ce niveau, il est encore très facile même pour un débutant car tout ce qu'il faut est déjà dans le sujet.

Bien, pour commencer il ne vous faudra ouvrir votre invite de commandes, et de juste exécuter cette `commande` :
```sh
votre_nom_d'utilisateur> ssh bandit0@labs.overthewire.org -p 2220
```
```sh
`ssh`: pour se connecter à un serveur distant de manière sécurisée à travers un réseau;
`bandit[0 → 34]`: nom d'utilisateur que vous souhaitez utiliser pour vous connecter au serveur;
`bandit.labs.overthewire.org`: nom de l'hôte que vous souhaitez vous connecter;
`p 2220`: spécifie le port SSH que vous souhaitez utiliser pour vous connecter au serveur;
`l`: pour préciser le nom de l'utilisateur (en Englais c'est `localhost`)
=>  le nom d'utilisateur peut être spécifié directement après le nom d'hôte avec un `@`.
```

`Rappel :` à chaque MDP trouvé, vous faites appel à `exit`, et refait appel, d'ordre croissant, à : 
```sh
ssh bandit[1 → 34]@labs.overthewire.org -p 2220
```

# Bandit Niveau 0 → Niveau 1
à partir d'ici je vais juste mettre les commandes utilisés, conséquence de chaque commande, et les expliquer ensuite. <br>
Les lignes où il y a `bandit[0 → 34]@bandit:~$` sont les lignes où on invite les commandes, en bas, les conséquences. Attention, parfois ça n'affiche rien, non pas parce que la commande est fausse mais on ne voit juste pas des yeux ce qui ce passe derrière. Si la commande est fausse, on sera toujours prevenu par l'invite de commande.  
```sh
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL  [le MDP]
bandit1@bandit:~$ exit
```
`ls:` permet d'afficher une liste des fichiers et des répertoires dans le répertoire courant;<br>
`cat:` permet d'afficher le contenu d'un ou plusieurs fichiers sur la sortie standard

# Bandit Niveau 1 → Niveau 2
```sh
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi [le MDP]
bandit1@bandit:~$ exit
```
Pour comprendre le `cat ./-`, veuillez vous diriger ici : https://tldp.org/LDP/abs/html/special-chars.html ou là : https://www.google.com/search?q=dashed+filename

# Bandit Niveau 2 → Niveau 3
```sh
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG [le MDP]
bandit2@bandit:~$ exit
```
 Pour comprendre le `cat spaces\ in\ this\ filename`, veuillez vous diriger ici : https://www.google.com/search?q=spaces+in+filename
