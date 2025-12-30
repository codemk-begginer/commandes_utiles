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

###changer le proprietaire d'une partition et son groupe  
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
