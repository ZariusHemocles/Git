# Git
NB : Prise de note git
======================================

Créer un nouveau repo par ligne de commande :

0) echo "description du projet" >> readme.md

1) se placer dans le repos local à mettre sur dépot distant ; git init

2) ajouter fichier à envoyer sur la prochaine "sauvegarde" ; git add fichier.fi

3) Commenter la prochaine "sauvegarde" ; git commit -param "commentaire"

4) Sélection de la branche sur laquelle l'envoie sera fait ; git branch -param nom_de_branche

5) ?? ; git remote add origin https://...

6) envoie de la "sauvegarde" ; git push -u origin main

==========================================

Pousser un repo existant :

0) git remote add origin https://....

1) git branch -param nom_de_branche

2) git push -u origin main

==========================================

ou importer du code depuis un autre repo.


git = gestionnaire de version
github = service en ligne

git enregistre les versions du document en créant un /repo
(local ou distant(privé ou public)).
le repo local permet de garder son travail pres de nous, le distant est hébergé sur le réseau 
et permet d'avoir plusieurs repo, un historique délocalisé et aussi des droits différents.

les enregistrements de versions permettent de revenir à des versions précédentes
pour etudier les codes d'un point de vue logique et administratif
et tenter de minimiser les marges d'erreur.

à chaque actions sensible, les identifiants seront demandés si la connexion se fait en 
https, mais les identifiants ne seront pas demandés en SSH.

)) avant toute chose, activer le protocole ssh pour la connexion avec ; eval "$(ssh-agent -s)"

a) ssh-keygen -t ed25519 -C "your_email@example.com"

- générer la clé en se plaçant dans le dossier /.ssh/

b) copier le contenu dela clé.pub pour enregistrer sur le serveur github

- cat /.ssh/clépublique.pub

c) commencer à relier le repo local au distant.

- ssh-add /.ssh/cléprivé pour ajouter la clé à l'agent qui fait la requete

- git remote add origin git@github.com:user/Project.git
    # ajouter l'url du depot git distant
- git branch -M main
    # placer le prochain push sur la branche main
- git push -u origin main
    # pousser les éléments sur repo distant


Le local est composé de 3 phase de travail

1. le working directory : dossier de travail direct sur l'ordinateur.
2. le stage : représente les fihciers modifié qui devra apparaitre dans la prochaine version. (git add)
3. le repo : stockage des fichiers (git commit -m "message" (-m = indiquation d'un message))

pour verifier, faire 'git status'
si le document est en rouge, il est modifié mais pas indexé
si il est vert, le document à été git add et est maintenant en stage (indexé)

conseil ==================

1. Toujours commencer par créer un dépot distant lors d'un nouveau projet.
2. Toujours commencer par un dépot local avant tout (l'intéret est de mettre en dépot distant
    la version sûr et utilisable, alors que la version local est un clone de la version distante,
    et plus un enregistrement personnel pour les modification de code).
3. toujours laisser un message claire sur les modifications d'un fichier dans un commit.

--------------------------------------------------------------------------------------

git remote rename nomorigine neworigine = renommer un nom de lien

git remote set-url origin git@github.com:user/file = modifier un lien attribué à un nom

