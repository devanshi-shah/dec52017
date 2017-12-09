Git commands:

Basic commands:
-----------------------------------------------------
clear -> Clear the cmd screen
~ -> Shows the User directory
ls -> show the list of directory under the current folder it is pointing to
ls-l -> List view of the data along with the permissions
pwd -> Path of the current directory
mkdir -> To create a new directory/folder
cd -> to go inside the directory
vi -> to open a file
:wq and Shift + ZZ  -> to save the file
:q!/q -> to quit/Exit
cd /c/ -> to go into a drive (Here c drive for example)

Clone the project
-----------------------------------------------------
Go into the appropriate directory where you want to clone the project under some folder and then follow the below steps:
1. git clone (Paste the URL from your created fork) 
2. git remote -v (To check where the URL is pointing currently)
3. git remote add upstream (Paste the main URL from the upstream repository) 
**It is important that you clone only ONCE!**

To create a new branch 
-----------------------------------------------------
git checkout -b (give the new name for an branch) **Create a parent branch**
git checkout -b (name of the branch) (branch name from which you want to create a new branch)**Create a child branch**

To go to a branch 
-----------------------------------------------------
git checkout (branch name)


To get all local branches
-----------------------------------------------------
git branch


To get all branches
-----------------------------------------------------
git branch -a


To delete a branch
-----------------------------------------------------
git branch -D (branch name) [This will delete the branch from the local]
git push origin -d (branch name) [This will delete from the branch from the fork]

Push the new branch to the upstream/origin
-----------------------------------------------------
git push origin (branch name)
git push upstream (branch name) **Never use git PUSH upstream**


Steps to commit the changes made to file:
-----------------------------------------------------
1. Go to that specific branch
    git checkout branch_name
2. Make changes to the file manually and Save
3. git add .
4. git commit -m "comments"
5. git push origin (branch_name)

If anything was merged before we make changes to new file then follow below steps(When working on new feature)
------------------------------------------------------------------------------------------------------
1. git checkout (branch_name)
2. git fetch --all
3. git pull upstream (branch_name) 
**Whenever we perform git pull upstream we should always reset our branch with upstream**
4. git reset --hard upstream/(branch_name) **Note: Never use when a PULL REQUEST is open**
5. git push origin (branch_name) -f
**-f is used to forcibly push the current changes to the origin**
Then you can make new changes to the code and follow "Steps to commit the changes made to file"

If you want to add the changes to the same commit:
-----------------------------------------------------
1. git checkout (branch_name)
2. Make changes to the file and Save
3. git log (check whether the last commit was yours or not)
4. git commit --amend
5. Save the file by saving with the same commit name by using :wq
6. git push origin (branch_name) -f
7. Create a PR

When and how should we use Rebase(when we have the conflict)
-----------------------------------------------------------------
1. git fetch --all
2. git pull upstream (branch_name) -- rebase
3. Make changes to the file
4. git add .
5. git rebase --continue
6. git log
7. git push origin (branch_name) -f

How to discard the rebase 
-----------------------------------------------------
git rebase --abort and start over again.


How to remove the recent commit from the git log
-----------------------------------------------------
1. git log
2. git reset HEAD~1 (1 to remove the recent commit)







