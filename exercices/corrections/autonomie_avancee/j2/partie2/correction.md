# Correction J2 partie 2 : modifier votre historique

4. Question : vous décidez de faire un *rebase* pour n'avoir qu'un seul commit de toutes les modifications que vous avez effectué sur votre projet en utilisant la commande `git rebase --help`
```bash
# Réponse 
git rebase --soft ID_PREMIER_COMMIT
git commit -m "feat: add todolist, menu, playlist and animation"
```