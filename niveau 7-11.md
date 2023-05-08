# Bandit Niveau 7 → Niveau 8
```sh
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ cat data.txt
...
...
... (des et des tas de trucs)
...
... 
bandit7@bandit:~$ man grep
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP [le MDP]
bandit7@bandit:~$ exit
```
`man`(abbréviation de "manuel"): permet d'afficher les pages de manuel (ou "manpages") de différents programmes et commandes disponibles (sur un système Unix ou Unix-like).<br>
Les pages de manuel fournissent une documentation détaillée sur les différentes options, les arguments et l'utilisation générale d'une commande;<br>
`grep:` elle est généralement utilisée pour filtrer les lignes d'un fichier qui correspondent à un modèle particulier, ou pour rechercher une chaîne de caractères spécifique dans un grand nombre de fichiers

# Bandit Niveau 8 → Niveau 9
```sh
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ cat data.txt
......
......
......
bandit8@bandit:~$ sort data.txt | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t [le MDP]
bandit8@bandit:~$ exit
```
`sort:` pour trier et manipuler de grandes quantités de données dans un environnement Unix (elle peut être utilisée en combinaison avec d'autres commandes);<br>
`uniq -u:` permet d'afficher uniquement les lignes uniques d'un fichier ou d'un flux de données

# Bandit Niveau 9 → Niveau 10
```sh
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ cat data.txt
....
....
....
bandit9@bandit:~$ strings data.txt | grep "=="
4========== the#
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s [le MDP]
bandit9@bandit:~$ exit
```
`strings:` permet d'extraire et d'afficher les chaînes de caractères lisibles dans un fichier binaire (elle est souvent utilisée pour extraire des chaînes de caractères à partir de fichiers binaires tels que des exécutables, des bibliothèques partagées, des fichiers d'image, etc.);<br>
Petit rappel : `grep:` elle est généralement utilisée pour filtrer les lignes d'un fichier qui correspondent à un modèle particulier, ou pour rechercher une chaîne de caractères spécifique dans un grand nombre de fichiers

# Bandit Niveau 10 → Niveau 11
```sh
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ base64 -d data.txt
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM [le MDP]
bandit10@bandit:~$ exit
```
`base64 -d:` permet de décoder une chaîne de caractères codée en Base64
