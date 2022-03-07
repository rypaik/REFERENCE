https://github.com/swingology/REFERENsCE/compare/master?expand=1#diff-6f6e8bfdd114ef2cc8ae23c378569c3d2e5b39aa129ca08c2e8b5a56a690201b

https://github.com/swingology/REFERENCE/compare/master?expand=1#diff-6f6e8bfdd114ef2cc8ae23c378569c3d2e5b39aa129ca08c2e8b5a56a690201b

## @ghcli: @cheatsheet:

GITHUB CLI IS FOR GITHUB ADMINS

https://cli.github.com/manual

![IMAGE](https://i0.wp.com/build5nines.com/wp-content/uploads/2020/04/GitHub-CLI-Cheat-Sheet-Build5Nines.jpg?fit=787%2C506&ssl=1)

USAGE
  gh <command> <subcommand> [flags]

CORE COMMANDS
  | gist: |       Manage gists |
  issue:      Manage issues
  pr:         Manage pull requests
  release:    Manage GitHub releases
  repo:       Create, clone, fork, and view repositories

ACTIONS COMMANDS
  actions:    Learn about working with GitHub actions
  run:        View details about workflow runs
  workflow:   View details about GitHub Actions workflows

ADDITIONAL COMMANDS
  alias:      Create command shortcuts
  api:        Make an authenticated GitHub API request
  auth:       Login, logout, and refresh your authentication
  completion: Generate shell completion scripts
  config:     Manage configuration for gh
  help:       Help about any command
  secret:     Manage GitHub secrets
  ssh-key:    Manage SSH keys

FLAGS
  --help      Show help for command
  --version   Show gh version

EXAMPLES
  $ gh issue create
  $ gh repo clone cli/cli
  $ gh pr checkout 321

ENVIRONMENT VARIABLES
  See 'gh help environment' for the list of supported environment variables.

LEARN MORE
  Use 'gh <command> <subcommand> --help' for more information about a command.
  Read the manual at https://cli.github.com/manual

FEEDBACK
  Open an issue using 'gh issue create -R github.com/cli/cli'

quick commands

### issues

gh issue list

gh issue create --label bug

gh issue view '#25'

#### @gh repo

gh repo create

gh repo clone cli/cli

gh repove view --web

#### Working with Pull requests

You can use the `gh pr` command with a set of arguments to fully manage your pull requests.

```
  checkout:   Check out a pull request in git
  checks:     Show CI status for a single pull request
  close:      Close a pull request
  create:     Create a pull request
  diff:       View changes in a pull request
  list:       List and filter pull requests in this repository
  merge:      Merge a pull request
  ready:      Mark a pull request as ready for review
  reopen:     Reopen a pull request
  review:     Add a review to a pull request
  status:     Show status of relevant pull requests
  view:       View a pull request
```

# GITHUB

[ZSH cheatsheet for git plugin - DEV Community](https://dev.to/equiman/zsh-cheatsheet-for-git-plugin-1f6a)

# Basics

| Alias     | Command            | Description                                |
| --------- | ------------------ | ------------------------------------------ |
| `g init`  | `git init`         | Initialize a local Git repository          |
| `g clone` | `git clone <path>` | Create a local copy of a remote repository |

But sincerely, I prefer to use my own `cake` or `cape` command for cloning.

[

![equiman image](https://res.cloudinary.com/practicaldev/image/fetch/s--fZmfjfJv--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://res.cloudinary.com/practicaldev/image/fetch/s--i3D3aaTj--/c_fill%2Cf_auto%2Cfl_progressive%2Ch_150%2Cq_auto%2Cw_150/https://dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/60846/7c649d45-d4c7-4ed0-8ec1-8413e51a80d4.png)

](https://dev.to/equiman)[

## Automatic change directory after git clone

### Camilo Martinez ・ Mar 1 ・ 2 min read

#productivity #zsh #git #terminal

](https://dev.to/equiman/automatic-change-directory-after-git-clone-8ei)

# [](https://dev.to/equiman/zsh-cheatsheet-for-git-plugin-1f6a#snappshoting)Snappshoting

| Alias               | Command                        | Description                                                    |
| ------------------- | ------------------------------ | -------------------------------------------------------------- |
| `gst`               | `git status`                   | Check status                                                   |
| `gaa`               | `git add --all`                | Add all new and changed files to the staging area              |
| `grh`               | `git reset`                    | Removes all files from staging area                            |
| `ga <file>`         | `git add <file>`               | Add a file to the staging area                                 |
| `gru <file>`        | `git reset -- <file>`          | Remove a file from staging area                                |
| `gcmsg "<message>"` | `git commit -m "<message>"`    | Commit changes with message description                        |
| `gcam`              | `git commit -a -m "<message>"` | Add all new files and commit changes with message description. |

# [](https://dev.to/equiman/zsh-cheatsheet-for-git-plugin-1f6a#stash)Stash

| Alias              | Command                     | Description                                                                  |
| ------------------ | --------------------------- | ---------------------------------------------------------------------------- |
| `gsta -m <name>`   | `git stash push -m <name>`  | Create stash with name                                                       |
| `gstall -m <name>` | `git stash --all -m <name>` | Create stash with all files, including untracked and ignored files with name |
| `gstl`             | `git stash list`            | List down all your stashes                                                   |
| `gstaa stash@{n}`  | `git stash apply stash@{n}` | To apply a stash and keep it in the stash stack                              |
| `gstp stash@{n}`   | `git stash pop stash@{n}`   | To apply a stash and remove it from the stash stack                          |
| `gstd`             | `git stash drop`            | Remove a single stash entry from the list of stash entries                   |
| `gstc`             | `git stash clear`           | Remove all stashed entries                                                   |

# [](https://dev.to/equiman/zsh-cheatsheet-for-git-plugin-1f6a#branching)Branching

| Alias               | Command                         | Description                                             |
| ------------------- | ------------------------------- | ------------------------------------------------------- |
| `gb`                | `git branch`                    | List branches (the asterisk denotes the current branch) |
| `gba`               | `git branch -a`                 | List all branches (local and remote)                    |
| `gb <branch-name>`  | `git branch <branch-name>`      | Create new branch                                       |
| `gbd <branch-name>` | `git branch -d <branch-name>`   | Delete a branch                                         |
| `gcb <branch-name>` | `git checkout -b <branch-name>` | Create a new branch and switch to it                    |
| `gco <branch-name>` | `git checkout <branch-name>`    | Switch to a branch                                      |
| `gco -`             | `git checkout -`                | Switch to previous branch                               |

# [](https://dev.to/equiman/zsh-cheatsheet-for-git-plugin-1f6a#remote)Remote

| Alias                     | Command                                          | Description                                                                         |
| ------------------------- | ------------------------------------------------ | ----------------------------------------------------------------------------------- |
| `gra origin <path>`       | `git remote add origin <path>`                   | Add a remote repository                                                             |
| `grset origin <path>`     | `git remote set-url origin <path>`               | Set remote repository                                                               |
| `gf`                      | `git fetch`                                      | Gets status of 'origin'. Does not change your working directory or local repository |
| `gf <repo> <branch-name>` | `git fetch <repo> <branch-name>`                 | Get status of remote on                                                             |
| `gfa`                     | `git fetch --all --prune`                        | `Fetch all remote branches, delete branch if upstream is gone`                      |
| `gl`                      | `git pull`                                       | Incorporates changes from 'origin' into local repo                                  |
| `gl <repo> <branch-name>` | `git pull <repo> <branch-name>`                  | Incorporates changes from remote on into local repo                                 |
| `gp`                      | `git push`                                       | Incorporates changes from local repo into 'origin'                                  |
| `gpsup`                   | `git push --set-upstream origin <currentbranch>` | Set upstream current branch                                                         |
| `gp <repo> <branch-name>` | `git push <repo> <branch>`                       | Incorporates changes from local repo into remote on                                 |
| `gp -d <remote> <branch>` | `git push -d <remote> <branch>`                  | Delete remote branch                                                                |

# [](https://dev.to/equiman/zsh-cheatsheet-for-git-plugin-1f6a#merging)Merging

| Alias                                | Command                                     | Description                           |
| ------------------------------------ | ------------------------------------------- | ------------------------------------- |
| `gd <source-branch> <target-branch>` | `git diff <source-branch> <target-branch>`  | Preview changes before merging        |
| `gm <branch-name>`                   | `git merge <branch-name>`                   | Merge a branch into the active branch |
| `gm <source-branch> <target-branch>` | `git merge <source-branch> <target-branch>` | Merge a branch into a target branch   |
| `glog`                               | `git log --oneline --decorate --graph`      | View changes                          |

git push <remote> <branch>

git push <remote> --force

git puss <remote> --all

git push <remote> --tags

```
git checkout main
git fetch origin main
git rebase -i origin/main
# Squash commits, fix up commit messages etc.
git push origin main
```

SSH keys
