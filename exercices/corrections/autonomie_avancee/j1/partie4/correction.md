# Correction J1 partie IV : fusion des branches

## Rappels résolution conflit

Contexte d'utilisation ou d'application : un fichier ou plusieurs fichiers à un ou plusieurs emplacements (endroits) ont été modifiés chacun de leur côté sur chacune de deux branches à fusionner. *Git* ne sait pas qu'elle version garder et vous place dans une branche temporaire, il fait la fusion de 2 versions combinées de ce fichier en y ajoutant des caractères spéciaux (***===, <<<***) pour distinguer le contenu de chaque version et vous demande de trancher en choisissant soit :
- Conserver l'une des 2 versions
- Créer une nouvelle version (en combinant les deux, créant une résultante, etc).
A la fin de votre résolution de conflit sur tous les fichiers ayant des conflits, vous devez effectuer un commit pour revenir sur la branche courante ou la commande `git merge` a été effectuée.

## Questions/réponses

1. Question (Q): fusionnez la branche *feature/j1/p1* dans la branche *main*.
- En cas de conflit, résolvez le conflit en lisant le diapo du cours 57 et/ou en vous appuyant sur les explications ci-dessus
```bash
# Réponse (R)
git checkout main
git merge feature/j1/p1
# En cas de conflit, résolvez le conflit et effectuez un commit du style "fix: conflict ..."
```
2. Q : fusionnez la branche *feature/j1/p2* dans la branche *main*.
- En cas de conflit, résolvez le conflit en lisant le diapo du cours 57 et/ou en vous appuyant sur les explications ci-dessus
```bash
# Réponse (R)
git checkout main
git merge feature/j1/p2
# En cas de conflit, résolvez le conflit et effectuez un commit du style "fix: conflict ..."
```
3. Q : créez une nouvelle branche *feature/j1/p4* à partir de la branche *main* propre.
```bash
# R
git checkout main
git checkout -b feature/j1/p4
```
4. Q : modifiez le fichier *README.md* en ajoutant d'autres objets.
- R : cf [README.md](./README.md)
5. Q : effectuez un commit en respectant les bonnes pratiques.
```bash
# R
git add README.md
git commit -m "feat: add video games"
```
6. Q : fusionnez la branche *feature/j1/p4* dans la branche *main*.
```bash
# R
git checkout main
git merge feature/j1/p4
```
7. Q : envoyez toutes vos modifications (branches *feature/j1/p1*, *feature/j1/p2*, *feature/j1/p4* et *main*) vers votre dépôt distant GitHub.
```bash
# R
git checkout feature/j1/p1
git push -u feature/j1/p1
git checkout feature/j1/p2
git push -u feature/j1/p2
git checkout feature/j1/p4
git push -u feature/j1/p4
git checkout main
git push -u main
```