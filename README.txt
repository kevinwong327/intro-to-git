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