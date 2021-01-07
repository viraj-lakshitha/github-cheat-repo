# Git and GitHub
Git is a distributed version-control system for tracking changes in any set of files, originally designed for coordinating work among programmers cooperating on source code during software development.

## Difference between Git and GitHub
#### What is Git ?
First developed back in 2005, Git is an extremely popular version control system that is at the heart of a wide variety of high-profile projects. Git is installed and maintained on your local system (rather than in the cloud) and gives you a self-contained record of your ongoing programming versions. It can be used completely exclusive of any cloud-hosting service, you don’t even need internet access, except to download it.

#### What is GitHub ?
GitHub is designed as a Git repository hosting service. It’s an online database that allows you to keep track of and share your Git version control projects outside of your local computer/server. Unlike Git, GitHub is exclusively cloud-based. Also unlike Git, GitHub is a for-profit service (although basic repository-hosting features are available at no cost to those who are willing to create a user profile, making GitHub a popular choice for open-source projects).

## Git Cheat Sheet
### Download and Install Git

For Microsoft Users :  [Download](https://windows.github.com/)
For Mac Users : [Download](https://mac.github.com/)

### Setup & Configuration

* Setup name that is identifible for credit when review version history
`
git config --global user.name “firstname lastname”
`

* Set an email address that will be associated with each history marker
`
git config --global user.email "valid-email"
`

*  For more uer friendly , set automatic command line coloring for Git for easy reviewing
`
git config --global color.ui auto
`

### Setup Git repository inside specific folder
* Open command prompt
* Navigate to the required location 
`cd <folder-path>`
* Before initilize the Git repo , make sure to follow above **Setup & Configuration** 
* Initilize new Git repo
`git init`
* Otherwise, You can create repo in GitHub account and clone it to that sepcific folder
`git clone <url-address>`


### Stages and Snapshots
Show modified files in working directory, staged for your next commit
```
git status
```

Add a file as it looks now to your next commit (stage)
```
git add <files>
```

Unstage a file while retaining the changes in working directory
```
git reset <files>
```

Changes you have done but not stage
```
git diff
```

Change you have done and stage but not committed

```
git diff --staged
```
Commit your all staged content as a new commit
```
git commit -m “<descriptive-message>”
```

### Tips for making meaningful commit on Git
-   Commit messages must have a subject line and may have body copy. These must be separated by a blank line.
-   The subject line must not exceed 50 characters
-   The subject line should be capitalized and must not end in a period
-   The subject line must be written in imperative mood (_Fix_, not  _Fixed_  /  _Fixes_  etc.)
-   The body copy must be wrapped at 72 columns
-   The body copy must only contain explanations as to  _what_  and  _why_, never  _how_. The latter belongs in documentation and implementation.

### Branch and Merge
Isolating work in branches, changing context, and integrating changes
Show the commit history for the currently active branch
 ```
 git branch
 ```
 Create a new branch at the current commit
 ```
 git branch [branch-name]
 ```
Switch to another branch and check it out into your working directory
 ```
 git checkout
 ```
Merge the specified branch’s history into the current one
 ```
 git merge [branch]
 ```
Show all commits in the current branch’s history
 ```
 git log
 ```
 
### Inspect and Compare

*Examining logs, diffs and object information*

Show the commit history for the currently active branch
 ```
 git log
 ```
Show the commits on branch A that are not on branch B
 ```
 git log branchB..branchA
 ```
Show the commits that changed file, even across renames 
 ```
 git log --follow <file> 
 ```
Show the diff of what is in branchA that is not in branchB
 ```
 git diff branchB...branchA 
 ```
Show any object in Git in human-readable format
 ```
 git show <object>
 ```


### Tracking Changes
*Versioning file removes and path changes*

 Delete the file from project and stage the removal for commit
 ```
 git rm <file>
```
Change an existing file path and stage the move
 ```
git mv [existing-path] [new-path] 
```
Show all commit logs with indication of any paths that moved
 ```
 git log --stat -M
 ```

### Share and Update

*Retrieving updates from another repository and updating local repos*

Add a Git URL as an alias
 ```
git remote add [alias] [url]
 ```  
Fetch down all the branches from that Git remote
 ```
git fetch [alias]
 ```
Merge a remote branch into your current branch to bring it up to date
 ```
git merge [alias]/[branch]
 ```
Transmit local branch commits to the remote repository branch
 ```
git push [alias] [branch]
 ```
Fetch and merge any commits from the tracking remote branch 
 ```
git pull 
 ```

### Rewrite History

*Rewriting branches, updating commits and clearing history*

Apply any commits of current branch ahead of specified one
 ```
 git rebase [branch]
 ```

Clear staging area, rewrite working tree from specified commit
 ```
 git reset --hard [commit]
 ```


### Temporary Commits
*Temporarily store modified, tracked files in order to change branches*

Save modified and staged changes
 ```
 git stash
```
List stack-order of stashed file changes
 ```
 git stash list
 ```
Write working from top of stash stack
 ```
 git stash pop
 ```
Discard the changes from top of stash stack 
```
 git stash drop
 ```


### What is Fork on GitHub ?
Creating a “fork” is producing a personal copy of someone else’s project. Forks act as a sort of bridge between the original repository and your personal copy.
When you **Fork** a repository, you create a copy of the original repository (upstream repository) but the repository remains on your GitHub account. Whereas, when you **Clone** a repository, the repository is copied on to your local machine with the help of **Git**.

### What is Star on GitHub ?
When you star somones repo on GitHub, you can get a notificaion when the owner update the repository and also You can star repositories and topics to discover similar projects on GitHub. When you star repositories or topics, GitHub may recommend related content in the discovery view of your news feed. For more information

### What is Issue on GitHub ?
Issues are a great way to keep track of tasks, enhancements, and bugs for your projects. They’re kind of like email  except they can be shared and discussed with the rest of your team. Most software projects have a bug tracker of some kind. GitHub’s tracker is called **Issues**, and has its own section in every repository

-   A  **title**  and  **description**  describe what the issue is all about.  
-   Color-coded  **labels**  help you categorize and filter your issues (just like labels in email)  
-   A  **milestone**  acts like a container for issues. This is useful for associating issues with specific features or project phases
-   One  **assignee**  is responsible for working on the issue at any given time.
-   **Comments**  allow anyone with access to the repository to provide feedback.

## Git and GitHub related applications

### GitHub Desktop [Download](https://desktop.github.com/) 
* **Attribute commits with collaborators easily**
Quickly add co-authors to your commit. Great for pairing and excellent for sending a little love/credit to that special someone who helped fix that gnarly bug of yours. See the attribution on the history page, undo an accidental attribution.

* **Checkout branches with pull requests and view CI statuses**
See all open pull requests for your repositories and check them out as if they were a local branch, even if they're from upstream branches or forks. See which pull requests pass commit status checks, too!

* **Syntax highlighted diffs**
The new GitHub Desktop supports syntax highlighting when viewing diffs for a variety of different languages.

### Visual Studio Code 
Using  [GitHub](https://github.com/)  with Visual Studio Code lets you share your source code and collaborate with others. GitHub integration is provided through the  [GitHub Pull Requests and Issues](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)  extension.

Install the GitHub Pull Requests and Issues extension

To get started with the GitHub in VS Code, you'll need to  [Create an account](https://help.github.com/github/getting-started-with-github/signing-up-for-a-new-github-account)  and install the  [GitHub Pull Requests and Issues](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)  extension. In this topic, we'll demonstrate how you can use some of your favorite parts of GitHub without leaving VS Code.

#### Cloning a repository
You can search for and clone a repository from GitHub using the  **Git: Clone**  command in the Command Palette (Ctrl+Shift+P) or by using the  **Clone Repository**  button in the Source Control view (available when you have no folder open).
#### Authenticating with an existing repository
Enabling authentication through GitHub happens when you run any Git action in VS Code that requires GitHub authentication, such as pushing to a repository that you're a member of or cloning a private repository. You don't need to have any special extensions installed for authentication; it is built into VS Code so that you can efficiently manage your repository.
For more Doucmentations [Click](https://code.visualstudio.com/docs/editor/github)
