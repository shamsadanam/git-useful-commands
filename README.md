# git-useful-commands
## Adding Username and Email
```
git config --global user.name "username"
git config --global user.email "email@here.please"
```

## Logout/Unset Credentials from/in a device
```
git config --global --unset-all user.name
git config --global --unset-all user.email
```

## Undo All Changes to Last Commit
[source](https://stackoverflow.com/questions/4630312/reset-all-changes-after-last-commit-in-git)
### First, reset any changes
This will undo any changes you've made to tracked files and restore deleted files:
```
git reset HEAD --hard
```

### Second, remove new files
This will delete any new files that were added since the last commit:
```
git clean -fd
```



