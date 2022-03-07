SSH-AGENT

STEPS

If starting with a fresh install

[gh repo create | GitHub CLI](https://cli.github.com/manual/gh_repo_create)

[gh reference | GitHub CLI](https://cli.github.com/manual/gh_help_reference)

```shell
# create a repository under your account using the current directory name
$ git init my-project
$ cd my-project
$ gh repo create

# create a repository with a specific name
$ gh repo create my-project

# create a repository in an organization
$ gh repo create cli/my-project

# disable issues and wiki
$ gh repo create --enable-issues=false --enable-wiki=false
```

## Starting with just a blank rep

[NPM guser](https://www.npmjs.com/package/guser)

in Shell,

guser

(takes care of the git config step)

1. make local directory

2. [git init](https://git-scm.com/docs/git-init)

3. guser

4. [gh auto login -h](https://cli.github.com/manual/gh_help_reference)
   
   > *if ssh keys are in ssh-agent* - To setup ssh login
   > 
   > gh auh login -h [git@github.com](mailto:git@github.com)
   > 
   > make sure during setup process - you are already logged into the git account in browser that matches the ssh you want to usegit

5. set git config user.name and user.email

6. [gh repo create <name> <flags>](https://cli.github.com/manual/gh_repo_create)
   
   >  gh repo create test_repo --private

7. ssh-add -l      # make sure all the ssh keys are loaded

8. set git config user.name and user.email

9. 

### git commit

Say you’ve got an existing project that you want to start tracking
with git.https://github.com/ryanpaik2002/github_pull.git

```
mkdir myDirName    #this is the name of your directory
cd /myDirName
git init
touch readME.md   #this is to create an initial file to push
git commit -m "enter commit message here"
git remote add origin git@github.com:YOUR_USERNAME/myDirName.git

curl -u USERNAME:PASSWORD https://api.github.com/user/repos -d '{"name":"myDirName"}' #this will create the repo in github.

# if you haven't generated and SSH key for github access then follow these steps, otherwise you're good to push your shit to github.
eval $(ssh-agent -s)
ssh-keygen -t rsa -b 4096 -C "email@yourdomain.com" #this should be your github email address
## you'll be prompted to a couple of times. Press enter for the first prompt. choose a passphrase for the second prompt, or press enter twice for no passphrase
ssh-add ~/.ssh/id_rsa   #this is your private key
cat ~/.ssh/id_rsa.pub   # copy the output of this command. this is your SSH public key
curl -u USERNAME:PASSWORD https://api.github.com/user/keys -d '{"title":"KEY_NAME", "key":"YOUR_RSA_PUBLIC_KEY_HERE"}'   #the value you copied earlier and your keyname. I recommend using a combination of machine name and app (My-laptop (Git CLI)
git push -u origin mastermkdir myDirName    #this is the name of your directory
cd /myDirName
git init
touch readME.md   #this is to create an initial file to push
git commit -m "enter commit message here"
git remote add origin git@github.com:YOUR_USERNAME/myDirName.git

curl -u USERNAME:PASSWORD https://api.github.com/user/repos -d '{"name":"myDirName"}' #this will create the repo in github.

# if you haven't generated and SSH key for github access then follow these steps, otherwise you're good to push your shit to github.
eval $(ssh-agent -s)
ssh-keygen -t rsa -b 4096 -C "email@yourdomain.com" #this should be your github email address
## you'll be prompted to a couple of times. Press enter for the first prompt. choose a passphrase for the second prompt, or press enter twice for no passphrase
ssh-add ~/.ssh/id_rsa   #this is your private key
cat ~/.ssh/id_rsa.pub   # copy the output of this command. this is your SSH public key
curl -u USERNAME:PASSWORD https://api.github.com/user/keys -d '{"title":"KEY_NAME", "key":"YOUR_RSA_PUBLIC_KEY_HERE"}'   #the value you copied earlier and your keyname. I recommend using a combination of machine name and app (My-laptop (Git CLI)
git push -u origin master
```

- Go into the directory containing the project.
- Type `git init`.
- Type `git add` to add all of the relevant files.
- You’ll probably want to create a `.gitignore` file right away, to
  indicate all of the files you don’t want to track. Use `git add .gitignore`, too.
- Type `git commit`.

```
$ git remote add origin git@github.com:username/new_repo
$ git push -u origin master
```

Actually, the first line of the instructions will say

```
$ git remote add origin https://github.com/username/new_repo
```

[Using SSH agent forwarding - GitHub Docs](https://docs.github.com/en/developers/overview/using-ssh-agent-forwarding)

You must be using an SSH URL to check out code

SSH forwarding only works with SSH URLs, not HTTP(s) URLs. Check the .git/config file on your server and ensure the URL is an SSH-style URL like below:

```
[remote "origin"]
 url = git@github.com:yourAccount/yourProject.git
 fetch = +refs/heads/*:refs/remotes/origin/*
```

need to adjust enter data into ssh-agent 

check 

```powershell
# RESETS dentities added into ssh-agent
eval `ssh-agent -s`


# either add one key at a time using ssh-add with proper flags
or
# use ssh-agent plugin for oh-my-zsh
source ~/.zshrc             # loads up the keys in a preset

ssh-add -l                 # lists the keys loaded

to add 
ssh-add <id_rsa_key>
ssh-add -K <id_ras_key> # for Mac to rememeber the key



# Test github ssh-connection

ssh -T git@github.com

ssh -vT git@github.com
```

make sure .git/config in local repo is properly referenced by the ssh-agent

```
[remote "origin"]
 url = git@github.com:yourAccount/yourProject.git
 urls 
 fetch = +refs/heads/*:refs/remotes/origin/*
```

vim ~/.ssh/config

```
Host *
        AddKeystoAgent yes      
        # UseKeychain yes
# AddKeystoAgent must be turned on


# Ryan Github
Host github.com-ryanpaik2002
   HostName github.com
   User ryanpaik2002
   IdentityFile ~/.ssh/id_rsa_work_rp2002_github
   IdentitiesOnly yes


# Swingology Github
Host github.com-swingology
   Hostname github.com
   User swingology
   IdentityFile ~/.ssh/id_rsa_gh_swing
   IdentitiesOnly yes

.git/config (in local repository) will be referencing the Host name so they must sync


# Swingology DOCSETS REPO
Host DOCSETS.github.com
   HostName github.com
   User git
   IdentityFile ~/.ssh/id_rsa_gh_swing
   IdentitiesOnly yes
```

270

[](https://stackoverflow.com/posts/42167480/timeline)

For just one repo:

```
git config user.name "Your Name Here"
git config user.email your@email.com
```

For (global) default email (which is configured in your ~/.gitconfig):

```
git config --global user.name "Your Name Here"
git config --global user.email your@email.com
```

FROM GITHUB TO START A REPO

echo "# testproject" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main   # NAMES BRANC to main
git remote add origin git@github.com:swingology/testproject.git
git push -u origin main

### [Git Remove Remote: A Guide | Career Karma](https://careerkarma.com/blog/git-remove-remote/).....

### …or push an existing repository from the command line

git remote add origin git@github.com:swingology/testproject.git
git branch -M main
git push -u origin main

[ssh - How to tell git which private key to use? - Super User](https://superuser.com/questions/232373/how-to-tell-git-which-private-key-to-use)

## Environment variable `GIT_SSH_COMMAND`:

From Git version 2.3.0, you can use the environment variable `GIT_SSH_COMMAND` like this:

```
GIT_SSH_COMMAND="ssh -i ~/.ssh/id_rsa_example" git clone example
```

Note that `-i` can sometimes be overridden by your config file, in which case, you should give SSH an empty config file, like this:

```
GIT_SSH_COMMAND="ssh -i ~/.ssh/id_rsa_example -F /dev/null" git clone example
```

## Configuration `core.sshCommand`:

From Git version 2.10.0, you can configure
 this per repo or globally, so you don't have to set the environment 
variable any more!

1 methond

```
git config core.sshCommand "ssh -i ~/.ssh/id_rsa_example -F /dev/null"
git pull
git push
```

2 use method

Use custom host config in `~/.ssh/config`, like this:

```
Host gitlab-as-thuc  
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa.thuc
    IdentitiesOnly yes
```

then use your custom hostname like this:

```
git remote add thuc git@gitlab-as-thuc:your-repo.git  
```

## LInks

[resetting git user](https://stackoverflow.com/questions/37486350/local-git-config-not-overriding-global-user-for-projecthttps://stackoverflow.com/questions/37486350/local-git-config-not-overriding-global-user-for-project)

```shell
git config --local --git config user.name "Your Name Here"git config user.email you credential.helper
git config --global --unset credential.helper
git config --system --unset credential.helper 
```

from git

https://docs.github.com/en/github/getting-started-with-github/getting-started-with-git/setting-your-username-in-git

```shell
/c/ global/windows git config files (master) 
$ sudo git config --edit --global
 ~/.gitconfig

$ sudo git config --edit --system
>>/usr/local/etc/gitconfig   
```

GIT CONFIG 

[Git - Git Configuration](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration)

[Where to find system, global and local Git config files on Windows and Ubuntu Linux - Coffee Talk: Java, News, Stories and Opinions](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/Where-system-global-and-local-Windows-Git-config-files-are-saved)

[The Git working tree, index and commit history explained by example](https://www.theserverside.com/video/Understand-the-Git-working-tree-status-command-for-easy-DVCS)

[git - Can I specify multiple users for myself in .gitconfig? - Stack Overflow](https://stackoverflow.com/questions/4220416/can-i-specify-multiple-users-for-myself-in-gitconfig)

```shell
Global config ~/.gitconfig

[user]
    name = John Doe
    email = john@doe.tld

[includeIf "gitdir:~/work/"]
    path = ~/work/.gitconfig

Work specific config ~/work/.gitconfig

[user]
    email = john.doe@company.tld
```

[Managing remote repositories - GitHub Docs](https://docs.github.com/en/github/getting-started-with-github/getting-started-with-git/managing-remote-repositories)

[Managing remote repositories - GitHub Docs](https://docs.github.com/en/github/getting-started-with-github/getting-started-with-git/managing-remote-repositories#renaming-a-remote-repository)

[Managing remote repositories - GitHub Docs](https://docs.github.com/en/github/getting-started-with-github/getting-started-with-git/managing-remote-repositories#removing-a-remote-repository)

## Useful Git commands

git remote -v

git remote

git status

git branch

[git checkout](https://git-scm.com/docs/git-checkout)

[git config](https://git-scm.com/docs/git-config)

124

[](https://stackoverflow.com/posts/19730914/timeline)

If you've already committed a bunch of unwanted files, you can unstage them *and* tell git to mark them as deleted (without actually deleting them) with

git reset HEAD -- path/to/file

git reset HEAD  -- . 

git reset @  # @ is HEAD

```
# If you've already committed a bunch of unwanted files, you can unstage them and tell git to mark them as deleted (without actually deleting them) with 
git rm --cached -r .
```

Now at v2.24.0 suggests

```
git restore --staged <individual_file>
git restore --staged .
```

to unstage files.

```shell
git add -A
to reverse

git rest
git reset HEAD . 
git check```

git checkout -- .
```

______

git show-ref

From `git branch` it appears that somehow your local branch name is "origin".

You can rename the branch with `-mv` flag, like this:

`git branch -mv origin master`

After this `git branch` should show `master` :-)

[How can I reset a Git repository to its newly-cloned state? - Stack Overflow](https://stackoverflow.com/questions/52995503/how-can-i-reset-a-git-repository-to-its-newly-cloned-state)

Your best option to remove all local artifacts is to make a fresh [clone](https://git-scm.com/docs/git-clone).

Otherwise, you have to run different commands to perform the individual components of the cleanup.

To get rid of all untracked files, use [`git clean`](https://git-scm.com/docs/git-clean), with any number of flags turned on to wipe out everything:

```
git clean -fd
```

Now rest all your branches to the remote version ([`git reset`](https://git-scm.com/docs/git-reset)) or delete them if they are local-only ([`git branch`](https://git-scm.com/docs/git-branch)):

```
git checkout master
git reset --hard origin/master

git branch -d local-branch
```

The same goes for tags. You can delete all local tags like this:

```
git tag -d $(git tag -l)
```

## working example

```shell
# .git/config in repo


[remote "master"]
        url="ssh://git@github.com:swingology/DOCSETS.git"
[user]
        name = swingology
        email = swingology19@gmail.com
[remote "docsets"]
        url = git@github.com:swingology/DOCSETS.git
        fetch = +refs/heads/*:refs/remotes/docsets/*
[branch "main"]
        remote = docsets
        merge = refs/heads/main
~
```

```shell
# ~/.ssh/config

Host * 
        AddKeystoAgent yes      
        # UseKeychain yes



# Ryan Github
Host github.com-ryanpaik2002
   HostName github.com
   User git
   IdentityFile ~/.ssh/id_rsa_work_rp2002_github
   IdentitiesOnly yes


# Swingology Github
Host github.com-swingology
   Hostname github.com
   User git
   IdentityFile ~/.ssh/id_rsa_gh_swing
   IdentitiesOnly yes


# Swingology DOCSETS REPO
Host DOCSETS.github.com
   HostName github.com
   User git
   IdentityFile ~/.ssh/id_rsa_gh_swing
   IdentitiesOnly yes


core]
        repositoryformatversion = 0
        filemode = true
        bare = false
        logallrefupdates = true
```

### 

## MORE LINKS

[How to change remote git repository | XENOVATION](https://xenovation.com/blog/source-control-management/git/how-to-change-remote-git-repository)

[Push identical code into two git remote repositories | XENOVATION](https://xenovation.com/blog/source-control-management/git/push-code-into-two-git-remote-repositories)

https://xenovation.com/blog/source-control-management/git/git-revert-commit
