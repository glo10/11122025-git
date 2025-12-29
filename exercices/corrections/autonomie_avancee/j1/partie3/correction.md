# Correction J1 Partie III : modifier un message de commit

1. Question  (Q): toujours dans la branche *feature/j1/p2*, effectuez des changements, ajoutez ses changements sans écrire un nouveau message de commit.
```bash
# Réponse (R)
git add README.md # add cherry
git commit --amend --no-edit
```
2. Q : modifiez le dernier message de commit par un autre message.
```bash
# R
git commit --amend
# 1. Tapez ECHAP + i pour passer en mode insertion
# 2. Remplacez le message actuel par un nouveau
# "refactor: remove img/ from .gitignore"  remplacé par "refactor: follow img/"
# 3. Tapez ECHAP + : + x pour quitter le mode insertion et enregistrer
git log --oneline # pour vérifier que le dernier message a bien été modifié
```