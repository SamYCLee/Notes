# Git - Five Branch Model

## Five Branches

In each project, we will ALWAYS keep TWO (2) branches alive forever (master & develop).

Below is a table to summarise different branches.

| Name | Type | Branch off from | Merge back to | Remarks |
|----|----|----|----|----|
| master | main | - | - | Never delete |
| develop | main | - | - | Never delete |
| feature | supporting | develop | develop |  |
| release | supporting | develop & develop | master & develop |  |
| hotfix | supporting | master | master & develop |  |

### Master branch

**Purpose of Master Branch:**

- The current version of the software that are using by the customers
- The initial point/base of all branches in the development process for every new version of software or new software
- The final version/product that be delivered to the customers

**Way of Practice:**

- Only one master branch in a project
- Should only be merged with the develop branch and hotfix branch
- When being merged with the develop branch, make sure that all features that intended to deliver in the new version should be merged with the develop branch already

### Develop branch

**Purpose of Develop branch:**

- Contains the original software code with more workable and checked features added, waiting for being delivered to the customer
- Can be deemed as the next version of the software

**Way of Practice:**

- Only one develop branch in a project
- The base of the other features
- Should be merged with release branch
- Should only be merged with when the features are workable and being checked by the others (other developers, program manager, test engineer)

### Feature branch

#### Purpose of Feature branch

- Representing a specific feature to be developed
- When developing multiple features in a team at the same time, better isolation of code helps preventing the work from the others affects you all the time
- Help tracing what you have done as well as debugging

#### Way of Practice

- Feature branches can have more than one at the same time period (as multiple new features are being developed at the same time)
- As there may be multiple functions to be developed to make a feature, commit it each time when you have done part of the features, like finishing one of the functions inside that feature
- Think of the commits as the milestones of developing this feature
- When the feature branch finished its development, the feature branch should be merged to a new release branch created from the develop branch directly

#### Git operations

If you need to add a new feature/module, create a new feature branch as follows:

- checkout develop branch

```shell
git checkout develop
```

- git pull
- add new feature branch

```shell
git branch hotel-booking
```

- checkout new branch

```shell
git checkout hotel-booking
```

Then write your code in the new branch. When it is ready, merge it back to develop ONLY as follows:

- git commit and push from feature branch
- checkout develop

```shell
git checkout develop
```

- merge the feature branch to develop

```shell
git merge --no-ff hotel-booking
```

- git push from develop

```shell
git push
```

### Release branch (very important)

> **_Note:_** The usage of release branch in this practice is slightly different from other people.

#### Purpose of Release branch

- As a buffer when merging a new feature to the develop/master branch
- For the other people (project manager, test engineer, etc.) to check whether the added feature can fulfill all the requirements/specifications

#### Way of Practice

- Should be created when the development of a feature/hotfix branch is completed and start to merge with the develop/master branch
- Fix all conflicts, if any, during the merging
- May need to modify the local environment before testing, e.g. server IP
- If say feature A is required to test or check with the existence of the feature B, the release branch of feature A should be formed by merging feature A and the release branch of feature B

#### Practice flow

After the development work is finished for a feature or hotfix branch, you need to create a release branch for testing. The order of merging is reversed for feature (develop) and hotfix (master) branch.

> Feature branch

- You want to merge your feature branch back to develop branch after finish
- Add a "dev_rel_xx" release branch from develop
- merge your feature branch to this "dev_rel_xx" release branch
- make any local environment changes, e.g. change template, config, testing server IP
- test your code
  - if ok, merge this "dev_rel_xx" branch back to develop branch
  - if not ok, delete this "dev_rel_xx" branch and continue to work on your feature branch.
- after merge back to develop branch, test again
  - if ok, add a new "master_rel_xx" release  branch from master branch
  - merge the develop branch to this "master_rel_xx" release branch
  - make any local environment changes, e.g. change template, config, production server IP
  - test again
    - if ok, merge "master_rel_xx" branch back to master branch
    - if not ok, delete this "master_rel_xx" branch and continue to work on your feature branch.

> Hotfix branch

- You want to merge your hotfix branch back to master branch after finish
- Add a "master_rel_xx" release branch from master
- merge your hotfix branch to this "master_rel_xx" release branch
- make any local environment changes, e.g. change template, config, testing server IP
- test your code
  - if ok, merge this "master_rel_xx" branch back to master branch
  - if not ok, delete this "master_rel_xx" branch and continue to work on your hotfix branch.
- after merge back to master branch, test again
  - if ok, add a new "dev_rel_xx" release  branch from develop branch
  - merge the hotfix branch to this "dev_rel_xx" release branch
  - make any local environment changes, e.g. change template, config, production server IP
  - test again
    - if ok, merge "dev_rel_xx" branch back to develop branch
    - if not ok, delete this "dev_rel_xx" branch and continue to work on your hotfix branch.

> Multiple Feature Branches

- if you have more than 1 feature branch want to test
- add "dev_rel_1" from develop branch as above
- merge "feature 1" to "dev_rel_1" branch and test
  - if ok, add "dev_rel_2" from "dev_rel_1" branch
    - merge "feature 2" to "dev_rel_2" branch and test
    - in this case, you have both "feature 1" and "feature 2" on "dev_rel_2" branch
    - continue to add more release branches until all new feature branches are tested.

### Hotfix branch

#### Purpose

- Use for fixing bugs found in the current using software (Master Branch)

#### Way of Practice

- For each bug is found, there is a single Hotfix branch for that particular bug.
- Should be merged to Master branch AND Develop branch after the bugs is fixed

#### Git operation steps

Always create hotfix branch from master. Follow these steps:

- checkout master branch

```shell
git checkout master
```

- git pull
- add new hotfix branch (e.g. hotfix-0.5.4) change the 3rd digit for hotfix.

Do your work in the new hotfix branch. When complete, merge it back to BOTH master & develop by

- git commit and push from hotfix branch
- checkout master
- merge the hotfix branch to master

```shell
git merge --no-ff hotfix-0.5.4
```

- git push from master
- checkout develop

```shell
git checkout develop
```

- merge the hotfix branch to develop

```shell
git merge --no-ff hotfix-0.5.4
```

- git push from develop

```shell
git push
```

## Reference

- <http://nvie.com/posts/a-successful-git-branching-model/>
