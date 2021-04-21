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
```
tree .git
```
- The `.git `folder is the directory which is created when you do `git init` `.git `folder makes your project a "git" repository. Without `.git`, your project is a local project and not a git project, that means you cannot perform any git operations.

- The .git folder contains all the information that is necessary for your project in version control and all the information about commits, remote repository address, etc. All of them are present in this folder. It also contains a log that stores your commit history so that you can roll back to history.

- git stores the metadata and object database for the project in this directory like:
    - Remote information (to which remote server your project is connected)
    - History of all local commits
    - Branch information (on which branch is your current project state (HEAD) pointing to)
    - All logs of all local commits you have ever made (including revert changes)
    - The config file will hold all the configuration


### Add you name and email
This is to know who commited something when we type git log

### To add you name 
```
git config --global user.name "Your Name"
git config --global user.name "Tia M"
```

### To add you email 
```
git config --global user.email "your email address"
git config --global user.email "tia@gmail.com"
```

### To list the global configuration
```
git config --list
or 
cat ~/.gitconfig
```

### Create a new repo in Github
- [How to create a repository in github](https://docs.github.com/en/github/getting-started-with-github/create-a-repo)
- Create a new repository
- Repository name Add a README file


### What is .gitignore file in Git?
- [Ignoring files](https://docs.github.com/en/github/getting-started-with-github/ignoring-files)

- You can configure Git to ignore files you don't want to check in to GitHub.
- You can create a .gitignore file in your repository's root directory to tell Git which files and directories to ignore when you make a commit.
```
$ touch .gitignore
```
```
# Terraform
**/.terraform/*
terraform.tfvars
*.tfstate
*.tfstate.*
*.terraform
backend.tf
provider.tf
```

### What is a README file in Git?
- [About READMEs](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/about-readmes)

- You can add a **README** file to your repository to tell other people why your project is useful, what they can do with your project, and how they can use it.

- **A README** is often the first item a visitor will see when visiting your repository. README files typically include information on:
    - What the project does
    - Why the project is useful
    - How users can get started with the project
    - Where users can get help with your project
    - Who maintains and contributes to the project


### How to delete a repository in github?
[Deleting a repository](https://docs.github.com/en/github/administering-a-repository/deleting-a-repository)

1. On GitHub, navigate to the main page of the repository.
2. Under your repository name, click Settings.
3. Under Danger Zone, click Delete this repository.
4. Read the warnings.
5. To verify that you're deleting the correct repository, type the name of the repository you want to delete and hit delete


### Create a new repo in Github without README file
- Create a new repository
- Repository name and hit create

### Create a new repository on the command line
```
echo "# test" >> README.md
git init
git add README.md or git add .
git status
git commit -m "first commit"
git branch -M main
git branch -a
git remote add origin https://github.com/leonardtia1/test.git
git push -u origin main
```

### Push an existing repository from the command line
```
git remote add origin https://github.com/leonardtia1/test.git
git branch -M main
git push -u origin main
```

### Github authentification 
- 3 ways to authenticate Github:
    - Personal access token
    - Username and password (HTTPS: This is the default one)
    - SSH
**NB:** SSH is the most widley used by companies our there for Github authentification


### Github authentification with personal access token
[Creating a personal access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token)

- Personal access tokens (PATs) are an alternative to using passwords for authentication to GitHub when using the GitHub API or the command line.

- You should create a personal access token to use in place of a password with the command line or with the API.

- As a security precaution, GitHub automatically removes personal access tokens that haven't been used in a year.

- Personal access tokens can only be used for HTTPS Git operations. If your repository uses an SSH remote URL, you will need to switch the remote from SSH to HTTPS.

**Using a token on the command line:**
- Once you have a token, you can enter it instead of your password when performing Git operations over HTTPS.
- For example, on the command line you would enter the following:
```
$ git clone https://github.com/username/repo.git
Username: your_username
Password: your_token
```

### Github Enterprise authentification with SSH
[Connecting to GitHub with SSH](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)

**About SSH**
Using the SSH protocol, you can connect and authenticate to remote servers and services. With SSH keys, you can connect to GitHub without supplying your username and personal access token at each visit.

**Generating a new SSH key and adding it to the ssh-agent**
```
ssh-keygen -t ed25519 -C "your_email@example.com"
sh-keygen -t ed25519 -C "jean.paul@tcs.com"
cd /root/.ssh/
```

**Adding your SSH key to the ssh-agent**
```
$ eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```
**Add the SSH key to your GitHub account.**
```
cat /root/.ssh/id_ed25519.pub

ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIBIWJDbpAkgztMeT2x/mUMTqPADK9Htt1LN3BmhOC8PG jean.paul@tcs.com
```

**Another way to authenticate github with ssh but not use by companies our there.**
```
mkdir -p /root/tmp/.ssh
ssh-keygen
/root/tmp/.ssh/id_rsa.pub
```

### How to use a shell script to push code to Github?
```sh
read -r -p 'Commit message: ' desc  # prompt user for commit message
git add .                           # track all files
git commit -m "$desc"               # commit with message
git push -u origin master           # push to origin
```








### list all the branch
git branch -a


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