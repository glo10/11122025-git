# Correction partie 4 : mettre de côté les films et séries

Vous créez une nouvelle branche pour faire une sélection des films et séries à regarder durant ses vacances de fin d'année dans un fichier *netflix.md*.
A 20% de la fin de cette liste, votre entourage vous demande de modifier la playlist. Pour ne pas perdre votre travail en cours, vous avez décidé :
- tout d'abord, de le mettre de côté vos modifications
- ensuite de modifier la playlist
- enfin, de revenir sur la branche dédiée aux films et séries pour terminer votre travail.
```bash
# R
## Création de la nouvelle branche pour ajouter des films et séries
git checkout main
git checkout -b feature/netflix
touch netflix.md # remplissez ce fichier avec des films et séries
## Tout d'abord, mettre de côté les modifications en cours
git stash
## Ensuite, se déplacer sur la branche feature/playlist pour faire des modifications
git checkout feature/playlist
### Modifier le fichier playlist.md et effectuez un commit
git add playlist.md
git commit -m "refactor: update playlist"
## Enfin, appliquer les modifications mises de côté + terminer + commit
git stash apply
git add netflix.md
git commit -m "feat: add movies and series"
```