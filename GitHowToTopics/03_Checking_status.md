\# 3. Checking the status of the repository



\## Goals

Learn how to check the repository’s status.



\### 01 Check the status of the repository

Use the git status command, to check the current state of the repository.



Run:

git status



Result:

$ git status

On branch main

nothing to commit, working tree clean



If you see On branch master instead of On branch main, rename the branch:



git branch -m master main



The command checks the status and reports that there’s nothing to commit.



