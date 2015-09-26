**HEAD** 
    
    -is the tip of the current branch repository
    -the last state or checkout

###3 Trees

+ Repository
+ Staging
+ Working

**Undo changes in the WORKING directory**

    git diff                        - to show changes
    git checkout index.html

- this will replace whats in the *working* directory with the
current repository.

the proper syntax
    
    git checkout -- index.html

    -- means to stay in the current branch
    because checkout works in branch as well in files

    this will make my working directory the same as the repository


**Undo changes in STAGING directory**

    git add index.html

to unstage

    git reset HEAD index.html

this will move it back from staging to the working directory
this is used when you are putting a commit

**AMEND repository or commits**

Can only be done if your in the last commit

    git commit --amend -m "message"

Use it if your:

    -same file same repository
    -change commit message

**Reverting Commits**

Undo commits

    git revert HASH

Text editor will pop up
save
close

**Reset Soft**

Used to rewind the HEAD

    copy the log on a text editor so that it can be used as reference for later

    git reset --soft HASH
    git diff --staged               -show changes


**Viewing Changes**

View changes in Working directory

    git diff

    + old version       (added)
    - new version       (removed)

View changes in Staging directory

    git diff --staged
