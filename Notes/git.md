# Git Notes
## Introduction
Git is a version control system that allows you to track changes in your code and collaborate with others effeciently. It keeps a history of your work, making it easy to revert changes if something goes wrong. Using Git brings numerous advantages that enhance the development process for both individual developers and teams. Here are some compelling reasons to incorporate Git into your workflow:
- Staging and Version control
- Undoing Mistakes and Collaboration
- Integration with Other Tools and Branching & MErging
- Community and Support and Distributed System
- Standard in the Industry and Tracking Changes

## What makes a Good Commit vs Bad Commit
### Atomic changes
Any time something is changed, it must be committed to Github, however there is a difference between a good commit and bad commit. A good commit should consist of only one atomic change in the code for example "added user authentication", whereas if you have multiple changes then that would be a bad commit - "added user authentication and update UI styles. This makes the project easier to track and troubleshoot.

### Descriptive Commit Message
Every commit message should describe exactly what was done, rather than a generalised description such as "fixed bug" - this does not help anyone who looks at the code. The message should be specific and descriptive such as "Fix correct null pointer exception in user login.

git commit - m "Add user authentication"

## Using Git with Command Line
To start using Git, we are first going to open up our Command shell. For Windows, you can use Git Bash.

### mkdir
You can make a new folder for a project using the command mkdir and then change the current working directory to it by using the command cd.
```
mkdir Newproject
cd Newproject
```

### git init
You can initialise a new Git repository in the current directory using git init. It sets up the basic files and directories needed to start tracking changes.
```
git init
```

### git status
You can check the current status of the repositiory using git status or git status -s. This command shows the status of the repository and the changes that are currently staged or unstaged.
```
git status
git status -s
```

### git add
Add a file or directory to the staging area. This command prepares the changes for the next commit. It adds the specified file or directory to the index.
To add a single file:
```
git add <got cofile>
```
To add all files:
```
git add .
git add -A
```
To add all files in a directory:
```
git add <directory>
```

### git commit
Creates a new commit with a message describing the changes made. This command creates a new commit with the changes you made to your local repository. The commit message describes the changes made in this commit.
```
git commit -m "commit message"
git commit --message "commit message"
```

### git push
This command pushes the local changes to the remote repository. It updates the 'remote' repository with the changes you made locally. This is something you would use both, if you are working by yourself and with others - pushing any changes you make back to the remote repository.
```
git push
```
To push for a specific branch:
```
git push origin main
```

### git pull
This command updates the local repository with changes from the remote repository, to put directly into the working directory. It pulls the changes from the remote repository and merges them with the local changes. This is something you will likely only use when working with others, for example someone else changes code, or writes new code and has pushed to the repository. Then you need to write something using that updated code, but you don't have their updates on your local repository - so you pull from the remote repository. This can apply to working on open source projects also.
```
git pull
```
For a specific branch example -main branch
```
git pull origin main
```
Note - git pull is like combining git fetch + git merge. It does both of those things in one command.

### git clone
This command clones an existing Git repository on your local machine. It copies the entire history and files of the specified repository to your local machine. First, navigate to the directory where you want to clone the repository. Then, run the git clone command followed by the URL of the repository you want to clone. 
```
git clone <repository-url>
```
Note - this is refering to a local link, not a website link.

### git branch
#### Create branch
This command creates a new branch with the name branch_name. The new branch is created based on the current branch. The current branch is the branch you are currently on. The new branch will have the same commit history as the current branch.
```
git branch branch_name
```

#### List Branches
This command lists all the branches in the repository. It shows the current branch you're on and highlights it with an asterisk.
```
git branch
git branch --list
```

### git checkout
This command switches to the branch_name branch. It changes the working directory to the branch specified. The changes in the working directory are based on the branch you switch to.
```
git checkout branch_name
```
If you wanted to switch to the main branch:
```
git checkout main
```

### git merge
This command merges the changes from the branch_name branch into the current branch. It creates a new commit that includes the changes from both branches.
```
git merge branch_name
```

### git branch -d (delete)
This command deletes the branch with the name branch_name. The branch must be fully merged into the current branch before it can be delted. If the branch has unmerged changs the command will fail. To force delete the branch anyway, use the -D option instead of -d.
```
git branch -d branch_name
```
This command deletes the branch even if it has unmerged changes. It is recommended to use this command with caution as it can result in data loss.

### git log
This command shows the commit history of the repository. It displays the commit hash, author, date, and commit message for each commit. The output is displayed in reverse chronological order, with the most recent commit at the top. The output is displayed in reverse chronological order, with the most recent commit at the top.
```
git log
```

### git diff
This command shows the changes between the working directory and the staging area. It displays the differences line by line for each file that has been modified, but not yet staged. The output is displayed in a unified diff format, which shows the removed lines with a '-' prefix and added lines with a '+' prefix.
```
git diff
```
To view the changes between the staging area and the last commit, you can use the following command:
```
git diff --staged
```

### git fetch
This command fetches the changes from the remote repository to the local repository. It updates the remote tracking branches in the local repository. The changes are not merged with the local branches. To merge the changes, you can use the git merge command.
```
git fetch
```

### git remote
#### List remote repositories
This command lists the remote repositories that are associated with the local repository. The -v flag shows the URLs of the remote repositories.
```
git remote -v
```

#### Add a remote repository
This command adds a new remote repository to the local repository. The remote_name is the name of the remote repository, and remote_url is the URL of the remote repository.
```
git remote add remote_name remote_url
```

#### Remove a remote repository
This command removes the remote repository with the name remote_name from the local repository.
```
git remote remove remote_name
```
### git reset
This command resets the changes in the working directory to the last commit. The changes in the staging area are preserved. The changes in the working directory are not preserved. The changes are not committed to the repository. The changes are not pushed to the remote repository.
```
git reset
```

#### For a specific file
This command resets the changes in the working directory to the specified file to the last commit, and does the same as git reset,
```
git reset file.txt
```

#### For a specific commit
This command resets the changes in the working directory for the specified commit. Example directory "HEAD~1"
```
git reset HEAD~1
```

#### For a specific commit and preserve changes
This command resets the changes in the working directory to the specific commit. The changes in the staging area are preserved, and the changes in the working directory are preserved. The changes are not committed to the repository. The changes are not pushed to the remote repository. Example directory "HEAD~1"
```
git reset --soft HEAD~1
```

#### For a specific commit and discard changes
This command resets the changes in the working directory to the specific commit. The changes in the staging area are discarded, and the changes in the working directory are discarded. The changes are not committed to the repository. The changes are not pushed to the remote repository. Example directory "HEAD~1"
```
git reset --hard HEAD~1
```

### git revert
This command creates a new commit that undoes the changes made in the specified commit. It does not delete the specified commit, but it creates a new commit that reverts the changes made in that commit.
```
git revert commit_hash
```

## .gitignore
We can use a .gitignore file in our project to include any files that we don't want to be uploaded to github. The way this is done is by stating the file extensions within the code.

For example, we could exclude .env files which store special API keys with are used to authenticate you with the API. These keys must be protected.