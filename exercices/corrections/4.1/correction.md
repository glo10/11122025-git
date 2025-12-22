# Exercice 4.1 : travailler en équipe au jour le jour

## Correction Partie I 

1. Question (Q) : A la suite de l'exercice 2.1, créez un fichier *README.md* contenant la liste des ingrédients de votre sandwich préféré, un ingrédient par ligne comme dans l'exemple ci-après.
- Réponse (R): [regarder le fichier README.md](./README.md)

2. Q: Exécutez la commande `git status` pour voir l'état de votre dépôt.
- R : 
```bash
git status
```
Avec cette commande on devrait voir que git détecte la création du nouveau fichier et vous indique de faire un `git add`

3. Q : Effectuez votre premier commit avec la commande `git commit -m "first commit"`
- R : Avant d'effectuer cette commande il faut au préalable ajoute au moins un fichier dans l'index avec la commande `git add README.md`
```bash
# Cette commande fait un git add grâce à l'option -a et un commit
git commit -am "first commit" 
# Ou décomposer avec les commandes suivantes
git add .
git commit -m "first commit"
# git add . , avec le point, git ajoute tous les fichiers et dossiers du dossier courant dont le status est nouveau ou modifiés (ne prend pas en compte les fichiers traqués qui ont été supprimmés)
# Autres alternatifs
# - "git add README.md un_autre_fichier.txt un_dossier/", ici vous ajoutez vos fichiers et dossiers en le séparant par un espace
# - git add --all : ajoute tout, fichiers et dossiers dont le status est nouveau, modifié ou supprimé
``` 

4. Q : Ajoutez une image de votre sandwich préféré dans le dossier */img* 
- R : ajout du lien vers le ficher [img/eiliv-aceron-mAQZ3X_8_l0-unsplash.jpg](./img/eiliv-aceron-mAQZ3X_8_l0-unsplash.jpg) dans le [README.md](README.md)

5. Q : Regardez l'état de votre dépôt
```bash
# R
git status
``` 
- R : avec la commande précédente, vous devez voir que *README.md* a été modifié et que git détecte le nouveau fichier d'image

6. Q : effectuez un second commit avec un message court et clair de vos modifications.
```bash
# R
git commit -am "refactor: add sandwich image"
``` 
7. Q : ajoutez au moins 3 nouvelles photos, effectuez un commit par nouvelle photo.
```bash
# R
# 1ère modification du fichier physique README.md
git commit -am "refactor: update README.md"
# 2eme modification du fichier physique README.md
git commit -am "refactor: another update README.md"
# 3eme modification du fichier physique README.md
git commit -am "refactor: last update README.md"
``` 
- S'il n'y a pas de modification de votre dépôt et ni au moins un fichier dans l'index, la modification ne sera pas pris en compte.

---

## Correction Partie II

8. Q : utilisez la commande `git tag --help` pour voir la documentation de cette commande
```bash
# R
git tag --help
```
9. Ajoutez un nouveau ***tag v1.0.0*** associé au dernier commit
```bash
# R
git tag v1.0.0
```
10. Q : affichez la liste des tags.
```bash
# R
git tag --list
```
11. Q : créez un nouveau fichier burger.md avec la liste des ingrédients
- R : cf [burger.md](burger.md)
12. Effectuez un commit et créer un nouveau ***tag v1.0.1***
```bash
# R
git add burger.md
git commit -m "feat: add burder.md"
git tag v1.0.1
```
13.  Q : créez un dépôt distant sur GitHub et laissez-vous guider par les commandes de GitHub pour faire le lien avec votre dépôt distant et votre dépôt local. 
- R : [vidéo création nouveau repository GitHub](../videos/create-new-repo.mp4)

```bash
# R : 2eme partie de la réponse avec le lien entre repo distant et local
# en remplaçant https://github.com/glo10/new-repo-test.git par l'URL de votre dépôt distant 
git remote add origin https://github.com/glo10/new-repo-test.git
```
---

## Correction Partie III

14. Q : envoyez vos fichiers vers le dépôt distant à l'aide de la commande `git push`
```bash
# Renommage de la branche courante par main
git branch -M main
# Création de la branche distante main avec l'option -u car elle n'existe pas et envoie du local vers le distant 
git push -u origin main
```
15. Q : effectuez les modifications en ligne du fichier *README.md* depuis GitHub en ajoutant dans le *README.md* un sandwich végan
- R : [vidéo des actions à effectuer sur GitHub.com]()
16. Récupérez les modifications effectuées en ligne en local à l'aide de la commande `git pull`
```bash
```
17. Ouvrez le *README.md* et vérifiez que vous avez bel et bien le contenu du sandwich végan
```bash
```

---

## Correction Partie IV

18. Comparez l'état de votre dépôt entre le premier et le dernier commit à l'aide des hashs associées à chaque commit à l'aide de la commande `git diff [hash_premier_commit] [hash_dernier_commit]`
```bash
```
19. Affichez les changements de manière plus détaillée du fichier *README.md*
```bash
```

---

## Correction Partie V

20. Utilisez la commande `git format-patch HEAD -1 -o ./patches` pour extraire les changements du dernier commit dans un fichier *0001-[message-commit].patch* dans le dossier */patches/* (nouvellement crée)
```bash
```
21. Créez un nouveau dossier en dehors votre projet git encore et initialisez un nouveau projet git
- Attention à ne pas initialiser un dépôt git dans un autre dépôt git
```bash
```
22. Effectuez votre premier commit sur ce nouveau dépôt
```bash
```
23. Copiez/collez le dossier */patches/* du premier dépôt au second dépôt (à la racine du projet)
```bash
```
24. Depuis le nouveau dépôt local, exécutez la commande `git am --3way ./patches`
```bash
```
25. Observez le résultat et regardez l'état de votre dépôt ainsi que l'historique des commandes
```bash
```