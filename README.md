# FORMATION GIT

## installation d'une vm vagrant

1. install de vgrant && reboot
2. `vagrant box add [box_name]`
3. `vagrant up` dans le dossier du Vagrantfile
4. récupérer l'ip et faire le dns local

## essentiels de git

1. les trois zones:
  * la copie de travail: répertoire où l'on place le code
  * l'index (staging area): zone abstraitre de préparation au commit
  * le dépôt: le dossier .git dans la copie de travail

2. les 4 états d'un fichier dans git
  * Untracked / non suivi: nouveau fichier, inconnu du dépôt
  * Added / staged / ajouté: mis dans l'index
  * Unmodified: iso par rapport au dépôt (dernier commit contenant ce fichier)
  * Modified: modifié par rapport au dépôt
  * options
    - à supprimer : suite à git rm (bon pour commit)
    - à renommer : suite à git mv (bon pour commit)

3. création de commits et bases:
  * [voir ici](./parts/base_commands.md)

## Actions négatives
  * [voir ici](./parts/undoing.md)


## Dépôts distants

  1. synchronisation des dépôts
    * `ssh-keygen`: génération d'une paire pubkey/privkey
    * upload de la pubkey sur le serveur
    * config ssh de la privkey en local

    ```
    Host gitlab.myusine.fr
     IdentityFile "/c/Users/Admin stagiaire.DESKTOP-8967908/.ssh/gitlab"
     UserKnownHostsFile /dev/null
     StrictHostKeyChecking no
    ```
  2. commandes usuelles
    * `git remote [add | rename | remove] [repo_name] [addr]`: gestion des dépôts en local
    * `git push [-u] [repo_name] [branch_name]` : envoi de commits sur un dépôt distant
      - -u ou --set-upstream: déclaration de [repo_name]/[branch_name] comme dépôt / branche par défaut: permet de lancer git fetch, push, pull sans arguments

## SCRUM

![shcéma SCRUM](https://www.bocasay.com/wp-content/uploads/2022/02/Scrum-process-schema-FR-small.webp)

## BRANCHES

* `git branch [branch_name]`: création de branche sans bascule à partir de la branche / commit courant
* `git checkout [-b]  [--track] [branch_name]`: bascule sur la branche
  - -b: + création
  - --track: + création à partir de la branche de suivi (upstream)
* `git merge [--no-ff] [branch_name]`: fusionner [branch_name] dans la branche courante 
* `git revert -m 1 [merge_commmit]`: revert une branche entière

## Merge REQUEST GITLAB (gitlab flow)

1. créer une issue
2. créer une merge request (MR) à partir de l'issue
3. capter la branche de feature créée en local
   - `git checkout --track origin/....`
4. coder la branche de feature
5. pousser sur la branche distante
6. CI/CD
7. Revue de code collégiale
8. merge avec possibilité de squasher (comprimer) les commits de la branche en 1 seul   
## TAG

* `git tag -a [tag_name] [hash | HEAD] -m ["msg"]`: création
  - -d: suppression
* git push [--delete] [repo_name] [tag_name]: pousser et pousser suppression
* git tag ... --force: déplacer le tag sur un nouveau commit
