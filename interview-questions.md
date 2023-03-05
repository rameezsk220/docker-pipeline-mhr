Git questions
------------
git config --global user.name “hanumantharao”

git config  --global user.email “********” 

git init reponame  ---it is used to intiailse the new repository

git clone  git@github.com:hanumantharao19/terrafrom-basics.git

git clone  https://github.com/hanumantharao19/terrafrom-basics.git

git branch --it is used to list the branches


git add . ---it is used to add the all files in the current directory to stage area

git status ---> it shows the tracked  and untracked files and staged files

git commit  -m "commit message" ---commit the files to local repository

git log  -- it is used list the commit history

git push origin master

git branch <branch name>  -- To create new branch

git checkout –b branchname   To create new branch from master and switch to new branch
  
git checkout  <branch name>  -- To switch into the other branch
  
git branch -d <branch name>  -- To delete the branch but not able to current branch where we are
  
git merge  <branch name>   --It is used to merge mentioned branch into current branch
  
git show <commit id>  --To know what files and changes added in this commit
  
git diff --This command shows the file differences which are not yet staged
  
git diff  <first branch>  <second branch>  --This command shows the differences between the two branches mentioned.
  
git rm  <filename> This command deletes the file from your working directory and stages the deletion

  git checkout filename  ---It is used to discard the changes in the file

git checkout *    ---> it is used to discard changes in all files

git reset *  ---> it is used to un stage the all files
  
git reset filename or git reset HEAD filename  ---> it is used to un stage the file from staging area
  
git reset HEAD~1  -it is to used to undo the  last commit in local repo
  
git reset HEAD~2  ---it is to  undo last three commits
  
git reset --soft HAED~1 --undo the recent commit but files available in staging area
  
git reset --hard HEAD~1 --undo the recent commit and files also not available in working area
  
git reset  <commitid>  -- This command undoes all the commits after the specified commit and preserves the changes locally.

git show  <commitid> --> it will display committed file and changed content
  
git stash  # it is used to save changes which are doing in the git tracked files
  
git stash list # to list the stashs
  
git stash apply # it is used to apply the latest changes to the repo
  
git stash pop  # it is used to apply the  latest changes  to the repo and remove the stash in the list
  
git stash drop # it issued to remove the stash and removed the  changes in working directory
  
git stash clear # it used to clear all stashs





