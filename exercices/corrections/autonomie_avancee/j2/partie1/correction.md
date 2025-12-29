# Correction J2 partie 1 : planter le décor

1. Question (Q) : pour chaque élément, créez une nouvelle branche et ajoutez le contenu puis effectuez un commit.
Les différents fichiers sont :
- **TODO.md**
- **menu.md**
- **playlist.md**
- **animation.md**
```bash
# Réponse (R)
# Au préalable, il faut faire un 1er commit sur la branche principale avant de commencer la création des nouvelles branches
# Premier commit
touch README.md
git add README.md
git commit -m "first commit"
git branch -m Main # uniquement si la branche courante se nomme master
# Travail branche todolist
git checkout -b feature/todolist
touch TODO.md # remplissez ce fichier avec du contenu
git commit -am "feat: add todolist"
# Travail branche menu
git checkout main
git checkout -b feature/menu
touch menu.md # remplissez ce fichier avec du contenu
git commit -am "feat: add menu"
# Travail branche playlist
git checkout main
git checkout -b feature/playlist
touch playlist.md # remplissez ce fichier avec du contenu
git commit -am "feat: add playlist"
# Travail branche animation
git checkout main
git checkout -b feature/animation
touch animation.md # remplissez ce fichier avec du contenu
git commit -am "feat: add animation"
```
2. Votre entourage vous demande de créer une nouvelle *playlist*, vous décidez de créer une nouvelle *playlist* dans une nouvelle branche avec un nouveau fichier *playlist.md* à la racine du projet.
```bash
# R
git checkout main
git checkout -b feature/playlist-family
touch playlist.md # remplissez ce fichier avec du contenu, idéalement différent du contenu de la branche feature/playlist
```
3. Vous avez fini de remplir le contenu de vos fichiers depuis leur branche respective, vous décidez de tout fusionner dans *main* et de résoudre le conflit sur les playlists
```bash
# R
git checkout main
git merge feature/todolist
git merge feature/menu
git merge feature/playlist
git merge feature/animation
git merge feature/playlist-family
```
- Resolvez le conflit comme nous l'avons abordé dans le cours page 57 et dans les exercices précédents