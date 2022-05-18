# cheat-sheet-GitHub

 ### Git flow pour mettre à jour ma branch avec le code fait par un autre dev ou prof sur la branche master
- commencer par commiter mon travail sur la branch dans laquelle je me trouve
- migrer vers la branch master `git checkout master`
- je vérifie si je suis bien sur master `git branch`
- je pull les changements réalisé sur master (ici prof)  `git pull prof master --allow-unrelated-histories --no-edit -X theirs`
- je vérifie alors que mon master local est à jour Si oui je migre dans une nouvelle branche
- créer une branche et switcher dedans `git checkout -b jour3` ou idem `git switch -c day2`
- - /!\ commande dangereuse, car elle peut faire perdre des données comités sur master `git checkout master && git reset --hard prof/master`
---
- ensuite je bosse dans ma nouvelle branch et pour commiter je dois d'abord préciser à GitHub que ma branch sera celle de push par défaut  `git push --set-upstream origin jour3`
- ensuite comme d'hab => `git add .` `git commit -m""`  `git push`

### le pull request workflow
- on fait une PR de notre branche vers `master` (ou `main`)
- nos collègues font le retour
- on fix les retours sur notre branche
- La PR **à continuer**






