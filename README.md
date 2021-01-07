# Git and GitHub
Git is a distributed version-control system for tracking changes in any set of files, originally designed for coordinating work among programmers cooperating on source code during software development.

### Difference between Git and GitHub
#### What is Git ?
First developed back in 2005, Git is an extremely popular version control system that is at the heart of a wide variety of high-profile projects. Git is installed and maintained on your local system (rather than in the cloud) and gives you a self-contained record of your ongoing programming versions. It can be used completely exclusive of any cloud-hosting service, you don’t even need internet access, except to download it.

#### What is GitHub ?
GitHub is designed as a Git repository hosting service. It’s an online database that allows you to keep track of and share your Git version control projects outside of your local computer/server. Unlike Git, GitHub is exclusively cloud-based. Also unlike Git, GitHub is a for-profit service (although basic repository-hosting features are available at no cost to those who are willing to create a user profile, making GitHub a popular choice for open-source projects).

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
 
 
 
