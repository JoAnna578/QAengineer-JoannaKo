10\. Getting older versions

Goals

Learn how to check out any previous version into the working directory.

Git make time traveling possible, at least for your project. The checkout command will update your working directory to any previous commit.



01Getting hashes of the previous commit

Run

git log

Result

$ git log

b7614c1 2023-11-28 | Added HTML header (HEAD -> main) \[Alexander Shvets]

46afaff 2023-11-28 | Added standard HTML page tags \[Alexander Shvets]

78433de 2023-11-28 | Added h1 tag \[Alexander Shvets]

5836970 2023-11-28 | Initial commit \[Alexander Shvets]

Check the log data and find the hash of the initial commit. You will find it in the last line of the output. Use the hash (its first 7 characters are enough) in the command below. After that check the contents of the hello.html file.



Run

git checkout <hash>

cat hello.html

Many Git commands accept commit hashes as arguments. Commit hashes will vary from repository to repository, so when you see a command with the <hash> mark, it means that you need to substitute it with the actual hash from your repository.



You will see:



Result

$ git checkout 5836970

Note: switching to '5836970'.



You are in 'detached HEAD' state. You can look around, make experimental

changes and commit them, and you can discard any commits you make in this

state without impacting any branches by switching back to a branch.



If you want to create a new branch to retain commits you create, you may

do so (now or later) by using -c with the switch command. Example:



&nbsp; git switch -c <new-branch-name>



Or undo this operation with:



&nbsp; git switch -



Turn off this advice by setting config variable advice.detachedHead to false



HEAD is now at 5836970 Initial commit

$ cat hello.html

Hello, World!

Note that the current content of the hello.html file is the content that we started with in the very beginning.



02Returning to the latest version in the main branch

To return to the latest version of our code, we need to switch to the default main branch. We can use the switch command to switch between branches.



The checkout command has been a swiss army knife in the world of Git for a long time. It has tons of various options that let you run entirely different things: switch branches, reset code, etc. At some point, the Git team decided to split the command into several commands. The switch command is one of them—its sole purpose is to switch between branches. The checkout command is still available, but it is no longer recommended to use it for switching branches.



Run

git switch main

cat hello.html

You will see:



Result

$ git switch main

Previous HEAD position was 5836970 Initial commit

Switched to branch 'main'

$ cat hello.html

<html>

&nbsp; <head>

&nbsp; </head>

&nbsp; <body>

&nbsp;   <h1>Hello, World!</h1>

&nbsp; </body>

</html>

main is the name of the default branch. By switching to a branch, you go to its latest version.

