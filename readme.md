#Git workshop 

In this workshop you will learn the basics of git and git feature branch workflow.

- Git bash and basic commands
- Setup new local repositary
- Working with remote repositary
- Merging and resolving conflicts
- Feature branch workflow intro
- SourceTree application intro

=============
## Before you start

1. Create github account at http://www.github.com
2. Ask your supervisor to add you as a collaborator to project
3. Download and install Git at https://git-scm.com/downloads
4. Download and install SourceTree application at
https://www.sourcetreeapp.com/download/

## Task 1 - local environment, init, add, commit
This task will introduce you to the basics of git local repositaries, how to create git repositary and work with your changes

1. create empty folder named **git_workshop**
2. inside create another folder **task_1**
3. `cd task_1` and initialize the git repositary to track any changes done to this folder
4. you can use `git status` command to check what has been done"
5. create **game.txt, alzak.txt and player.txt** files (in bash you can just `touch alzak.txt`)
6. run `git status`. You should see 3 untracked files
7. Add **game.txt** to the staging area
8. Use `git commit` to save your work on game.txt in the history (**`-m` parameter helps you to add message without opening any console editor**)
9. Use `--all` parameter to add alzak.txt and player.txt to your staging area. They share similar functionality therefore it's good to add them as a separate commit. It's logical!
10. Commit your files with any message you want.
11. Create branch **laser_gun** `git checkout -b <branch>`. Then checkout back to master
11. Make some changes to **player.txt** (e.g. add knife) and commit them. Hint: use `-a` param to add file and commit at once
12. Checkout to **laser_gun**, make changes to **player.txt** (add blaster to players arsenal), commit your changes.
13. Now switch to master and try to merge your **laser_gun** branch. (you can run `git status` to make sure you don't have any uncommited changes on master). `git merge <branch>`
14. You have CONFLICT. `git status` will tell you more detailed info as always. Open player.txt and try to resolve your conflict.
15. If you are confident about your resolution, commit it. You can `cat player.txt` to check the file. `git log` command will show nice history.  **Congratulations, you are now ready to kill that monster!**


## Task 2 - remote environment, source tree, feature branch workflow, stash
1. Clone project to a sourceTree application (github project url
provided by supervisor)
2. Click Git Flow to setup Feature Branch workflow
3. Click Git Flow again to create feature branch called
**[your_github_user_name]_move_system**
4. Create new file called **[your_github_user_name].txt and add your
Real name to it's content.
5. Commit your changes with message "[your_github_user_name] adding new feature"
6. Push your feature branch to origin
7. Go to your github account and create a **Pull request** to **DEVELOP** branch Wait for
code review / approval and merge by your supervisor
8. Click Fetch in menu to see what happened
9. Pull changes from origin
10. Create new feature branch
**[your_github_user_name]_boosting_player** and change **player.txt**
so it contains new line with "name: [your_github_user_name]". Commit
your changes. If line already exists, just change the name
11. Create sub-branch from feature branch and add
**[your_github_user_name]_2.txt** file
12. Commit changes and merge the sub-branch to feature branch. (HINT:
you need to be on feature branch)
13. Push your feature to origin, create pull request to develop branch.
14. Wait for supervisor, then **Fetch** from origin
15. Pull changes to develop (and master if needed)
16. Checkout to your feature branch and **Pull** from develop.


## Resources
How to become advanced in git: read https://www.atlassian.com/git/tutorials/

How to become pro in git: practice, practice, practice
