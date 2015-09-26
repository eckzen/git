# git
My git commands

#Alias i added for git

    alias gs='git status '
    alias ga='git add '
    alias gb='git branch '
    alias gc='git commit -m'
    alias gd='git diff'
    alias go='git checkout '
    alias gk='gitk --all&'
    alias gx='gitx --all'
    alias gl='git log'
    alias gp='git push origin master'

**Levels in Git**

+ Repository        - git commit -m 'message'
+ Staging           - git add .
+ Working           - save the changes from the file
+ Stash

Start from local

    git init
    git add . 
    git commit -m 'comment about the file'
    git clone <git URL>
    git push origin/master

To unstage from Staging back to Working directory

    git rm --cached <file>

Same file in working and staging. 
The file in the staging is deleted
The file in the working remains untouched

Unstage the file

    git reset <file>

Remove file in the Working
Deletes the file 
    
    git checkout <file>

Undo commit
From repository to working

    git log                     - To show commit list
    git reset <commit>
    git reset --hard <commit>   - Erases the history

View difference betweeen working and staged changes in a file

    git diff <file>

Delete the file

    git rm -f <file>

**Branch**

Create a new branch

    git branch <new branch name>

Move from branch

    git checkout <branch name>
    git checkout master         - go to master branch

Branch list

    git branch
    git branch -a               - view all branch

Make a new branch and open that branch

    git checkout -b <branch name>

Branch
    + master
    + new_branch

Merge new branch to master

    git checkout master
    git merge new_branch

Rename a branch

    git branch -m <old name> <new name>

Show diffrence between branches

    git diff master new_branch

Delete a branch 

    git branch -D new_branch

**Cloning a Repository**

   + git clone URL
   + cd <repository>
   + npm install
   + gulp

**Remotes**

Remote server
<<<<<<< HEAD

^      |

^ push |fetch

^      |                       __

^ My computer--->origin/master   |

^                                |- merge origin / master

=======
^      |
^ push |fetch
^      |                       __
^ My computer--->origin/master   |
^                                |- merge origin / master
>>>>>>> 1c4b0bb5936ffb615d8353e68b32e386dcb7a7d0
Master                         __|

*merge origin/master*

    used to sync origin/master to master

    git remote
    git remote add <alias> <URL>    alias = origin
    git remote -v
        .git/config file
    git remote rm origin            delete

From My computer to Remote

    git push -u origin master

Pushing a branch to remote
    
    git branch -r           - shows remote branch
    git branch -a           - shows all branch

Pulling the remote to local

    git clone URL

