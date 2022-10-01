# Git Cheat Sheet
Basic Git Commands Cheet Sheet

### 🖥️ Setting up your GIT information

From scratch -- Set your name associated with your user account         
```git config --global user.name "NAME"```
<br>
Set your email associated with your user account  
```git config --global user.email "youremail@abc.com"```

### 🛠 Create a Repository

Create a new local repository         
```git init [project name]```
<br>
Download from an existing repository  
```git clone my_url```
### 🔎 Observe your Repository
List new or modified files not yet committed        
```git status```
<br>
Show the changes to files not yet staged        
```git diff```
<br>
Show the changes to staged files        
```git diff --cached```
<br>
Show all staged and unstaged file changes        
```git diff HEAD```
<br>
Show the changes between two commit ids         
```git diff commit1 commit2```
<br>
List the change dates and authors for a file         
```git blame [file]```
<br>
Show the file changes for a commit id and/or file         
```git show [commit]: [file]```
<br>
Show full change history         
```git log```
<br>
Show change history for file/directory including diffs         
```git log -p [file/directory]```
<br>
### 🌴 Working with Branches
List all local branches         
```git branch```
<br>
List all branches, local and remote         
```git branch```
<br>
Switch to a branch, branch_name, and update working directory         
```git checkout branch_name```
<br>
Create a new branch called new branch                  
```git branch branch_name ```
<br>
Delete the branch called my_branch         
```git branch -d my_branch```
<br>
Merge branch _a into branch_b         
```git checkout branch_b```
```git merge branch_a```
<br>
Tag the current commit         
```git tag my_tag```
<br>
### 👛 Make a change
Stages the file, ready for commit         
```git add [file]```
<br>
Stage all changed files, ready for commit         
```git add .```
<br>
Commit all staged files to versioned history         
```git commit -m "commit message"```
<br>
Commit all your tracked files to versioned history         
```git commit -am "commit message```
<br>
Unstages file, keeping the file changes         
```git reset [file]```
<br>
Revert everything to the last commit         
```git reset --hard```
<br>
Overwrite commit history with your own local history (force push):
```git push --force```
<br>
### 🚰 Synchronize
Get the latest changes from origin (no merge)         
```git fetch```
<br>
Fetch the latest changes from origin and merge         
```git pull```
<br>
Fetch the latest changes from origin and rebase         
```git pull --rebase```
<br>
Push local changes to the origin         
```git push```
<br>
### 🗣Help
When in doubt, use git help         
```git command --help```
<br><br>
