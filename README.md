## Get good at git
#### <i>CreatedBy - Linus torvalds in 2005</i>

<hr />

* First download git https://git-scm.com/downloads if you don’t have already

<hr />

#### To get | global’s

`git config --global --list`

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
 
    - `touch index.html`
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

### # BTW, We have some options to see logs as well

- `git log`
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
