## BASIC COMMANDS
git                     => says I'm using git

git --version => tells me what version of git I'm using

git init            => tells git to start paying attention. makes your current folder into a repo.

git add [WHATEVER YOU'RE ADDING] => tells git what you want to track this version (usually use git add . to add everything)

git commit -m "[INSERT MESSAGE HERE]" => saves a version and adds the label [INSERT MESSAGE HERE]

## *~*~*~*VIM TRAP!*~*~*~*
If you forget your commit message or otherwise end up in VIM:

1) Type any messages you wanted to type (may have to type "i" to trigger INSERT)
2) Hit "esc" to get out of insert mode
3) Type :wq to get out of VIM
*~*~*~*~*

git log     => shows a list of commits
git diff    => shows changes since last commit
git status=> tells me what's what

git branch                          => tells me what branches exist and which one I'm on
git branch [BRANCH_NAME]=> creates a new branch BRANCH_NAME, but does not check it out
git branch -d [BRANCH_NAME] => deletes BRANCH_NAME

git checkout [BRANCH_NAME]=> switches me to BRANCH_NAME (branch already exists)
git checkout -b [BRANCH_NAME] => creates [BRANCH_NAME] and switches me to it

git merge [BRANCHNAME] => merges all changes made in [BRANCHNAME] to current branch

git remote add origin [URL_OF_REMOTE_REPO] => define a remote (usually online/cloud) location to store your code, e.g. GitHub, and call that remote 'origin'

git push origin [BRANCH_NAME] => upload all commits from your current branch to the relevant branch on the origin location
git push => can just use this command after you use the above command initally

git clone [URL_OF_REMOTE_REPO] => download a remote repo for the first time
git pull origin master => download all commits that have changed since the last time you downloaded (from origin repo, master branch)

## DELETING A LOCAL GIT REPO
rm -rf [REPO_NAME]

## COMMANDS YOU USE A LOT
git add .
git commit -m "INSERT MESSAGE HERE"
git push origin [BRANCHNAME]


. . . . . . . . . . . . . . . . . .
## BRANCHING & MERGING
Branching = concept of going down a different path in the code base from a specific commit.
Merging = concept of applying changes made in one branch to another.

Usually teams will merge when they reach a specific goal.

```
					Main Branch
						|
						1
					   	|
					   	2
			   	   	      /   \
					     1B -- |
					      |    |
					     2B -- **
```

. . . . . . . . . . . . . . . . . .
## TYPICAL GIT WORKFLOW
Prob only want to do a couple commits max before you merge so things don't get crazy.

```
			   * – – – – – – – – – – – - - – – *
		   	    \  				  /	
feature branch		    -\ _ _ commit _ _ commit _ _ /- 	merge changes
 created from		      1 			 2 	back into
  master							master
```

#testy-test
