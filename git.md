#ALIAS#
------------------------------
logs ==> l
commit ==> c
auto commit ==> cc
checkout ==> ch
status ==> s
branch ==> b
merge ==> m
fetch ==> f		
tag ==> t
------------------------------

#GENERAL#
------------------------------
git status
git branch -m new_name						// rename branch
git branch -a || git remote || git tag		// list
git log --oneline --graph				
------------------------------

#REMOTE#
------------------------------										
git remote add origin $url$ 
git remote remove origin
git fetch
git checkout -b <new_branch> <remote>/<branch>						// create branch, branch = remote, checkout
git merge --allow-unrelated-histories <remote>/<branch> 			// merge without relation
git branch --set-upstream-to=<remote>/<branch> <localBranchName>		// set upstream
git push -u origin <localBranchName> 									// push to the branch with the same name on remote (creates if necessary) + set upstream
git push origin HEAD:<localBranchName> 								// push to remote
git push origin --delete <localBranchName>							// delete branch remotely
------------------------------

#LOCAL#
------------------------------
git checkout <pointer*>								// HEAD = pointer
git checkout -b <branch> <pointer*>					// create branch, branch = pointer, checkout
git merge --allow-unrelated-histories <branch>		// merge without relation
git branch -d <localBranchName>						// delete branch localy
git reset HEAD~1									// changes unstagged
git reset HEAD~1 --hard 							// changes deleted
git reset HEAD path/to/file 						// unstage in file
git reset HEAD . 									// unstage everything
git restore path/to/file							// delete unstage in file
git restore .										// delete all unstage
git clean <option>									// delete untracked
git rebase
git tag <pointer*>
git tag -d <tag>
------------------------------ 