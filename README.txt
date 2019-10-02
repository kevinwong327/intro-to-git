git reset --hard 10538 to go to specific commit
"git commit -m "Add all html file"" to add file to repository
"git reset HEAD file2.txt" to remove files from stage area
git commit -m "Add all html file"
touch .gitignore , then add file to be ignored by git
git branch to check which branch we are on
git checkout -b feature1 to switch to new branch feature1
Merge branch: 
git merge master OR
git checkout master, then git merge feature1


git remote add origin git@github.com:nax3t/intro-to-git.git



------------
git branches
- Listing all branches
- Adding a branch
- Changing branches
- Merging a branch
- Removing a branch
git branch -d feature1

         /-----0--0
        /        /
0------0----0---/

==================================================
Connect local git to github:
git remote add origin https://github.com/kevinwong327/intro-to-git.git

Check origin setup:
git remote -v

upload to github:
git push -u origin master

Download from Git Hub Repository:
git clone https://github.com/nax3t/webdevbootcamp.git

To change a latest git commit comment:
git commit --amend<enter> then edit the commit message and save the commit
git commit --amend -m "..." will change latest description to ...

Amending the message of the most recently pushed commit
git push --force example-branch

Amending the message of older or multiple commit messages
use interactive rebase , then force push to change the commit history
- on the command line, navigate to the repository that contains the commit you want to amend.
- "git rebase -i HEAD~n" to display a list of the last "n" commits in your default text editor
---------------------------------------------------------------------------------------------
pick e499d89 Delete CNAME
pick 0c39034 Better README
pick f7fde4a Change the commit message but push the same commit.
# Rebase 9fdb3bd..f7fde4a onto 9fdb3bd
#
# Commands:
#  p, pick = use commit
#  r, reword = use commit, but edit the commit message
#  e, edit = use commit, but stop for amending
#  s, squash = use commit, but meld into previous commit
#  f, fixup = like "squash", but discard this commit's log message
#  x, exec = run command (the rest of the line) using shell
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.
#
# Note that empty commits are commented out
---------------------------------------------------------------------------------------------

- replace "pick" with "reword" before each commit message you want to change

--------------------------------------------------------------------------------------------
pick e499d89 Delete CNAME
reword 0c39034 Better README
reword f7fde4a Change the commit message but push the same commit.
--------------------------------------------------------------------------------------------

- save and close the commit list file

- In each resulting commit file, type the new commit message, save the file, and close it.
- Force-push the amended commits. "git push --force"

# Save from origin to a new repo:
Create a new repo at github.
Clone the repo from fedorahosted to your local machine.
git remote rename origin upstream
git remote add origin URL_TO_GITHUB_REPO
git push origin master
