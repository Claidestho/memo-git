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

- **git checkout** : Permet de revenir à une version précédente, en précisant le commit à sélectionner. Permet également de naviguer entre les différentes branches du projet.

    - ex : <code>git checkout acffcf1 instructions/etapes.md</code> -> Le fichier **etapes.md** est modifié tel qu'il était avant le commit **acffcf1**
- **git revert** : Cette commande permet d'inverser les changements apportées par un commit (création > suppresion, inversion déplacement, etc...)

- **git tag** : Permet d'étiquetter un commit pour montrer son importance (exemple v1.0 pour la premiere version utilisable d'un programme).

- **git pull** : Importe dans le repo local les élements du repo distant 

- **git merge** : Permet de fusionner la branche ciblée avec la branche principale

- **git branch** : Permet d'afficher les différentes branches et de monter la branche active.

- **git clone** : Télécharger en local le repo spécifié 

        git init / git clone -> git add-> git commit -> git diff -> git push

## Eviter de push un fichier



## Clé SSH
Pour éviter de remettre toujours login/mdp -> enregistrement de la clé SSH publique.


## Réponse à l'exo bonus 
Réponse à la quête : **On n'apprend bien qu'a force de se tromper**

# Conflits / Résolution

En cas d'un conflit qui ne peut pas être gérer par Github via un auto merge, il faut arriver à sortir du statut de merge :

- En abandonnant le commit causant le conflit en revenant au dernier commit actuel.

- Soit en modifiant les différents fichiers générant des conflits en vérifiant quelles sont ceux modifiés par le push causant le conflit grâce aux marqueurs de fusion ajoutés au code source. Grâce à VS code on peut facilement choisir quoi faire pour chaque changement (garder le changement, annuler le changement, etc...)

# Pull requests 

Les pulls request sont crées afin de demander la fusion d'une branche à la branche principale. Cela permet de vérifier les changements apportées par cette fusion avant de la mettre en place. Une pull request peut être demandée par un contributeur mais devra toujours être validée par un maintener.

# HEAD détaché

Le HEAD est en réalité un pointeur qui indique où l'on se trouve au niveau de l'évolution du repo -> sur une branche, un ancien commit, etc....

Il est tout à fait possible de retourner voir d'anciennes version de notre repo, cependant si un commit est fait depuis une version précédente c'est à ce moment la que le HEAD va se détaché de la branche active. Ce commit se hors du flow de git et ne sera donc que temporaire.

Afin de remédier à cela, il est possible de transformer ce commit en branche et de la merge avec la branche principale.
