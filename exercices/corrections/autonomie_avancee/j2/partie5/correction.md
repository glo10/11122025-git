# Correction J2 partie V : tags

7. Question : vous décidez de versionner votre projet en y ajout des tags

```bash
# Réponse
## Ici remplacez ID_COMMIT par l'identifiant d'un commit de votre dépôt local
## et appliquez les versions selon leur pertinence et la nature des modifications apportées (version majeure, mineure ou patch)
##  majeure => rupture, incompatibilité avec les versions précédentes
##  mineure => nouvelles fonctionnalités sans rupture
##  patch => correction
git tag v1.0.0 ID_COMMIT # majeure
git tag v1.1.0 ID_COMMIT # mineure
git tag v1.1.1 ID_COMMIT # patch
git tag v1.2.0 ID_COMMIT # mineure
git tag v2.0.0 ID_COMMIT # majeure
```