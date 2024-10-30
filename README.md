# Git
NB : Prise de note git
======================================

Créer un nouveau repo par ligne de commande :

0) echo "description du projet" >> readme.md

1) se placer dans le repos local à mettre sur dépot distant
git init

2) ajouter fichier à envoyer sur la prochaine "sauvegarde"
git add fichier.fi

3) Commenter la prochaine "sauvegarde"
git commit -param "commentaire"

4) Sélection de la branche sur laquelle l'envoie sera fait
git branch -param nom_de_branche

5) ??
git remote add origin https://...

6) envoie de la "sauvegarde"
git push -u origin main

==========================================

Pousser un repo existant :

0) git remote add origin https://....

1) git branch -param nom_de_branche

2) git push -u origin main

==========================================

ou importer du code depuis un autre repo.
