\# 1. Git credentials



\## Goals

To be fully prepared to work with Git.



\### 01 Setting up name and email address

If you've never used Git before, the first step is to set up your name and email address. Run the following commands to let Git know your name and email. If Git is already installed, you can skip this step.



Run:

git config --global user.name "Your Name"

git config --global user.email "your\_email@whatever.com"



\### 02 Default branch name

We will use main as the default branch name. To set this up, run the following command:



Run:

git config --global init.defaultBranch main



\### 03 Line endings treatment

Also, for users of Unix/Mac:



Run:

git config --global core.autocrlf input

git config --global core.safecrlf warn



For Windows users:



Run:

git config --global core.autocrlf true

git config --global core.safecrlf warn



