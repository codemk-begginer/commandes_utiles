# Commandes docker
## Crée et lancer un conteneur 
```bash
docker run <nom de l\'image>

```

## Affecter l'id d'une cle gpg a docker 
```bash
    pass init <id de la cle gpg>
```

##lister les cle gpg 
```bash
      gpg --list-keys
 ```
 ##generer une nouvelle cle gpg
```bash
     gpg --full-generate-key
```

## Lister les conteneurs en cour d'exécution

```bash
     docker ps
```
```bash
   docker container ps

```

### Lister tous les conteneurs 

```bash
docker container ps -a

```

## Lister les images 

```bash
docker images

```

## supprimer un conteneur 

```bash
docker container rm <id du conteneur a supprimer >

```
```bash
docker rm <id du conteneur a supprimer > 

```

## Supprimer une image 

```bash
docker image rm <id de l\'image >

```

```bash
docker rmi <id de l\'image>

```

## Lancer un conteneur et interagir 

```bash
docker run -it <nom de l\'image >

```

## Lancer un conteneur et le supprimer automatiquement

```bash
docker run -it --rm <nom de l\'image>

```

## Redémarer un conteneur 

```bash
docker docker start <id conteneur>

```

## Arreter un conteneur 

```bash
docker stop <id conteneur>

```

## entrer et interagir dans un conteneur déjas démarer

```bash
docker exec -it <id conteneur> bash

```

## redémarer et interagir avec un conteneur en une ligne de commande 

```bash
docker start -ai <id conteneur>

```

## Télécharger une image 

```bash
docker pull <nom de l\'image>

```

## Volumes

### Mappé un volume

```bash
docker run -it --rmm <dossier local>:<dossier du conteneur> <nom de l'image>

```

### Managé un volume 
 
## Créer un volume

```bash
docker volume create <nom du volume>

```

## Lister les volumes 

```bash
docker volume ls

```

## supprimer un volume 

```bash
docker volume rm <nom du volume >

```

## Relier un volume manager 

```bash
docker run -it --rm -v <nom du volume>:<dossier conteneur> <image>

```

## Information du volume 

```bash
    docker volume inspect <nom du volume>
```

## Dockerfile

### Construire une image 

```bash
docker built -t <image> .

```

### Ajouter l'image au dockerhub

```bash
docker tag <image> <repository>
docker push <repository>

"il faudra se connecter a docker via le terminal "

```

### verifier le status de docker depuis le terminal 
```bash
     sudo systemctl status docker
```
### demarer docker depuis le terminal 

```bash
   sudo systemctl start docker
```
 
### arreter docker depuis le terminal 
```bash
    sudo systemctl stop docker
```
   
### verifier le status de docker desktop depuis le erminal 

```bash
    systemctl --user status docker-desktop
```

### demarer docker desktop depuis le terminal 
```bash
    systemctl --user start docker-desktop
```
 
 ### arreter docker desktop depuis le terminal 
```bash
    systemctl --user stop docker-desktop
```
 
 ### ajouter un tag a une image docker
```bash
 docker tag image_name username_docker_hub/image_name:1.0
```

### pusher son image sur docker hub
```bash
 docker push username_docker_hub/image_name:1.0
```

### creer un reseau docker externe 
```bash
    docker network create applications-network
```

### Afficher les logs d'un conteneur docker depuis le terminal
```bash
      docker logs <nom du conteneur>
```
### Exporter une base de donnees  spécifique dans un containner docker
```bash
     docker exec -t postgres_db \
     pg_dump -U postgres nom_base > dump.sql
```

** docker exec → exécute une commande dans le conteneur **

** pg_dump → outil natif PostgreSQL **

** -U postgres → utilisateur **

** nom_base → base à exporter **

** > dump.sql → redirection vers ton système hôte **















