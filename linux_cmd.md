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
