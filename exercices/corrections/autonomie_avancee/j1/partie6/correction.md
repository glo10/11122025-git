# Correction J1 partie 6 : mettre de côté les modifications en cours

1. Question (Q) : créez une nouvelle branche nommée *feature/j1/p6* à partir de la branche *main* en local.
```bash
git checkout main
git checkout -b feature/j1/p6
```
2. Q : modifiez le fichier *README.md* en ajoutant d'autres objets.
- R : cf [README.md](./README.md), même contenu que précédemment, les modifications avec l'ajout des films par exemple ont été mises de côté avec `git stash`
3. Q : mettez votre travail de côté (à l'aide de la commande `git stash`)
```bash
# R
git stash # va mettre de côté vos modifications en cours qui n'ont pas été commité
```