## Get good at git
#### <i>CreatedBy - Linus torvalds in 2005</i>

<hr />

* First download git https://git-scm.com/downloads if you don’t have already

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

### # Update more changes into previous commit or just edit / update commit message
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
