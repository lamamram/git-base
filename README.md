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