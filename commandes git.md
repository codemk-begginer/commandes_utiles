### afficher les remotes et leur url assocer a un repertoire git en local **
```bash 
      git remote -v
```

### changer le remote associer a un repertoire git en local 
```bash 
     git remote set-url origin  https://github.com/codemk-begginer/cwa_spring_security_course.git
```
  
### (Optionnel) Si vous voulez supprimer puis ré-ajouter le remote :
```bash
    git remote remove origin
    git remote add origin <nouvelle_url>
```


##afficher l'historique des commits

```bash
    git log 
    git log --oneline
    git log --oneline --all
```
 
### revenir sur un commit en particulier 
 
```bash
      git reset --hard <id_du_commit>
```

### modifier le message du dernier commit 
 
```bash
     git --amend
 ```
  
### ajouter une modification sur le dernier commit effectuer 

```bash
     git commit --amend --no-edit
```
     
### changer de branche en la creant si elle n'existe pas 

```bash
     git checkout -b <nom de la branche>     
```
    
### changer de branche  
 ```bash
     git checkout  <nom de la branche>
```
    
### fusioner deux branches 

```bash
      git merge feature/style    
``` 
    
### supprimer une branche en local  

```bash
      git branch -D feature/styles     
```

  
### supprimer une branche distant  

```bash
        git push origin --delete feature/styles     
```
    
## voir les differences qui ont ete appliquer sur la branche principale  

```bash
        git diff main
```    
