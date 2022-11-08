# COMMANDES DE BASE


* `git init`: création d'un dépôt vide dans le repertoire de travail
* `git config [--local | --global] section.param [value]`: configurer le dépôt
* `git add [-i] [path | .]` : ajout à l'index
* `git commit [-m "MSG"] [-a] [--amend]`
   - -a : ajoute auto tous les fichiers à l'état Modified
   - --amend: met à jour le commit courant (HEAD) avec un nouveau contenu / message
* `git log [-p] [-num] [--all] [--oneline]` affiche l'historique
    - -p: montre le diff avec le commit précédent
	- -num : montre les num derniers commits
	- --all: montre toutes les branches
	- --oneline: montre sur une ligne
