# Exercice en autonomie

**PS : Avec le jargon technique**

## Prérequis :

- Utilisez la [convention de nommage d'Angular](https://www.conventionalcommits.org/en/v1.0.0/) pour vos messages de commit et vos branches.

## Partie 1

1. Créer un nouveau dossier de travail
2. Initialisez un dépôt git
3. Faites la liaison entre votre dépôt local et le dépôt distant sur gitHub, GitLab ou BitBucket
4. Créez un fichier *.gitignore* dont le contenu doit exclure le sous-dossier *img*.
5. Faites votre premier commit
6. Renommez le nom de la branche *master* en *main* 
7. Créez et (dé)placez-vous dans une branche nommée *feature/ex-part1*
8. Créez un sous-dossier *img*
9. Ajouter le fichier *.gitkeep* dans *img*.
10. Commitez en respectant la convention de nommage Angular.
11. Créez fichier README.md à la racine contenant une liste des objets de votre choix parmi la liste suivante ou à partir de votre imagination débordante :
- Fruits
- Voitures
- Sandwich
- Jeux
- Films
- Etc.
12. Effectuez un ou plusieurs commits sur cette branche *feature/ex-part1*

---

## Partie 2

1. Créez un nouvelle branche *feature/ex-part2*
2. Créez le fichier *README.md* avec une autre liste d'objet.
3. Faites une capture d’écran de l’état de votre dépôt et enregistrez le fichier dans le sous-dossier *img/*.
4. Effectuez un commit votre travail en respectant les bonnes pratiques de commit [voir l'annexe partie commits](./../annexe.md).
4. Faites à nouveau une capture d’écran de votre dépôt et enregistrez le fichier dans le sous-dossier *img/*.
5. Retirez la ligne contenant *img* dans le *.gitignore*.
6. Effectuez un commit

---

## Partie 3

1. Toujours dans la branche *feature/ex-part2*, effectuez des changements, ajoutez ses changements sans écrire un nouveau message de commit.
2. Modifiez le dernier message de commit par un autre message.

### Aide

1. Commitez sans modifier le dernier message de commit : `git commit --amend --no-edit`
2. Commitez en modifiant le dernier message de commit (sans en créer un nouveau) : `git commit --amend`
- Votre éditeur (celui configuré à l'installation) s'ouvre et vous pouvez éditer votre message puis l'enregistrer.

#### Cas particulier éditeur VIM

1. Tapez sur la touche *Echap* puis sur la lettre `i` pour passer en mode édition.
2. Modifier votre message de commit
3. Tapez sur le bouton `Echap` pour quitter le mode d'édition.
4. Tapez sur les touches `:x` pour enregistrer les modifications et quitter l'éditeur.

---

## Partie 4

1. Fusionnez la branche *feature/ex-part1* dans la branche *main*.
- En cas de conflit, résolvez le conflit en lisant le diapo du cours 57
2. Fusionnez la branche *feature/ex-part2* dans la branche *main*.
- En cas de conflit, résolvez le conflit en lisant le diapo du cours 57
3. Créez une nouvelle branche *feature/ex-part4* à partir de la branche *main* propre.
4. Modifiez le fichier *README.md* en ajoutant d'autres objets.
5. Effectuez un commit en respectant les bonnes pratiques.
6. Fusionnez la branche *feature/ex-part4* dans la branche *main*.
7. Envoyez toutes vos modifications (branches *feature/ex-part1*, *feature/ex-part2*, *feature/ex-part3* et *main*) vers votre dépôt distant GitHub.
