# Bandit Niveau 11 → Niveau 12
```sh
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ man tr
bandit11@bandit:~$ cat data.txt | tr abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ nopqrstuvwxyzabcdefghijklmNOPQRSTUVWXYZABCDEFGHIJKLM
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv [le MDP]
bandit11@bandit:~$ exit
```
`tr:` permet de traduire ou de supprimer des caractères dans une chaîne de texte. Le nom "tr" signifie "translate" ou "transliterate". La commande prend en entrée une chaîne de texte et applique des transformations sur les caractères de cette chaîne, selon les options spécifiées.<br>
Petit rappel : `man`(abbréviation de "manuel"): permet d'afficher les pages de manuel (ou "manpages") de différents programmes et commandes disponibles (sur un système Unix ou Unix-like).<br>
Les pages de manuel fournissent une documentation détaillée sur les différentes options, les arguments et l'utilisation générale d'une commande;

# Bandit Niveau 12 → Niveau 13
```sh
bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ cat data.txt
......
......
bandit12@bandit:~$ cd /tmp

bandit12@bandit:/tmp$ mkdir dean
mkdir: cannot create directory ‘dean’: File exists
bandit12@bandit:/tmp$ cd dean
bandit12@bandit:/tmp/dean$ ls
data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ cd
bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ cp data.txt /tmp/dean
bandit12@bandit:~$ cd /tmp/dean
bandit12@bandit:/tmp/dean$ ls
data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ man xxd
bandit12@bandit:/tmp/dean$ ls
data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ xxd -r data.txt
@4Aڀh4C@hd2@hF4XdBGaB~6VAGf͌>G`wBx)B׭xk|IFDs>R4"^d!P^g!)O^1IF       7kFx,2=l [ĵF7YxXHF;ň<AVPIdJ-Se'yu3_1��Ft#^haX"l=]fwDZo,AB
4@weRI7}8v9H;uH%}$iKL12v)|Rib AN]BA>Y|.Ebandit12@bandit:/tmp/dean$ xxd -r data.txt data2.txt
bandit12@bandit:/tmp/dean$ ls
data2.txt  data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ file data2.txt
data2.txt: gzip compressed data, was "data2.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix, original size modulo 2^32 581
bandit12@bandit:/tmp/dean$ mv data2.txt data2.bin.gz
bandit12@bandit:/tmp/dean$ ls
data2.bin.gz  data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ gunzip data2.bin
bandit12@bandit:/tmp/dean$ ls
data2.bin  data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ file data2.bin
data2.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/dean$ mv data2.bin data2.bin.bz2
bandit12@bandit:/tmp/dean$ ls
data2.bin.bz2  data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ file data2.bin
data2.bin: cannot open `data2.bin' (No such file or directory)
bandit12@bandit:/tmp/dean$ ls
data2.bin.bz2  data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ file data2.bin.bz2
data2.bin.bz2: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/dean$ bunzip2 data2.bin.bz2
bandit12@bandit:/tmp/dean$ ls
data2.bin  data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ file data2.bin
data2.bin: gzip compressed data, was "data4.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/dean$ mv data2.bin data4.bin.gz
bandit12@bandit:/tmp/dean$ ls
data4.bin.gz  data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ gunzip data4.bin.gz
bandit12@bandit:/tmp/dean$ ls
data4.bin  data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ file data4.bin
data4.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/dean$ man tar
bandit12@bandit:/tmp/dean$ ls
data4.bin  data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ mv data4.bin data5.bin.tar
bandit12@bandit:/tmp/dean$ ls
data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ tar -xf data5.bin.tar
bandit12@bandit:/tmp/dean$ ls
data5.bin  data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/dean$ mv data5.bin data5.bin.tar
bandit12@bandit:/tmp/dean$ ls
data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ tar -xf data5.bin.tar
bandit12@bandit:/tmp/dean$ ls
data5.bin.tar  data6.bin  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/dean$ mv data6.bin data7.bin bz2
mv: target 'bz2' is not a directory
bandit12@bandit:/tmp/dean$ mv data6.bin data7.bin.bz2
bandit12@bandit:/tmp/dean$ ls
data5.bin.tar  data7.bin.bz2  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ bunzip2 data7.bin.bz2
bandit12@bandit:/tmp/dean$ ls
data5.bin.tar  data7.bin  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ file data7.bin
data7.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/dean$ mv data7.bin data8.bin.tar
bandit12@bandit:/tmp/dean$ ls
data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ tar -xf data8.bin.tar
bandit12@bandit:/tmp/dean$ ls
data5.bin.tar  data8.bin  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ tar -xf data8.bin.tar
bandit12@bandit:/tmp/dean$ ls
data5.bin.tar  data8.bin  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix, original size modulo 2^32 49
bandit12@bandit:/tmp/dean$ mv data8.bin data9.bin.gz
bandit12@bandit:/tmp/dean$ ls
data5.bin.tar  data8.bin.tar  data9.bin  data9.bin.gz  data.txt
bandit12@bandit:/tmp/dean$ gunzip data9.bin.gz
gzip: data9.bin already exists; do you wish to overwrite (y or n)? y
bandit12@bandit:/tmp/dean$ ls
data5.bin.tar  data8.bin.tar  data9.bin  data.txt
bandit12@bandit:/tmp/dean$ file data9.bin
data9.bin: ASCII text
bandit12@bandit:/tmp/dean$ cat data9.bin
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw  [le MDP]
bandit12@bandit:/tmp/dean$ exit
```
`cp:` permet de copier des fichiers et des répertoires;<br>
`xxd:` permet de convertir une représentation hexadécimale d'un fichier en sa forme binaire;<br>
`file:` permet d'identifier le type de contenu d'un fichier. Elle affiche des informations sur le format du fichier;<br>
`mv:` permet de déplacer ou de renommer des fichiers ou des dossiers. Pour déplacer un fichier ou un dossier, il suffit de lui donner le nom du fichier ou du dossier en premier argument, suivi du nom du dossier de destination;<br>
`gunzip:` permet de décompresser des fichiers compressés avec le format de compression gzip;<br>
`tar -xf:` pour extraire les fichiers d'une archive tar. L'option '-x' est utilisée pour extraire les fichiers, et l'option '-f' est utilisée pour spécifier le nom du fichier d'archive;<br>
<br>
`.bin`: extesion pour des fichiers binaires, qui sont des fichiers contenant des données binaires brutes, c'est-à-dire des données non textuelles;<br>
`.gz:` extension pour des fichiers compressés avec le format de compression gzip. Pour décompresser un fichier gzip avec l'extension ".gz", vous pouvez utiliser la commande `gunzip ` ou `gzip -d`;<br>
`.bz2:` extenson pour des fichiers compressés avec le format de compression bzip2. Pour décompresser un fichier bzip2 avec l'extension ".bz2", vous pouvez utiliser la commande `bunzip2` ou `bzip2 -d`;<br>
`.tar:` extension pour des fichiers compressés avec le format de compression bzip2. Pour décompresser un fichier bzip2 avec l'extension ".bz2", vous pouvez utiliser la commande `bunzip2` ou `bzip2 -d`;<br>
`.bin.tar:`  une archive tar qui a été préalablement convertie en un fichier binaire

Petit rappel : `cd [répértoire]:` commande très utile pour naviguer dans les répertoires;
 
# Bandit Niveau 13 → Niveau 14
```sh
bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ cat sshkey.private
........
........
........
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p 2220
........
..........
.........
bandit14@bandit:~$ 
```
`ssh -i:` pour se connecter à un serveur distant en utilisant une clé privée spécifique plutôt qu'un mot de passe. L'option '-i' est utilisée pour spécifier le chemin d'accès à la clé privée.<br>
Pour plus d'approfondissement sur les clés privés et les clés publiques : https://help.ubuntu.com/community/SSH/OpenSSH/Keys
# Bandit Niveau 14 → Niveau 15
```sh
bandit14@bandit:~$ ls
bandit14@bandit:~$ cd /etc/bandit_pass/
bandit14@bandit:/etc/bandit_pass$ ls
bandit0   bandit11  bandit14  bandit17  bandit2   bandit22  bandit25  bandit28  bandit30  bandit33  bandit6  bandit9
bandit1   bandit12  bandit15  bandit18  bandit20  bandit23  bandit26  bandit29  bandit31  bandit4   bandit7
bandit10  bandit13  bandit16  bandit19  bandit21  bandit24  bandit27  bandit3   bandit32  bandit5   bandit8
bandit14@bandit:/etc/bandit_pass$ cat bandit1
cat: bandit1: Permission denied
bandit14@bandit:/etc/bandit_pass$ cat bandit2
cat: bandit2: Permission denied
bandit14@bandit:/etc/bandit_pass$ cat bandit10
cat: bandit10: Permission denied
bandit14@bandit:/etc/bandit_pass$ cat bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:/etc/bandit_pass$ echo fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq | nc localhost 30000
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt  [le MDP]

bandit14@bandit:/etc/bandit_pass$ exit
```
`echo:` pour afficher du texte à l'écran ou pour rediriger ce texte vers un fichier ou un autre processus;<br>
`nc`(netcat): est un outil de communication en réseau qui peut être utilisé pour créer des connexions réseau, envoyer des données à des serveurs et recevoir des données de serveurs
