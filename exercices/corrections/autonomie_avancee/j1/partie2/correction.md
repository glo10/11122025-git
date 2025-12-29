# Correction partie II J1 : consolidation

1. Question (Q) : créez une nouvelle branche *feature/j1/p2*
```bash
# Réponse (R)
git checkout main # toujours depuis main la création d'une nouvelle branche
git checkout -b feature/j1/p2
```
2. Q : créez le fichier *README.md* avec une autre liste d'objet.
- R : cf [README.md](README.md)
3. Q : faites une capture d’écran de l’état de votre dépôt et enregistrez le fichier dans le dossier *img/*.
- R : cf dossier [img/](./img/)
4. Q : effectuez un commit votre travail en respectant les bonnes pratiques de commit [voir l'annexe partie commits](./../annexe.md).
```bash
# Réponse (R)
git add README.md img/
git commit -m "feat: new fruits"
```
5. Q : faites une nouvelle capture d’écran de votre dépôt et enregistrez le fichier dans le dossier *img/*.
- R : cf dossier [img/](./img/)
6. Q : retirez la ligne contenant *img* dans le *.gitignore*.
- R : cf fichier [.gitignore](./.gitignore)
7. Q : effectuez un commit
```bash
# Réponse (R)
git commit -am "refactor: remove img/ from .gitignore"
```