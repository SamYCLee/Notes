# Git Application

## Caption

This note is dedicated for git application general information.

## What is Git ?

Git is a source control program which helps on both individual software development and teamwork software development.

In terms of individual software development process, Git has the following main benefits:

- Software version control
- Source code back-up in terms of changes

In terms of team-based software development process, it has even more benefits:

- Traceable workflow
- Better merging management
- More effective development process (**applying branch model**)

## How to use Git

In terms of individual software development process, **commit** is still very useful as it is contributed to the version control aspect as well as the code back-up in terms of changes. While the **push** and **pull** is
__not really useful__ as there are no remote origin involved.

- Branch model can still be applied as it helps to isolate your code for development needs.
- In additions, it also helps yourself to check and manage your development process and schedule.

## Not to
Since git is a source control program and it stores all your code changes like snapshots so that you can take it
back if you want, it should only be used on tracking your source code only, For other bin files like images, do not
use git to monitor these directories.

- If you try to use it like these, the size of the record file **\*.git** will increase dramatically comparing to the normal situation and more resources of your computer are used in a wasteful way. 

This can be avoided by using the **.gitignore file**. The files and directories mentioned in the **.gitignore file** will be
ignored by git.
