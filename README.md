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

## First, reset any changes
This will undo any changes you've made to tracked files and restore deleted files:
```
git reset HEAD --hard
```

## Second, remove new files
This will delete any new files that were added since the last commit:
```
git clean -fd
```

*Files that are not tracked due to .gitignore are preserved; they will not be removed*

