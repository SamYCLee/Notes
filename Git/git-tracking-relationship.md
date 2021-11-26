# Git Tracking Relationship

## Caption

This note is a brief record of the [reference][1].

## What is tracking relationship? Why should I set it up?

Setting up a tracking relationship in git between the local branch and the remote branch means that a creation has been created so that git can compare and remind you about the HEAD differences of the two branches.

With the tracking relation, one's can manage the version's more easily and accurately. Moreover, when using commands like `git pull` or `git push`, you can simply use the command itself without any other flags and target location in order to tell git which remote branch that you are pushing/pulling.

## How to set up the tracking relation?

To set up the tracking relation between the local branch and the remote branch, there are 3 scenarios :

- *Work on a new branch from the remote repository*

    > git checkout --track remoteRepository/branchName

- *Push a new local branch to the remote repository*

    > git push -u remoteRepository branchName

- *Set up the tracking relationship in a later point of time*

    > git branch -u remoteRepository/branchName

[1]: https://www.git-tower.com/learn/git/faq/track-remote-upstream-branch