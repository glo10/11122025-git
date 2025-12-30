# Correction J1 partie VII : tag et application des modifications mises de côté

1. Question (Q) : créez une nouvelle branche nommée *feature/j1/p7* à partir de votre branche *main*.
```bash
# Réponse (R)
git checkout main
git checkout -b feature/j1/p7
```
2. Q : modifiez le fichier *README.md* en ajoutant encore d'autres objets.
- cf [README.md](README.md)
3. Q : effectuez un commit en respectant les bonnes pratiques
```bash
# R
git commit -am "feat: add movies from feature/j1/p7"
```
4. Q : revenez sur la branche *feature/j1/p6*.
```bash
# R
git checkout feature/j1/p6
```
5. Q : récupérez le travail mis de côté (`git stash apply`) et effectuez un nouveau commit
```bash
# R
git stash apply
git commit -am "feat: add movies from feature/j1/p6"
```
6. Q : fusionnez la branche *feature/j1/p6* dans votre branche *feature/j1/p7*.
```bash
# R
git checkout feature/j1/p7
git merge feature/j1/p6
```
7. Q : résolvez le conflit et effectuez un commit de résolution de conflit.
- R : en cas de conflit, résolvez le conflit.
8. Q : fusionnez la branche *feature/j1/p7* dans la branche *main*.
```bash
# R
git checkout main
git merge feature/j1/p7
```
9. Q : ajoutez une version(tag) au dernier commit (`git tag v1.0.0`)
```bash
# R
git tag v1.0.0
```
10. Q : analysez l'état de votre dépôt à l'aide de la commande `git log`
```bash
# R
git log
```
11. Q : envoyez toutes vos branches locales vers votre dépôt distant GitHub.
```bash
# R
git push
git push --tag # pour envoyer également les tags
```
12. Q : en local, supprimez toutes les branches sauf la branche *main* (pour supprimer une branche `git branch -d branch_name`)

PS : avec l'option `-d`, s'il y a des travaux qui n'ont pas été mergés sur la branche principale, *Git* empêchera la suppression de la branche.
Avec l'option `-D`, la suppression est immédiate peu importe si la branche a été fusionnée ou non dans *main*.
```bash
# R
git branch -d feature/j1/p1
git branch -d feature/j1/p2
git branch -d feature/j1/p4
git branch -d feature/j1/p5
git branch -d feature/j1/p6
git branch -d feature/j1/p7
```