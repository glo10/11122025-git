# Correction J1 partie 8 : patch

1. Question (Q) : depuis la documentation de la commande `git format-patch`, créez un patch associé au commit qui a ajouté le sandwich dans le projet. L'extraction de votre patch doit se faire dans le dossier /patches à la racine de votre projet.
```bash
# Réponse (R)
# Remplacez ID_COMMIT_SANDWICH_VEGAN par l'identifiant du commit ayant ajouté le sandwich végan
git format-patch -o ./patches ID_COMMIT_SANDWICH_VEGAN
```
2. Q: créez un nouveau projet Git, en dehors du projet en cours.
```bash
# R
# Se placer en dehors du repertoire courant avec la commande cd puis effectuez la commande suivante
git init
```
3. Q : effectuez un premier commit sur ce nouveau dépôt.
```bash
# R : ajout d'un fichier README.md à la racine vide puis la commande suivante
git add README.md
git commit -m "first commit"
```
4. Q : copiez/collez le dossier patches/ d'un dépôt (celui d'extraction) à l'autre (vers le nouveau, celui qui va l'appliquer)
- R : copiez/collez le dossier patches/ depuis la source du dépôt précédent vers la destination ici [patches](./patches)
5. Q : appliquez le patch extrait du dossier /patches dans le nouveau dépôt.
```bash
git apply --3way ./patches/*
```