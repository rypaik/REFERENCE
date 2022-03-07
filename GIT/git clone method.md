# GIT CLONE METHOD

## SETUP

#### FROM GITHUB SITE

Create an empty repo

git clone with https address in the directory

LOCAL REPO

create a blank directory

git clone https://git.******/rep.git      # address of repo

------

   # I HAD TO 

git init                        # blank out the

-----

guser                # follow directions

ESLE: if it doesn't work

git config -l            # looks at git repo details

> git config user.name "<USER NAME>"
> 
> git config user.email "<USER EMAIL>"

git add README.md
git commit -m "first commit"

// Names first commit branch as main

git branch -M main                               # NAMES BRANCH to main

// gives the repo a label of origin so you don't ahve to keep punching in address on every pus

git remote add origin [git@github.com](mailto:git@github.com)/ryanpaik2002/github_pull.git

//PUSH

git push -u origin main

// to do a one way pull without overwriting

git pull origin main
