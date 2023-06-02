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
