# Correction exercice 2.1 : prise en main de git

1. Question (Q) : effectuez les configurations minimales à l'aide la commande `git config`

```bash
# Réponse (R)
git config --global user.name 'glodie-tshimini'
git config --global user.email 'contact@tshimini.fr'
```
- Permet de faire la configuration minimale requise nom et email pour pouvoir associer les futures modifications à un auteur unique.
2. Q : utilisez la commande `git config --help` pour voir la documentation complète de cette commande
```bash
# R
git config --help
```
- `--help` sur n'importe quelle commande `git` donne la documentation de celle-ci
3. Q : effectuez la commande `git config --list` pour voir le résultat
```bash
# R
git config --list
```
- Permet de voir la liste de paramètres qui peuvent être modifiés
4. Q : Modifiez une variable de la configuration de Git de votre choix
```bash
# R
git config --local help.format=info
```
- Modification de l'affichage de la documentation, par défaut une page web HTML, les autres valeurs sont *man, html* et *web*

5. Q : Créez un nouveau dossier dans l'emplacement de votre choix et initialisez un nouveau projet Git dessus
```bash
# R
# Vérifiez le dossier courant
pwd
# Si vous n'êtes pas au bon endroit, déplacez-vous vers le bon dossier avec la commande cd
cd vers/le/nouveau/dossier
# Commande Git qui vous permet d'initialiser un nouveau projet Git
git init
```
6. Questions 6, 7 et 8, création des dossiers avec des fichiers *.gitkeep* dans chaque dossier pour pouvoir versionner les dossiers. Un dossier vide n'est pas pris en compte par Git, il faut donc créer *.gitkeep* pour versionner ce dernier.

PS : normalement les dossiers admin/ config/ ne devraient pas être présent dans le dépôt distant, ils sont présents à cause de l'option -f du `git add -f` qui permet malgré la présence du fichier ou du dossier dans le *.gitignore* de le versionner