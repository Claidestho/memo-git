# Préparer l'environnement :

- Enregistrer le nom d'utilisateur et le mail utilisé sur github :
    - <code>git config --global user.name "user_name"</code>
    - <code> git config --global user.email "email_id"</code>

# Liste des commandes Git
- **git init** : Cette commande permet d'initialiser un nouveau repository. Sans arguments, cela permet de créer un dépot vide sur sa machine.

- **git add** : Cette commande est utilisée pour ajouter les fichiers qui seront inclus dans le dépot, et qui seront transmis lors des futus commits / push.

- **git commit** : Cette commande permet de modifier le dépot local avec les ficheirs choisis via git add

- **git push** : Push permet d'envoyer vers le dépot distant les modifications apportées par le dernier commit. 

- **git diff** : Cette commande permet d'afficher les différences entre les versions locales des fichiers et les versions sur le serveur distant indiqué via git add.

- **git status** :
Ordre apparent des commande : Affiche l'état du projet, la branche sur laquelle on travaille ainsi que tous les changements effectués.

- **git log** : Permet d'afficher le journal de toutes les opérations précédentes effectuées.

- **git checkout** : Permet de revenir à une version précédente, en précisant le commit à annuler. Permet également de naviguer entre les différentes branches du projet.

ex : <code>git checkout acffcf1 instructions/etapes.md</code> -> Le fichier **etapes.md** est modifié tel qu'il était avant le commit **acffcf1**

- **git revert** : Cette commande permet d'inverser les changements apportées par un commit (création > suppresion, inversion déplacement, etc...)

- **git tag** : Permet d'étiquetter un commit pour montrer son importance (exemple v1.0 pour la premiere version utilisable d'un programme).

- **git pull** : Importe dans le repo local les élements du repo distant 

- **git merge** : Permet de fusionner la branche ciblée avec la branche principale

-**git branch** : Permet d'afficher les différentes branches et de monter la branche active.

**git init** -> **git add** -> **git commit** -> **git diff** -> **git push**

Pour éviter de remettre toujours login/mdp -> enregistrement de la clé SSH publique.

Réponse à la quête : **On n'apprend bien qu'a force de se tromper**

# Conflits / Résolution