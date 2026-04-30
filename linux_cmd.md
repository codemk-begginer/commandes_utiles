### Afficher la date et l'heure 
```bash
       date
```

### Afficher tous le contenue d'un repertoire meme les fichiers cacher 
```bash
     ls -a
```

### Revenir en arriere sur deux repertoire 
```bash
    cd ../..
```

### Crer des dossier intermediaires 
```bash
    mkdir -p animaux/vertebres/chat
```

### Copier un dossier 
```bash
     cp -R 
```

### Copier tous les fichier d'un type precis 

```bash
    cp *.jpg mondossier/
```
### Copier tous les fichiers qui commence par une lettre precise

```bash
    cp so* mondossier/
```
### deplacer un fichier ou un dossier 
```bash
    mv 
```
###Le deplacement d'un fichier est similaire a la copie memme pour
###l'utilisation du joker (*) encore appeler wildcard 

### Renomer un fichier 
```bash
    mv nom_du_fichier nouveau_nom
```

### Deplacer et renommer des fichier ou dossier en memme temps 
```bash
    mv countcopie mondossier/supercountcopie.txt
```

### Le paramettre -v permet de demander des details de l'execution
## d'une commande
```bash
    rm -v fichierbidon fichiercopie
```

### Supprimer un dossier 
```bash
       rm -r nom_du_dossier_a_supprimer 
```

###lister les partitions et leurs informations
```bash
     lsblk -f
```

###changer le proprietaire d'une partition et son groupe. le -R permet d'affecter egalements les sous dossiers et fichiers au meme groupe et aux meme usrs
```bash 
    sudo chown -R stevemk:stevemk /media/stevemk/3C56-D97B
```
 
 ### installer un fichier  deb
 
```bash 
       cd /Downloads- sudo dpkg -i microsoft_online_apps.deb
```
### changer le proprietaire d'un fichier 
```bash
     chown stevemk rapport.txt
```
### verifier qu'un package existe bien sur apt
```bash
    apt show openssl
```

### installer un package
```bash
 sudo apt install openssl
```

### desinstaller un package 
```bash
 sudo apt purge openssl
```
### generer un mot de passe random avec openssl
```bash
  openssl rand -base64 32
```

### changer le proprietaire d'une fichier et son groupe
```shell
   chown patrick:amis rapport.txt
```

### modifier des droit sur tous les fichiers .html en utilisant des chiffres. le -R permet d'affecter egalement les droits aux sous dossiers et fichiers
```bash
   chmod 777 *.html
   chmod -R 777 /home/stevemk/Desktop/Test
```
### modifier les droit sur tous les fichier .html en utilisant des lettres
```bash
   chmod g-wx,o-rwx *.html
```

### afficher les allias
```bash
   alias
```
### definir un alias sur ne commande (dans le fichier bashrc)
```bash
  alias rm='rm --preserve-root'
```

### rechercher un package dans la liste disponible en cache
```bash
  apt-cache search breakout
```

### pour voir plus de details sur un paquet 
```bash
     apt-cache show lbreakout2
```
### desinstaller un paquet et toute ces dependances
```bash
     apt-get autoremove lbreakout2
```
### afficher le mannuel d'une commande
```bash
     man cp
```

### rechercher un fichier dans une base de donnee 
```bash
     locate notes.txt 
```

### rechercher un fichir dans un repertoire precis
```bash
     find "où" -name "quoi" "que faire avec" 
```

### rechercher un mot dans un fichier 
```bash
    grep alias .bashrc
```

### trier le contenue d'un fichier par ordre alphabetique
```bash
    sort noms.txt
```

### trier des nombres
```bash
    sort -n nombres.txt
```

### compter le nombre de mots ,le nombre de ligne et le nombre d'octets
```bash
    wc noms.txt
```

### supprimer les doublons. cette commande ne fonctionne que sur des listes triee.
```bash
    uniq doublons.txt
```

### Couper une parie du fichier a l'aide d'un delimiteur
#### -d : indique quel est le délimiteur dans le fichier
#### -f : indique le numéro du ou des champs à couper
```bash
    cut -d , -f 1 notes.csv
```
### Rediriger le resultat d'une commande dans un fichier
```bash
    cut -d , -f 1 notes.csv > eleves.txt
```
### Si vous ne voulez pas voir ce que retourne une commande ou vous ne voulez pas l'eregistrer dans un fichier

```bash
    commande_bavarde > /dev/null
```
### enregistrer la sortie d'erreur d'une commande dans un fichier

```bash
   cut -d , -f 1 fichier_inexistant.csv > eleves.txt 2> erreurs.log
```
### envoyer le contenue d'ubn fichier en paramettre a une commande

```bash
   cat < notes.csv
```
### envoyer les paramettre a une commande avec le clavier

```bash
   sort -n << FIN
```

### passer la sortie d'une commande en paramettre a une autre

```bash
   cut -d , -f 1 notes.csv | sort > noms_tries.txt
```

### afficher les infrmations sur les utilisateurs et le systeme

```bash
    w
```

### lister les processus en arriere plan pour l'utilisateur courrant 

```bash
    ps
```

### lister les processus lancer par tous les utilisateurs

```bash
    ps -ef
```

### lister les processus lancer par un utilisateur precis 

```bash
    ps -u stevemk
```

### lister les processus avec un affichage dynamique 

```bash
    top
```

### tuer un processus qui tourne en arriere plan 

```bash
    kill PID...
```
### tuer un processus sans lui laisser le temps de s'arreter proprement 

```bash
    kill -9 PID...
```

### tuer un processus et ses copies en utilisant son nom 

```bash
    killall find...
```
### arreter l'ordinateur en console 

```bash
    sudo halt
```

### redemarrer l'ordinateur depuis la console  

```bash
    sudo reboot
```
### faire passer l'execution d'une commande en arriere plan

```bash
    cp video.avi copie_video.avi &
```
### detacher le processus lancer en arriere plan de la console  

```bash
    nohup cp video.avi copie_video.avi
```

### mettre en pause un processus 
```bash
    ctrl + z
```

### passer le processus en arriere plan apres l'avoir mis en pause  

```bash
    bg
```

### faire passer un processus de l'arriere plan au premier plan

```bash
    fg %numero du processus
```

### creer plusieurs consoles en une seule

```bash
    screen
```

### detacher screen de la console

```bash
    ctrl + a  d
```
### diviser screen en plusieur parties

```bash
    ctrl + a s
```

### mettre en veille un onglet de screen

```bash
    screen -r 
```

### afficher les screen actuellement ouvert

```bash
    screen -ls
```

### programmer l'execution d'une commande

```bash
    at "informations sur la date et l'heure a la quelle la commande doit etre execute"
```

### lister les jobs en attente

```bash
    atq
```

### supprimer les jobs en attente

```bash
    atrm "numero du job a supprimer"

```

### enchainer plusieurs commandes

```bash
    touch fichier.txt; rm fichier.txt
```

### ajouter une pause entre les commandes

```bash
    touch fichier.txt; sleep 10; rm fichier.txt ou touch fichier.txt && sleep 10 && rm fichier.txt
```

### afficher la liste des crontab disponible

```bash
    crontab -l
```

### modifier le fichier crontab

```bash
    crontab -e
```

### programmer une tache dans le crontab

```bash
   47 15 * * * touch /home/mateo21/fichier.txt >> /home/mateo21/cron.log
```

### cree une archive avec un dossier contenant plusieurs fichiers

```bash
   tar -cvf nom_archive.tar nom_dossier/
   
   -c : signifie "créer" une archive tar.
   -v : signifie afficher le détail des opérations.
   -f : signifie assembler l'archive dans un fichier.

```

### voir le contennue d'une archive tar

```bash
   tar -tf tutoriels.tar
```


