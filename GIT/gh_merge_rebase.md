## LINKS

[merging vs rebbasing](https://www.atlassian.com/git/tutorials/merging-vs-rebasing)





## MERGING

git checkout feature 

git merge main

or

git merge feature main

git merge <source branch> < branch to be merged>



![img](https://wac-cdn.atlassian.com/dam/jcr:4639eeb8-e417-434a-a3f8-a972277fc66a/02%20Merging%20main%20into%20the%20feature%20branh.svg?cdnVersion=1665)



PROS:

non destructive

Avoids pitfalls of rebase



CONS:

creates extraneous merge commit everytime you need to incorporate upstream changes

**upstream** generally refers to the original repo that you have forked.





## REBASE

takes the curret branch and places all commits on teh target branch



git checkout feature

git rebase -i main 			# interactive

- reports all the cocmmits that are about to be moved





GOLDEN RULES OF REBASING

- The golden rule of `git rebase` is to never use it on *public* branches.





## FORCE PUSHING

git push --force



***example:***

If you try to push the rebased `main` branch back to a remote repository, Git will prevent you from doing so because it conflicts with the remote `main` branch.



 you can force the push to go through by passing the `--force` flag, like so:

```shell
 git push --force
```

This overwrites the remote `main` branch to match the rebased one from your repository and makes things very confusing for the rest of your team.





## WORKFLOW

###  Local Cleanup

One of the best ways to incorporate rebasing into your workflow is to clean up local, in-progress features. By periodically performing an  interactive rebase, you can make sure each commit in your feature is  focused and meaningful. This lets you write your code without worrying  about breaking it up into isolated commits—you can fix it up after the  fact.



```
git checkout feature git rebase -i HEAD~3

or 
git merge-base feature main
```

By specifying `HEAD~3` as the new base, you’re not actually  moving the branch—you’re just interactively re-writing the 3 commits  that follow it. Note that this will *not* incorporate upstream changes into the `feature` branch.

![image](https://wac-cdn.atlassian.com/dam/jcr:51d9f126-1fc1-4c6c-ba52-c4085cd59002/07%20Rebasing%20into%20Head-3.svg?cdnVersion=1665)