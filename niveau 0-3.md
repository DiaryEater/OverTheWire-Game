## N.B :  Je ne pourrais pas vous expliquer toutes les commandes mais au fûr et à mesure que vous les employz, vous comprendriez petit à petit.

Le but est de trouver un mot de passe (à l'aide des commandes) dans le niveau actuel pour enchaîner le niveau suivant.
Quand vous auriez le mot de passe, copiez le (`Ctrl + C`) et mettez le quelques part (comme un bloc notes). Pour le coller dans l'invite de commandes, `click droite`, et `Enter` (P.S : je suis sur Windows). (Si vous préférez) Utilisez "VMWare Workstation Pro" pour simuler un `linux`.
* Bref, commençons ...


# Bandit Niveau 0
Pour Commencer un jeu, bien sûr qu'il y a y toujours un commencement. A ce niveau, il est encore très facile même pour un débutant car tout ce qu'il faut est déjà dans le sujet.

Bien, pour commencer il ne vous faudra juste qu'exécuter cette `commande` :
```sh
ssh -u bandit.labs.overthewire.org -p 2220 -l bandit0
```
`-u`: pour indiquer l'hôte oû vous voulez vous connecter;
`p`: pour le port du réseau;
`l`: pour préciser le nom de l'utilisateur (en Englais c'est `localhost`)


`N.B :`Vous devriez utiliser cette commande à chaque `exit` pour changer d'utilisateur (autrement dit, changer de niveau), et sera :
```sh
ssh -u bandit.labs.overthewire.org -p 2220 -l bandit0
ssh -u bandit.labs.overthewire.org -p 2220 -l bandit1
ssh -u bandit.labs.overthewire.org -p 2220 -l bandit2
...
ssh -u bandit.labs.overthewire.org -p 2220 -l bandit34;
```
et n'oubliez de faire appel à la `commande exit` d'abord à la fin de chaque niveau pour en enchaîner un autre.


# Bandit Niveau 0 → Niveau 1

# Bandit Niveau 1 → Niveau 2
# Bandit Niveau 2 → Niveau 3
 