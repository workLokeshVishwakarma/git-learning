## Get good at git
#### <i>CreatedBy - Linus torvalds in 2005</i>

<hr />

* First download git https://git-scm.com/downloads if you don’t have already

<hr />

#### To get | global’s

`git config -l` or `git config --global --list`

#### To set | globally

`git config --global user.name "name"`

`git config --global user.email "email"`

<hr />

#### # How to see remote upstream url

`git ls-remote --get-url`
Or
`git config --get remote.origin.url`

<i>URL_example - git@github.com:username/repo-name.git</i>

#### # To edit / update origin->URL
`git remote set-url origin <URL>`

#### # To add origin->URL
`git remote add origin <URL>`

<hr />

```
Post 2020 branch name - master changed to
main
mega
mucho
```

#### See local branches using

`git branch`

#### To rename master to main, checkout master and run `git branch -m master main`.

This will rename the master branch to main. If you are not currently on the master branch, you can use the checkout command to switch to it. For example, to switch to the master branch, you would use the following command:

`git checkout master`

Once you are on the master branch, you can use the `branch` command to rename it. For example, to rename the master branch to main, you would use the following command: (if you are in the master)

`git branch -M main`

#### Run following command to check

`git status`

<hr />

### Vim <i><sup>(editor)</sup></i>

* To create a file - `touch file_name.extension`, or if you wanna create folder use `mkdir folder_name`
 
    - `touch index.html`es
    - `mkdir src`

* Then to edit a file, use `vim file_name.extension`

    - `vim index.html`
        - then hit `i` for insert mode
        - and as you complete your editing
            - hit `esc` then type `:wq`

                  `esc` to escape from edit mode
                  and `w` for save the file
                  `q` for quite

            - Or if you don’t wanna edit-save the your file (wanna discard your changes, exit file without saving), you can use
                - `q!` For discard and quite
                              
                      hit `esc` then type `:q!`


* Or if you wanna delete

    - File `rm file_name.extension`

    - Folder Forcefully / Recursive Force `rm -rf folder_name`


* And for rename

    - File `mv file_name.extension new_file_name.extension`

    - Folder
    `mv folder_name new_folder_name`

<hr />

### # Staging Changes
Moving it to the staging area, marking it for inclusion in the next commit. You can select all files, a directory or specific files as well for staging area to include in next commit. This means if you git add a deleted file the deletion is staged for commit. (If you wanna delete that file which you had included in previous commit).

`git add .`

### # Commiting changes
Now finally commiting changes moving from staging area to snapshot `.git` -> `localrepo` / commits area | called commiting a changes.

`git commit -m "commit msg"`

### # There's one Shorthand as well
This will gonna work for only those files, which are under `.git` tracking, will not gonna work for files which are showing in `U` or untracked, for those file you have to use `git add .` or `git add fileName.extension` first time / (once) at least manually, and then from the next time `-am` will properly gonna automate your work for you.

`git commit -am "This is, so time saving"`

<hr />

### # We can create aliases as well, for commonly repeating commands
Telling `git` to add this new alias in your `--global` `config` file, and alias name will be `alias.alias_name_without_space` then in double quotes write that command

`git config --global alias.ac "commit -am"` then we can use as `git ac "that's so cool"`

- ### # Update alias
    Suppose If you mistakenly typed wrong command `git config --global alias.ac "commit -amm"` | notice `-amm`, not `-am` typo mistake
    
    So you can use same command to overwrite, correct / update that same 
    
    `git config --global alias.ac "commit -am"`

- ### # Delete alias
    Directly edit global git config file, so you can edit aliases, user details, and many more
    
    `git config --global --edit`

    * BTW, We have one more direct option
        
        `git config --global --unset alias.ac`
        
<hr />

### # Update more changes into previous (recent) commit or just edit / update commit message
When you wanna add some new files / changes into the recent commit or just wanna edit last commit message

-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-

- Editing only commit message

    I'm making typo here `git ac "that's go cool"`

- Now check correction

    `git commit --amend -m "that's so cool"`

-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-

- Now suppose, There's a case where you just wanna add, new files / changes in to your recent commit and don't wanna change the commit message, (update changes into your last commit)

    `git add .` or `git add file_name.extension`

    `git commit --amend --no-edit`

-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-

- Or if you wanna add changes and wanna edit the message as well, then you can go with

    <i>This will do, `git add .` && `git commit --amend -m "new message"`</i>
    
    `git commit --amend -am "new message"`
    
<hr />

### # Edit and add new files / changes into any old commit

- First, stash your changes that you want to add to that specific commit.
    - `git add .` or `git add <path_to_file/file_name> ...<file's_name>`
    - `git stash`

- Use `git rebase -i HEAD~<number of previous commits>` to edit the commit, Ex - `git rebase -i HEAD~3`.
- A file will open, Replace `pick` with `edit` for the commit you want to edit.
- Then save the file and exit the editor, hit `ESC` then type `:wq` and `enter`

- Now, pop the stash using `git stash pop`.

- Amend the commit using `git commit --amend`.
    - ##### You can use the `--no-edit` flag if you don't want to change the commit message.
    - ##### You can also use the `-m "new message"` flag to specify a new commit message.

- Finally, continue the rebase using `git rebase --continue`.
- <i>If you want to abort the process, use `git rebase --abort`.</i>

```
Note: Any commits that come after the one you are editing will have their commit IDs changed.
```

<hr />

### # Update any specfic old commit->message

- Use `git rebase -i HEAD~<number of previous commits>` to edit the commit message.
- Replace `pick` with `reword` or `r` for the commit you want to edit.
- Then save the file and exit the editor, hit `ESC` then type `:wq` and `enter`

```
# For example, to update the second last commit message, use `git rebase -i HEAD~3`.
# This will open Vim, where you can replace the `pick` with `reword` for the second last commit.
# Save the file and exit Vim.
# The commit message will now be updated.
```

```
Note: Any commits that come after the one you are editing will have their commit IDs changed.
```

<hr />

### # BTW, We have some options to see logs as well

- `git log` or `git log <branch_name>`
    - `git log --oneline`
    - `git log --graph --oneline --decorate`
    
<hr />

### # Revert back onto any old specific commit, If you sure to lose you commits, this will unstaged all those of your commits-changes | all commits right after your picked commit <i><sup>(commit-id)</sup></i>

- `git revert <commit-id>`
    
<hr />

### # Web-based VS code, for github repo's, weather it's your or someone else

If you are stuck at your grandma's house, having low-configuration or old computer that can't handle VS Code, and you don't have the internet speed to download it suppose, but now you can still edit files, commit your changes, and do much more using the github.dev web-based editor.

- To use, simply log in to your GitHub account and open any repository that you want to work on. Then, press the `.` (dot) key to open the editor simply.

<hr />

### # To unstaged changes, that you’ve recently commit (unstaged current commit changes)
 
`git reset HEAD^`

<hr />

### # Messed up your file? Restore it to the last commit with:

`git restore <file_name>`

This will restore the file to the state it was in at the last commit. If you want to restore the file to a specific commit, you can use the `-c` flag to specify the commit ID. For example, to restore the file to the commit with ID `1234567890`, you would use the following command:

`git restore -c 1234567890 <file_name>`

-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-

##### - Or Wanna align them with the remote repo, use `git fetch origin` and `git reset --hard origin/master`. This will discard all your local changes and align your branch with same as remote repo/branch.
- ##### Or If you still seeing some untracked, build or meaningless files, and you wanna remove them, use `git clean -df`.

<hr />

### # To create new branch

`git branch new_branch_name`

#### # To create a new branch and at the same time also wanna checkout into it

`git checkout -b <new-branch-name>`

#### # Or if you wanna delete the branch, first checkout to different branch and then use

`git branch -D <branch-name>`
 
<hr />

### # To go back to the last checked-out branch, use:

`git checkout -`

This will switch to the branch that was previously checked out. If you want to switch to a specific branch, you can specify the branch name after the `checkout` command. For example, to switch to the `master` branch, you would use the following command:

`git checkout master`

<hr />

### # Just to see the changes of specific commit in terminal

`git show <commit-id>`

<hr />

### # Stash, save changes in temp.

If you are working on a feature branch and need to switch to a bugfix branch, you can use `git stash` to save your changes temporarily. Once you are done with the bugfix, you can reapply your stash with `git stash pop`

#### - Save the current changes to a stash
- `git stash`

<i>Stash name and message are used to identify stash. Message can also provide more info about stash.</i>

#### - With the name
- `git stash save my_stash`

#### - With the message
- `git stash -m "This is a stash with spaces in the name"`

#### # Delete stash
##### - Delete a single stash
- `git stash drop` or you can specify index as well `git stash drop <index_no>`

##### - Delete all of the stashes in the current repository.
- `git stash clear`

#### # Get your changes back
##### - Get your changes from stash and remove it from the stash list
- `git stash pop` or you can specify index as well `git stash pop —index <index_no>`

##### - Get your changes but leave it in the stash list
- `git stash apply` or you can specify index as well `git stash apply <index_no>`

-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-

##### To see the list of saved stashes, `git stash list`

##### To see the changes of any specify stash, `git stash show` or you can specify index as well `git stash show <index_no>`

##### To create a new branch out of any specify stash directly, `git stash branch <branch_name> <index_no>`

<hr />

### # Squash multiple commits into a single commit

- Use `git rebase -i HEAD~<number of previous commits>` to squash the commits.
- Replace `pick` with `squash` for the commits you want to squash.
- Save the file and exit the editor.

```
# For example, to squash the last three commits, and merge into one, use `git rebase -i HEAD~3`.
# This will open Vim, where you can replace the `pick` with `squash` for the last two commits.
# Save the file and exit Vim.
# Again another Vim will open, here you can specify a single commit message and comment other with `#`
# Now Final save the file and exit Vim.
# The commits will now be squashed into a single commit.
```

<hr />

### # Reorder commits

- Use `git rebase -i HEAD~<number of previous commits>` to reorder the commits, as you hit enter, you'll gonna see Vim editor.
- In the editor, simply change the order of the commits.
- Save the file and exit the editor.

-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-

- #### For example, to reorder the last three commits, use `git rebase -i HEAD~3`.
- #### This will open Vim, where you can change the order of the last three commits.
- #### Line start's with `#` means comments, So you need to reorder by changing the order of the lines which starts from `pick`.
- #### Now just save the file and exit Vim.

#### <i>The commits will now be reordered now.</i>

<hr />

### # Delete your current commit and get HEAD back onto the previous one

- `git reset --hard HEAD~1` will delete the current commit and reset your working directory and index to the state of the previous commit. <b><i>This is the most destructive option, as it will lose all uncommitted changes.</i></b>

- `git reset --soft HEAD~1` will remove the current commit from history and unstaged your that commit files / changes, also keep your working directory and index in the state they were in before you committed. <b><i>This is a good option if you want to undo a commit but keep your changes.</b></i>

-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-

#### To unstage changes

`git reset` you can use to undo changes from staging area `git add <...>` area get back in modified state, <b><i>This is a good option if you want to undo changes that you have staged for commit.</b></i>

<hr />

### # Delete any old specific commit

- Use the `git rebase -i` command to edit the commit history.
    This will open an editor, where you will see a list of all the commits in your history.
    
- Change the `pick` action to `drop` for the commit you want to delete. Save the file and exit the editor.

- Run the `git rebase --continue` command to finalize the changes. This will delete the commit from your history.

<hr />

### # Git cherry-pick
Just Wanna pick and apply any specific commit of any branch and wanna merge that commit changes to the current branch as a new commit

`git cherry-pick <commit-id>`

<hr />

### # git bisect
To find a bug commit, if your app is not working and it was working fine a few commits back, you can traverse back your commits one by one (if you want) and check the good one (the commit in which your app was working). As you track back, as soon as you find your app starts working, you can mark that commit as good and copy the commit ID. You can then revert to that commit or copy that commit code, if you want.

##### `git bisect start`, To start bisecting / traversing

##### First To mark the current commit as bad, run `git bisect bad`, Now Git will check out to the next commit.

##### If you are confident that your app was working in some previous commit, you can use git log to find the commit ID and then run `git bisect good <commit-id>`. Git will then check out that commit and you can test your app to see if the bug is still present.

##### If you still haven't found a commit where your app was working, you can mark comments also as `bad` by running `git bisect bad`. Git will then automatically check out next commits for you

##### Ok, let's say you find a commit that works. You can mark it as good by running `git bisect good`. After you run this command, you will have the commit ID of the good commit.

##### And now to finish-up the bisecting, The `git bisect reset` command tells Git to stop bisect and return to your last commit.

-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-x-

<i><b>Now that you have the good commit ID, you can see the changes of that commit with the `git show <commit-id>` command. You can then see what mistake you made after that commit and copy the changes from the previous commit and add them to your current commit. Alternatively, you can revert back to the good commit by running the `git revert <commit-id>` command. This will open an editor where you can enter a commit message for the revert commit. If you want you can go with the default commit message as well, so after completing now press `esc` and type `:wq` and press enter.</b></i>

<hr />
