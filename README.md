# Git Cheat Sheet
Basic Git Commands Cheet Sheet

### 🛠 Create a Repository

From scratch -- Create a new local repository         
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
List remote and local branches         
```git branch -a```
<br>
Switch to an existing branch, branch_name, and update working directory         
```git checkout branch_name```
<br>
Create a new branch called new branch                  
```git branch branch_name ```
<br>
Create a local branch and switch to it
```git checkout -b branch_name```
<br>
Delete the branch called my_branch         
```git branch -d my_branch```
<br>
Push branch to remote
```git push origin branch_name```
<br>
Rename current branch
```git branch -m new_name```
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
### 🧾 Logs and History
Show commit history in single lines
```git log --oneline```	
<br>
Show commit history for last N commits
```git log -2```	
<br>
Show commit history for last N commits with diff
```git log -p -2```	
<br>
Show all local file changes in the working tree
```git diff```	
<br>
Show changes made to a file
```git diff myfile```	
<br>
Show who changed what & when in a file
```git blame myfile```	
<br>
Show remote branches and their mapping to local
```git remote show origin```
<br>
### 🧹 Cleanup
Delete all untracked files    
```git clean -f```
<br>	
Delete all untracked files and directories    
```git clean -df```
<br>
Undo local modifications to all files   
```git checkout -- ```
<br>
Unstage a file    
```git reset HEAD myfile```
<br>
### 🗣Help
When in doubt, use git help         
```git command --help```
<br><br>

# Git Resources
You should definetly check some of these Git resources as they would be amazing to your journey.
You will master Git with these resources:

### ⭐ [Oh My Git](https://ohmygit.org/)
This is an open source card game that is dedicated to teaching important git commands. There's even an integrated terminal for you to test any git command you wish. Their graphics is nothing fancy but it helps with learning visually.

### ⭐ [The Odin Project](https://www.theodinproject.com/lessons/foundations-git-basics)
This site provides free full stack courses that are maintained by the open source community. They have two git courses that are well worth your attention.

### ⭐ [Learn Git Branching](https://learngitbranching.js.org/)
Branching is an important topic in Git. There's no better way to learn it than this interactive game.Run commands with their built-in terminal and let their graphics explain the rest.

### ⭐ [Git Tutorial by Atlasian](https://www.atlassian.com/git/tutorials)
Become a git guru with the help of Atlassian’s tutorials. Atlassian has done a fantastic job with their explanations and visuals to understand git. This is one of the top resources for learning Git.

### ⭐ [Git Immersion](https://gitimmersion.com/)
Learn all the fundamentals of Git with this guided tour. This resource explains every important Git command while you execute them in your local machine.

### ⭐ [Visual Git Reference](https://marklodato.github.io/visual-git-guide/index-en.html)
I'm a big believer that visual aids helps you better understand and remember information. Which is why this resource is a must-see. Their diagrams and explanations are top-tier.

### ⭐ [GitHub Minesweeper](https://profy.dev/project/github-minesweeper)
Get a dose of nostalgia with this one! Learn on-the-job Git workflow while playing minesweeper with another player. So much fun you'll forget you're even learning.

## Are you more of an extensive reader, we got you!

Here is GitHub's own GIT Cheatsheet for you 📗
- [GitHub's GIT Cheatsheet](https://github.com/MrKrishnaAgarwal/Git-CheatSheet/blob/main/git-cheat-sheet-education.pdf)

For more in-depth reading - you should check Git Notes for Professionals 📕
- [Git Notes for Professional by GoalKicker](https://goalkicker.com/GitBook/GitNotesForProfessionals.pdf)

<br>
