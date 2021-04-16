### To install git 
```
yum -y install git
apt-get install git -y
```

### To check if git is install
```
git --version
```

### To initialize a new local empty repository
```
mkdir git
cd git
git init
```

### This will show you .git which means local repo
```
ls -a
```

### What is the folder called .git?
- The `.git `folder is the directory which is created when you do `git init` `.git `folder makes your project a "git" repository. Without `.git`, your project is a local project and not a git project, that means you cannot perform any git operations.

- The .git folder contains all the information that is necessary for your project in version control and all the information about commits, remote repository address, etc. All of them are present in this folder. It also contains a log that stores your commit history so that you can roll back to history.

- git stores the metadata and object database for the project in this directory like:
    - Remote information (to which remote server your project is connected)
    - History of all local commits
    - Branch information (on which branch is your current project state (HEAD) pointing to)
    - All logs of all local commits you have ever made (including revert changes)
    - The config file will hold all the configuration






### list all the branch
git branch -a

### Configure your Git username/email
git config --global user.name "Name"
git config --global user.email "Email"

### To list the global configuration
git config --list

### Delete a feature branch
git branch -D feature/EC-2511

### Create a feature branch
git branch feature/EC-3060

### Push a branch 
git push origin feature/EC-3060


### delete branch locally
git branch -d localBranchName

### delete branch remotely
git push origin --delete remoteBranchName

### Add you indentity into git 
git config --global user.name "Name"
git config --global user.email Email.com

### How do I show my global Git configuration?
git config --list
git config --edit --global
cat ~/.gitconfig

### Git Basics - Tagging
git tag -a v1.4 -m "my version 1.4"
git tag
git show v1.4


### Renaming Git Branch
- Follow the steps below to rename a Local and Remote Git Branch:

* list all the branches
git branch -a

* Start by switching to the local branch which you want to rename:
git checkout <old_name>

* Rename the local branch by typing:
git branch -m <new_name>

* Push the <new_name> local branch and reset the upstream branch:
git push origin -u <new_name>

* Delete the <old_name> remote branch:
git push origin --delete <old_name>