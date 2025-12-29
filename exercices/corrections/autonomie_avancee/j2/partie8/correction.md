# Correction J2 partie 8 : défaire et modifier un commit

12.  Question (Q) : finalement, les films et séries s'avèrent ne pas être une bonne idée, vous préférez faire des activités dehors, vous décidez de défaire uniquement les changements effectués lors de l'ajout du fichier *netflix.md*
```bash
# Réponse (R) option 1 : si vous n'avez pas encore envoyé les modifications sur GitHub et pas vous n'avez pas encore effectué de merge sur main
git branch -D feature/netflix
# R option 2: même condition que précedemment sauf que vous voulez garder une trace de la branche sans conserver les modifications effectuées
git checkout feature/netflix
git reset --hard ID_COMMIT # Avec ID_COMMIT égale à l'identifiant du dernier commit avant l'introduction du ficher netflix.md
# R option 3 : changement envoyé sur la branche distante feature/netflix
git checkout feature/netflix
git revert ID_COMMIT # avec ID_COMMIT identifiant du premier commit ayant introduction le fichier netflix.md
# R option 4 : changement fusionné dans la branche main
git checkout main
git revert ID_COMMIT # avec ID_COMMIT identifiant du commit de merge de la branche feature/netflix dans main
```
13. Le message de commit crée lors de l'action précédente ne vous convient pas, vous décidez de le supprimer ou de le modifier avant d'envoyer vos dernières mises à jour en ligne.
```bash
# R : plusieurs façons de faire mais la plus adaptée ici modification du dernier commit donc
git commit --amend
```