# Correction J2 partie III : partager votre travail dans un dossier d'extraction

5. Question : votre ami(e) vous demande de lui partager des fichiers d'extractions de votre travail pour qu'il puisse les s'inspirer de votre travail pour ses préparatifs.

```bash
# Réponse
git format-patch -o ./patches # partagez ensuite ce dossier via les options de la commande format-patch il est possible de l'envoyer directement par e-mail à votre destinatire cf. la commande git format-patch --help
```