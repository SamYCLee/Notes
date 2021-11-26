# Remove directory from Git history

## Command

```shell
> git filter-branch --tree-filter 'rm -rf [directory]' --prune-empty HEAD
> git for-each-ref --format="%(refname)" refs/original/ | xargs -n 1 git update-ref -d
echo [direcrtory]/ >> .gitignore # if needed
> git add .gitignore # if .gitignore is edited
> git commit -m 'Removing [directory] from git history' #if .gitignore is edited
> git gc
> git push origin master --force
```

## Reference

- <https://stackoverflow.com/questions/10067848/remove-folder-and-its-contents-from-git-githubs-history>