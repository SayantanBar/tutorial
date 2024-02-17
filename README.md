1 `git init` -> Power your folder to be managed by git, and initialized to a empty repository. It also create a .git folder that has all relevent logic to
manage versions of your project

2 `Working area` -> There can be a bunch of files that currently are not handle by git.It means that the changes are done or to be done in those file
are not managed by git yet.A file which is in working area is not consider to be in the staging area. when we do `git status` and we see bunch of
`untrack files` then these are actually to be in working area.

3 `Staging Area` -> what all files are going to be part of the next version that we will create. the staging area is the place git knows what changes
will be done from last version to next version

4 `Repository Area` -> This area actually contains the details of all your previous register version.and the files in this area, git already
managed them, and knows there version history.

5. `git add` <filename> -> moves file from working area to staging area.

6. `git rm --cached <filename>` -> moves files from staging area to working area.

7. `commit` -> Commit is a particular version of the project. It captures a snapshot of the project's stage changes and create a version out of it.

8. `git commit` -> Register staging changes to a commit

9. `git log` -> List down all the commit of the repository.

10. `git restore <filename>` -> It removes all file changes from staging area to be commited. this can be useful if we did some dirty piece of
    code and now no more want it. Instead of deleting every line by line we can restore it or we can say restore last clean version of the file.

11. `git restore --staged <filename>` -> It removes file from changes from staging area to working area.
    this only works if changes are in your staging area.

12. Diff between git rm vs git restore
    ans : if we want to move the whole file back to the untrack state, then we do git rm. otherwise if we just want to changes to be moved in working
    area or staging area then we git restore.

13. `git diff commit1 commit2` -> give the diff between all files changes between two commits

14. If you want to avoid opening a text editor like vim/nano to commit massages you can use following command.

15.`git remote` -> List down all the remote connection names.

16.remote connection -> It helps you to link two git repositories for uploading and downloading changes from each otherwise.

17.`git remote add <name of the remote> <link of the remote>` : this command helps us to add a new link to the remote repo and
give a name to it.

18.`git remote rm <name of the remote>` this command delete a remote connection.

19.`git remote rename <oldname> <newname>`: this command renames the remote connections.
NOTE: The name of the remote connection is always used to establish communication between the repo.

20.`git pull <remote name> <branch name>` : downloads latest changes from the branch of the mention remote in your local repo.

### Recommended practice to do

- make changes
- git add <file>
- git commit
- git pull
- git push
