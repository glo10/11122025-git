# Correction partie I J1

1. Question (Q) : créez un nouveau dossier de travail
2. Q : initialisez un dépôt git
```bash
# Réponse (R)
# Au préalable, placez-vous dans votre dossier de travail depuis le terminal
git init
```
3. Q : effectuez la liaison entre votre dépôt local et le dépôt distant sur gitHub, GitLab ou BitBucket
```bash
# R en remplaçant https://github.com/glo10/11122025-git.git par l'URL de votre dépôt distant
git remote add origin https://github.com/glo10/11122025-git.git
```
4. Q : créez un fichier *.gitignore* excluant le dossier *img*.
- R : cf [.gitignore](./.gitignore)
```bash
# R contenu du fichier .gitignore
**/img # ** tous les niveaux des dossiers, parent, dossier, sous sous-dossier, etc.
```
5. Q : effectuez votre premier commit
```bash
# R
git add .gitignore
git commit -m "first commit"
```
6. Q : renommez le nom de la branche *master* en *main* 
```bash
# R
git branch -M main
```
7. Q : créez et (dé)placez-vous dans une branche nommée *feature/j1/p1*
```bash
# R
git checkout -b feature/j1/p1
```
8. Q : créez un dossier *img*
- R : cf. [/img/](./img/)
9. Q : ajoutez le fichier *.gitkeep* dans *img*.
- R : cf. [/img/.gitkeep](./img/.gitkeep)
10. Q : effectuez un commit en respectant la convention de nommage Angular.
```bash
# R
# Pour versionner le dossier /img/, 2 options soit enlever le dossier du .gitignore
# soit faire un git add -f img/
git add -f img/
git commit -m "refactor: add folder /img/"
```
11. Q : créez un fichier README.md à la racine contenant une liste des objets de votre choix parmi la liste suivante ou à partir de votre imagination débordante :
- Fruits
- Voitures
- Sandwich
- Jeux
- Films
- Etc.
```bash
# R
```
- cf [README.md](README.md)
12. Q : effectuez un ou plusieurs commits sur cette branche *feature/j1/p1*
```bash
# R
git add README.md
git commit -m "refactor: add README.md"
```