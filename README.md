# cheat-sheet-GitHub

 ## workflow pour mettre à jour ma branch avec le code fait par un autre dev ou prof sur la branche master
1. commencer par commiter mon travail sur la branch dans laquelle je me trouve
2. migrer vers la branch master `git checkout master`
3. je vérifie si je suis bien sur master `git branch`
4. je pull les changements réalisé sur master (ici prof)  `git pull prof master --allow-unrelated-histories --no-edit -X theirs`
5. je vérifie alors que mon master local est à jour Si oui je migre dans une nouvelle branche
6. créer une branche et switcher dedans `git checkout -b jour3` ou idem `git switch -c day2`
7. /!\ commande dangereuse, car elle peut faire perdre des données comités sur master `git checkout master && git reset --hard prof/master`
8. ensuite je bosse dans ma nouvelle branch et pour commiter je dois d'abord préciser à GitHub que ma branch sera celle de push par défaut  `git push --set-upstream origin jour3`
9. ensuite comme d'hab => `git add .` `git commit -m""`  `git push`
---
## pull request workflow
0. fork / clone / pull => the last changes in local
1. create a branch  `git checkout -b feature_x`
2. commit and push changes 
3. open a pull request "it'a a proposal of changing"
4. discuss and review code
5. rebase directly on branch or do `git rebase master` to take all changes that were commited on master and replay them on the current branch.
 - this operation works by resetting the current branch to the same commit as master, and applying each commit of the current branch.
7. tests
8. Merge branch to the master. After changes have been verified by lead dev or anyone who is in charge, merge is possible 
 - `git checkout master`
 -  `git merge <branch> --no-ff` 
---

 #### How to check a repository's status in Git:
 This command will show the status of the current repository including staged, unstaged, and untracked files.
 - `git status`
 #### How to see your commit history in Git:
 This command shows the commit history for the current repository:
 - `git log`






