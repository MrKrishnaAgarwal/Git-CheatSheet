# Git Cheat Sheet
A quick reference guide to the most commonly used Git commands

Here is a list of the most common git commands.  I've included the most common options for each command, but you can always run `git help <command>` to get more information.
This repository also lists some great resources and books for learning git.

### 🖥️ Setting up your Git information

From scratch -- Set the name associated with your user account.
```git config --global user.name "NAME"```
<br>
Set the email associated with your user account.
```git config --global user.email "youremail@abc.com"```
<br>
Set your default editor:
```git config --global core.editor "vim"```
<br>
Set your default merge tool:
```git config --global merge.tool "vimdiff"```
<br>
Set your default push behaviour:
```git config --global push.default "simple"```
<br>
Set your default pull behaviour:
```git config --global pull.rebase "true"```
<br>
Set your default branch name:
```git config --global init.defaultBranch "main"```
<br>
Set your default credential helper:
```git config --global credential.helper "cache --timeout=3600"```
<br>

### 🛠 Create a Repository

Create a new local repository:
```git init [project name]```
<br>
Download from an existing repository:
```git clone my_url```
### 🔎 Observe your Repository
To list new or modified files not yet committed:
```git status```
<br>
To show the changes to files not yet staged:
```git diff```
<br>
To show the changes to staged files:
```git diff --cached```
<br>
To show all staged and unstaged file changes:
```git diff HEAD```
<br>
To show the changes between two commit ids:
```git diff commit1 commit2```
<br>
To list the change dates and authors for a file:
```git blame [file]```
<br>
To show the file changes for a commit id and/or file:
```git show [commit]: [file]```
<br>
To show full change history:
```git log```
<br>
To show the change history for file/directory including diffs:
```git log -p [file/directory]```
<br>
To show the change history for a specific author:
```git log --author="[author name]"```
<br>

### 🌴 Working with Branches
To list all local branches:
```git branch```
<br>
To list remote and local branches:
```git branch -a```
<br>
To switch to an existing branch, branch_name, and update the working directory:
```git checkout branch_name```
<br>
To switch to the last used branch:
```git checkout - ```
<br>
To create a new branch called the new branch:
```git branch branch_name ```
<br>
To create a local branch and switch to it:
```git checkout -b branch_name```
<br>
To delete the branch called my_branch:
```git branch -d my_branch```
<br>
To push a branch to remote:
```git push origin branch_name```
<br>
To rename a current branch:
```git branch -m new_name```
<br>
To merge branch _a into branch_b:
```git checkout branch_b```
```git merge branch_a```
<br>
To abort the current merge:
```git merge --abort```
<br>
To tag the current commit:
```git tag my_tag```
<br>
To discard all local commits and changes:
```git reset --hard origin/<remote_branch_name>```
<br>

### 👛 Make a change
To stage the file, ready for commit:
```git add [file]```
<br>
To stage all changed files, ready for commit:
```git add .```
<br>
To commit all staged files to the versioned history:
```git commit -m "commit message"```
<br>
To commit all your tracked files to the versioned history:
```git commit -am "commit message```
<br>
To set the executable flag to a file foo.sh:
```git update-index --chmod=+x foo.sh```
<br>
To unstaged the file, keeping the file changes:
```git reset [file]```
<br>
To revert everything to the last commit:
```git reset --hard```
<br>
To overwrite commit history with your local history (force push):
```git push --force```
<br>
To reset remote branch to specific commit (danger: use only if not distributed to other people before):
```git reset --hard <commit-hash> && git push -f origin <branch-name>```
<br>

### 🚰 Synchronize
To get the latest changes from the origin (no merge):
```git fetch```
<br>
To fetch the latest changes from the origin and merge:
```git pull```
<br>
To fetch the latest changes from the origin and rebase:
```git pull --rebase```
<br>
To push local changes to the origin:
```git push```
<br>
### 🧾 Logs and History
To show commit history in single lines:
```git log --oneline```
<br>
To show the commit history for the last N commits:
```git log -2```
<br>
To show commit history for the last N commits with diff:
```git log -p -2```
<br>
To show reflog history for emergency actions:
```git reflog```
<br>
To show all local file changes in the working tree:
```git diff```
<br>
To show changes made to a file:
```git diff myfile```
<br>
To show who changed what & when in a file:
```git blame myfile```
<br>
To show remote branches and their mapping to local:
```git remote show origin```
<br>
### 🧹 Cleanup
To delete all untracked files:
```git clean -f```
<br>
To delete all untracked files and directories:
```git clean -df```
<br>
To undo local modifications to all files:
```git checkout -- ```
<br>
To unstaged a file:
```git reset HEAD myfile```
<br>
To undo local modifications to a file and stage it:
```git checkout -- myfile```
```git add myfile```
<br>
To find the commit that introduced a bug:
```git bisect start```
```git bisect bad```
```git bisect good <commit>```
<br>

### 📦 Submodules

To add a submodule:
```git submodule add <url>```
<br>
To update a submodule:
```git submodule update --remote```
<br>
To remove a submodule:
```git submodule deinit -f -- submodule_name```
```git rm -f submodule_name```
```git rm -f .gitmodules```
<br>
### 📦 Subtrees

To add a subtree:
```git subtree add --prefix=folder_name <url>```
<br>
To update a subtree:
```git subtree pull --prefix=folder_name <url>```
<br>
To remove a subtree:
```git subtree split --prefix=folder_name```
```git rm -rf folder_name```
```git commit -m "Remove folder_name"```
<br>

### 🗣Help

```git help -a``` and ```git help -g``` list available subcommands and some
concept guides. See ```git help <command>``` or ```git help <concept>```
to read about a specific subcommand or concept.
See ```git help git``` for an overview of the system.
<br>

## Git Resources
You should check some of these Git resources as they would be amazing for your journey.
You will master Git with these resources:

#### ⭐ [Oh My Git](https://ohmygit.org/)
This is an open-source card game that is dedicated to teaching important git commands. There's even an integrated terminal for you to test any git command you wish. Their graphics are nothing fancy but it helps with learning visually.

#### ⭐ [The Odin Project](https://www.theodinproject.com/lessons/foundations-git-basics)
This site provides free full-stack courses that are maintained by the open-source community. They have two git courses that are well worth your attention.

#### ⭐ [Learn Git Branching](https://learngitbranching.js.org/)
Branching is an important topic in Git. There's no better way to learn it than this interactive game. Run commands with their built-in terminal and let their graphics explain the rest.

#### ⭐ [Git Tutorial by Atlasian](https://www.atlassian.com/git/tutorials)
Become a git guru with the help of Atlassian tutorials. Atlassian has done a fantastic job with their explanations and visuals to understand git. This is one of the top resources for learning Git.

#### ⭐ [Git Immersion](https://gitimmersion.com/)
Learn all the fundamentals of Git with this guided tour. This resource explains every important Git command while you execute them on your local machine.

#### ⭐ [Visual Git Reference](https://marklodato.github.io/visual-git-guide/index-en.html)
I'm a big believer that visual aids help you better understand and remember information. Which is why this resource is a must-see. Their diagrams and explanations are top-tier.

#### ⭐ [GitHub Minesweeper](https://profy.dev/project/github-minesweeper)
Get a dose of nostalgia with this one! Learn on-the-job Git workflow while playing minesweeper with another player. So much fun you'll forget you're even learning.

## Are you more of an extensive reader, we got you!

Here is GitHub's own GIT Cheatsheet for you 📗
- [GitHub's GIT Cheatsheet](https://github.com/MrKrishnaAgarwal/Git-CheatSheet/blob/main/git-cheat-sheet-education.pdf)

For more in-depth reading - you should check Git Notes for Professionals 📕
- [Git Notes for Professionals by GoalKicker](https://goalkicker.com/GitBook/GitNotesForProfessionals.pdf)

## Want to learn Git more interactively?

Here are some of the best Git courses on Udemy 🎓

- [Git & GitHub - The Complete Git & GitHub Course](https://www.udemy.com/course/git-github-the-complete-git-github-course/): This course is a complete guide to Git and GitHub. It will teach you everything you need to know to start using Git and GitHub in your projects.

- [The Git & GitHub Bootcamp](https://www.udemy.com/course/git-and-github-bootcamp/): This course is a great way to learn Git and GitHub from scratch. It covers all the basics of Git and GitHub and also teaches you how to use Git and GitHub in your daily workflow.

- [Become an Expert in Git & GitHub in 4 Hours](https://www.udemy.com/course/git-expert-4-hours/): Become an Expert in Git & GitHub by writing commands, learning theory, and taking quizzes. Learn Git today in 4 hours!

<br>

### Contributing

Contributions are always welcome! Please read the [contribution guidelines](/CONTRIBUTING.md) first and then feel free to open a pull request.

### License

This project is licensed under the MIT License - see the [LICENSE](/LICENSE) file for details.

### Contributors

<b> ✨ Thanks goes to these wonderful people ✨ </b>

<table>
  <tbody>
    <tr>
      <td align="center"><a href="https://github.com/MrKrishnaAgarwal"><img src="https://avatars.githubusercontent.com/u/100597998?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Krishna Agarwal</b></sub></a><br /><a href="#maintenance-MrKrishnaAgarwal" title="Maintenance">🚧</a> <a href="https://github.com/MrKrishnaAgarwal/git-cheatsheet/commits?author=MrKrishnaAgarwal" title="Code">💻</a> </td>
      <td align="center"><a href="https://github.com/arefathi"><img src="https://github.com/arefathi.png" width="100px;" alt=""/><br /><sub><b>Arefat H</b></sub></a><br /><a href="https://github.com/MrKrishnaAgarwal/git-cheatsheet/commits?author=arefathi" title="Code">💻</a></td>
      <td align="center"><a href="https://github.com/Huluvu424242"><img src="https://github.com/Huluvu424242.png" width="100px;" alt=""/><br /><sub><b>Thomas Schubert</b></sub></a><br /><a href="https://github.com/MrKrishnaAgarwal/git-cheatsheet/commits?author=Huluvu424242" title="Code">💻</a></td>
      <td align="center"><a href="https://github.com/swatiaggrawal"><img src="https://github.com/swatiaggrawal.png" width="100px;" alt=""/><br /><sub><b>Swati Aggrawal</b></sub></a><br /><a href="https://github.com/MrKrishnaAgarwal/git-cheatsheet/commits?author=swatiaggrawal" title="Code">💻</a></td>
      <td align="center"><a href="https://github.com/LoftyDroid"><img src="https://github.com/LoftyDroid.png" width="100px;" alt=""/><br /><sub><b>Swati Aggrawal</b></sub></a><br /><a href="https://github.com/MrKrishnaAgarwal/git-cheatsheet/commits?author=LoftyDroid" title="Code">💻</a></td>
    </tr>
  </tbody>
</table>
<br>

#### If this project helped you in any way, please consider giving it a ⭐️. It will help us reach more people and help them learn Git & GitHub.


[![Open Source Love](https://firstcontributions.github.io/open-source-badges/badges/open-source-v1/open-source.svg)](https://github.com/MrKrishnaAgarwal/git-cheatsheet)
<a href="https://github.com/MrKrishnaAgarwal/git-cheatsheet/pulls" ><img src="https://img.shields.io/badge/Contributions-welcome-green.svg?style=flat&logo=github" alt="Contributions" /></a>
