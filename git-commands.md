///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\


Change Folder in Git
# Go to your project root
cd /c/Learn-development/Monitor_Porjects_App

# Go to backend folder
cd backend

# Go back to project root
cd ..

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

Make a New Branch
git checkout -b branch-name

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

switch back to the main branch (branch changing)
by running this command: git checkout main

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

check all the branches that exist
in your repo by running the "git branch" command

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

Change Branch Name
"git branch -M main" changes your main branch's name to "main". The default branch might be created as "master", but "main" is the standard name for this repo now. There is usually no response here

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

Add Remote Link of Repo
"git remote add origin [https://github.com/ihechikara/git-and-github-tutorial.git]"(https://github.com/ihechikara/git-and-github-tutorial.git) creates a connection between your local repo and the remote repo on GitHub

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\
Committing your changes

git commit -m "your message"

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

GitHub repo already has
a README or files → you need to pull first, then merge
git pull origin main --allow-unrelated-histories
git push -u origin main

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

Push Branch/Changes
"git push -u origin main" pushes your repo from local device to GitHub.

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

Clone Repo  - When Downloading complete project
"git clone YOUR_HTTPS_URL" for pull git repo changes from GitHub

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

Pull Request - When Changes are Made
git pull origin main

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

Merge Changes
we can merge the changes we made in the test branch into the main branch by running
"git merge test".
At this point, you will see all the changes made in the test branch reflected on the main branch.
GO in your branch to merge changes into it.

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\

Delete the merged branch

Once your feature branch is successfully merged:

git branch -d feature/zoomToLayer       # delete local branch
git push origin --delete feature/zoomToLayer  # delete remote branch

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

Remove the nested .git directory
# Navigate to the Backend folder
cd Backend/

# Remove the .git directory (this removes Git tracking from Backend)
rm -rf .git

# Go back to the main directory
cd ..

# Now add and commit normally
git add .
git commit -m "Add Backend folder"

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

Task					Command
Quick view of connected repo		git remote -v
Detailed info				git remote show origin
Check branch tracking			git branch -vv
See all remotes				git remote

Goal				Command
Discard one file’s edits	git restore filename
Discard all unstaged edits	git restore .
Unstage files (keep changes)	git restore --staged .

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

Rename the file using Git
git mv old_filename.ext new_filename.ext

///////////////////// **************************** \\\\\\\\\\\\\\\\\\\\\\\\\\\\

Situation								Command
You’re joining a new project for the first time				git clone
You already cloned the repo and want updates				git pull
You want to bring in others’ recent commits before pushing yours	git pull
You’re setting up on a new PC						git clone

To List all Commits and Copy the Commit Hash:

git log --oneline