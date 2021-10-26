# Note Summary

This note is for the purpose of recording the basic and experienced use cases of different commands.

## Command

----

### **git init**

`git init` is for initializing a new git repository. To use it:


    // in the root directory of your project
    > git init


### **git add**

`git add` is to stage changes that being made in the git repository.

    > git add *file*

### **git branch**

`git branch` is to list, create and delete branches.

#### *Create new branch*

    > git branch newBranchName

#### *List existing branches*

    > git branch --list

#### *Delete branch*

    > git branch -d targetBranchName

### **git checkout**

`git checkout` can be used to switch branch or create new branch.

#### *Switch branch*

    > git checkout targetBranch

#### *Create new branch and switch to it*

    > git checkout -b newBranchName

