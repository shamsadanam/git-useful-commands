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

## If you have decided to use Git submodules for your project, here is a step-by-step guide on how to work with submodules:

1. Add a Submodule:
   - Navigate to the root directory of your repository.
   - Use the `git submodule add` command followed by the URL of the external repository and the desired path within your repository where you want the submodule to be located.
   - Example: `git submodule add https://github.com/example/repo.git path/to/submodule`

2. Initialize and Update Submodules:
   - After adding a submodule, you need to initialize and update it.
   - Use the following commands:
     ```
     git submodule init
     git submodule update
     ```
   - The `git submodule init` command initializes the submodule and sets up the necessary configuration.
   - The `git submodule update` command fetches the contents of the submodule and checks out the commit specified in your repository's submodule configuration.

3. Working with Submodules:
   - When you make changes within a submodule, you need to commit and push those changes separately within the submodule.
   - To update a submodule to the latest commit of its remote repository, navigate to the submodule's directory and use `git pull`.
   - When you're ready to update the submodule reference in your main repository, navigate to the root directory and use `git submodule update --remote`.

4. Cloning a Repository with Submodules:
   - If you clone a repository that contains submodules, you need to initialize and update the submodules explicitly.
   - Use the `git clone --recurse-submodules <repository URL>` command to clone a repository and automatically initialize and update its submodules.
   - If you've already cloned the repository and need to initialize and update submodules, use the `git submodule init` and `git submodule update` commands.

These are the basic steps to work with Git submodules. Keep in mind that each submodule maintains its own independent Git repository, so you'll need to manage and update them separately when making changes or updating the submodule reference in your main repository.

For more advanced operations and additional information, you can refer to the official Git documentation on submodules: https://git-scm.com/book/en/v2/Git-Tools-Submodules

## Clone a Repo that has submodule
```
git clone https://github.com/aikiframework/json.git --recursive
```

## If you forgot the --recursive flag you can do:
```
git submodule update --init
```




