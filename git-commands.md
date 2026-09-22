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


I'll help you resolve this PAT (Personal Access Token) issue. Let me search for the official GitHub documentation on this.This is the correct behavior—GitHub now requires a **Personal Access Token (PAT)** instead of your account password for Git operations over HTTPS. Here's how to set it up:

## Create a Personal Access Token

1. Go to your GitHub settings: Click your profile picture → **Settings**
2. In the left sidebar, click **Developer settings** (or code icon)
3. Click **Personal access tokens** → **Tokens (classic)**
4. Click **Generate new token** → **Generate new token (classic)**
5. Give it a descriptive name (e.g., "VS Code" or "Terminal Access")
6. Select an expiration date (or leave it default)
7. Select the **repo** scope (this allows access to repositories)
8. Click **Generate token** and **copy it immediately** (you won't see it again!)

## Use the Token in Terminal/VS Code

When Git prompts you for credentials:

```bash
$ git clone https://github.com/USERNAME/REPO.git
Username: your-github-username
Password: your-personal-access-token  # Paste the token here
```

## Skip Repeated Prompts (Recommended)

Instead of entering credentials every time, **cache your credentials** so Git remembers them:

```bash
git config --global credential.helper cache
# (On macOS, use: git credential-osxkeychain)
# (On Windows, use: wincred)
```

Or use [Git Credential Manager](https://github.com/GitCredentialManager/git-credential-manager), which handles this automatically.

---

**For your friend:** They'll need to create their own PAT using the same steps above. Each person should use their own account and token—never share PATs!

Would you like help configuring this for a specific tool (VS Code, terminal, etc.)?

## Change the last commit message (most common)

If you just made a commit and want to edit its message:

```git commit --amend -m "New commit message"```

This rewrites the last commit with the new message.