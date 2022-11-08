# ACTIONS NEGATIVES

* git checkout -- [path]: écraser un fichier du rep. de travail avec la version d'un commit
* git rm [--cached] [-r], git mv: supprimer / renommer dans le dépôt et dans le rep. de travail
* git reset -- [path | .]: désindexation
* git revert [--no-edit] [HEAD~n | hash]
  - --no-edit: garder le message par défaut pour le nouveau commit
* git reset [--soft | --mixed | --hard] [hash | HEAD~n]
  1. déplacement de HEAD vers [hash | HEAD~n]
  2. suppression des commits suivant le nouveau HEAD
  3. écrasement ou conservation de l'index et ou de la copie de travail avec les options