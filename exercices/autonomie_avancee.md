# Exercice en autonomie

**PS : Avec le jargon technique**

## Prérequis :

- Utilisez la [convention de nommage d'Angular](https://www.conventionalcommits.org/en/v1.0.0/) pour vos messages de commit et vos branches.

## Partie 1 : les bases

1. Créer un nouveau dossier de travail
2. Initialisez un dépôt git
3. Faites la liaison entre votre dépôt local et le dépôt distant sur gitHub, GitLab ou BitBucket
4. Créez un fichier *.gitignore* dont le contenu doit exclure le sous-dossier *img*.
5. Faites votre premier commit
6. Renommez le nom de la branche *master* en *main* 
7. Créez et (dé)placez-vous dans une branche nommée *feature/ex-part1*
8. Créez un sous-dossier *img*
9. Ajouter le fichier *.gitkeep* dans *img*.
10. Effectuez un commit en respectant la convention de nommage Angular.
11. Créez fichier README.md à la racine contenant une liste des objets de votre choix parmi la liste suivante ou à partir de votre imagination débordante :
- Fruits
- Voitures
- Sandwich
- Jeux
- Films
- Etc.
12. Effectuez un ou plusieurs commits sur cette branche *feature/ex-part1*

---

## Partie 2 : les bases

1. Créez une nouvelle branche *feature/ex-part2*
2. Créez le fichier *README.md* avec une autre liste d'objet.
3. Faites une capture d’écran de l’état de votre dépôt et enregistrez le fichier dans le sous-dossier *img/*.
4. Effectuez un commit votre travail en respectant les bonnes pratiques de commit [voir l'annexe partie commits](./../annexe.md).
4. Faites à nouveau une capture d’écran de votre dépôt et enregistrez le fichier dans le sous-dossier *img/*.
5. Retirez la ligne contenant *img* dans le *.gitignore*.
6. Effectuez un commit

---

## Partie 3 : modifier un message commit

1. Toujours dans la branche *feature/ex-part2*, effectuez des changements, ajoutez ses changements sans écrire un nouveau message de commit.
2. Modifiez le dernier message de commit par un autre message.

### Aide

1. Effectuez un commit sans modifier le dernier message de commit : `git commit --amend --no-edit`
2. Effectuez un commit en modifiant le dernier message de commit (sans en créer un nouveau) : `git commit --amend`
- Votre éditeur (celui configuré à l'installation) s'ouvre et vous pouvez éditer votre message puis l'enregistrer.

#### Cas particulier éditeur VIM

1. Tapez sur la touche *Echap* puis sur la lettre `i` pour passer en mode édition.
2. Modifier votre message de commit
3. Tapez sur le bouton `Echap` pour quitter le mode d'édition.
4. Tapez sur les touches `:x` pour enregistrer les modifications et quitter l'éditeur.

---

## Partie 4 : fusion des branches

1. Fusionnez la branche *feature/ex-part1* dans la branche *main*.
- En cas de conflit, résolvez le conflit en lisant le diapo du cours 57
2. Fusionnez la branche *feature/ex-part2* dans la branche *main*.
- En cas de conflit, résolvez le conflit en lisant le diapo du cours 57
3. Créez une nouvelle branche *feature/ex-part4* à partir de la branche *main* propre.
4. Modifiez le fichier *README.md* en ajoutant d'autres objets.
5. Effectuez un commit en respectant les bonnes pratiques.
6. Fusionnez la branche *feature/ex-part4* dans la branche *main*.
7. Envoyez toutes vos modifications (branches *feature/ex-part1*, *feature/ex-part2*, *feature/ex-part3* et *main*) vers votre dépôt distant GitHub.

---

## Partie 5 : Dépôt distant

Depuis votre compte GitHub, à partir du dépôt où vous avez envoyé précédemment votre travail.
1. Créez une nouvelle branche *feature/ex-part5* à partir de la branche *main* depuis GitHub.
2. Modifiez le fichier *README.md* en ajoutant encore d'autres objets depuis GitHub.
3. A partir d'ici, toutes les opérations se font en local, effectuez un commit en respectant les bonnes pratiques depuis GitHub.
4. Récupérez les modifications du dépôt distant (aide commande à effectuer `git checkout -b feature/ex-part5 --track origin/feature/ex-part5`).
5. Fusionnez la branche *feature/ex-part5* dans la branche *main* en local.

---

## Partie 6 : Mettre de côté les modifications

1. Créez une nouvelle branche nommée *feature/ex-part-6* à partir de la branche *main* en local.
2. Modifiez le fichier *README.md* encore d'autres objets.
3. Mettez votre travail de côté (à l'aide de la commande `git stash`)

---

## Partie 7 : tag et application des modifications mises de côté

1. Créez une nouvelle branche nommée *feature/ex-part7* toujours à partir de votre branche *main*.
2. Modifiez le fichier *README.md* en ajoutant encore d'autres objets.
3. Effectuez un commit en respectant les bonnes pratiques
4. Revenez sur la branche *feature/ex-part6*.
5. Récupérez le travail mis de côté (`git stash apply`) et effectuez un nouveau commit
6. Fusionnez la branche *feature/ex-part6* dans votre branche *feature/ex-part7*.
7. Résolvez le conflit et effectuez un commit de résolution de conflit.
8. Fusionnez la branche *feature/ex-bonus/part-7* dans la branche *main*.
9. Ajoutez une version(tag) au dernier commit (`git tag v1.0.0`)
10. Analysez l'état de votre dépôt à l'aide de la commande `git log`
11. Envoyez vers votre dépôt distant GitHub toutes vos branches locales
12. En local, supprimez toutes les branches sauf la branche *main* (pour supprimer une branche `git branch -d branch_name`)

PS : avec l'option `-d`, s'il y a des travaux qui n'ont pas été mergé sur la branche principale, *Git* empêchera la suppression. 
Avec l'option `-D`, la suppression est immédiate peu importe l'état de la branche.
