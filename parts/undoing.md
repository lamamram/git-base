# ACTIONS NEGATIVES

* git checkout -- [path]: écraser un fichier du rep. de travail avec la version d'un commit
* git rm [--cached] [-r], git mv: supprimer / renommer dans le dépôt et dans le rep. de travail
* git reset -- [path | .]: désindexation

* git reset [--soft | --mixed | --hard] [HEAD~n | hash]
  | options       | index        | copie de travail
  |:---------------|:--------------:|-----------------:
  | --soft        | conservé     | conservée
  | --mixed [default] | écrasé   | conservée
  | --hard        | écrasé       | écrasée


* git revert [--no-edit] [HEAD~n | hash]
  - --no-edit: garder le message par défaut pour le nouveau commit