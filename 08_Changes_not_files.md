8\. Changes, not files

Goals

Understanding that Git works with the changes, not the files.

Most version control systems work with files. You add the file to source control and the system tracks changes from that moment on.



Git concentrates on the changes to a file, not the file itself. A git add file command does not tell Git to add the file to the repository, but to note the current state of the file for it to be committed later.



We will try to investigate the difference in this lesson.



01First Change: Adding default page tags

Change the "Hello, World" page so that it contained default tags <html> and <body>.



File: hello.html

<html>

&nbsp; <body>

&nbsp;   <h1>Hello, World!</h1>

&nbsp; </body>

</html>

02Add this change

Now add this change to the Git staging.



Run

git add hello.html

03Second change: Add the HTML headers

Now add the HTML headers (<head> section) to the "Hello, World" page.



File: hello.html

<html>

&nbsp; <head>

&nbsp; </head>

&nbsp; <body>

&nbsp;   <h1>Hello, World!</h1>

&nbsp; </body>

</html>

04Check the current status

Run

git status

You will see:



Result

$ git status

On branch main

Changes to be committed:

&nbsp; (use "git restore --staged <file>..." to unstage)

&nbsp;	modified:   hello.html



Changes not staged for commit:

&nbsp; (use "git add <file>..." to update what will be committed)

&nbsp; (use "git restore <file>..." to discard changes in working directory)

&nbsp;	modified:   hello.html



Please note that hello.html is listed in the status twice. The first change (the addition of default tags) is staged and ready for a commit. The second change (adding HTML headers) is unstaged. If you were making a commit right now, headers would not have been saved to the repository.



Let's check.



05Commit

Commit the staged changes (default values), then check the status one more time.



Run

git commit -m "Added standard HTML page tags"

git status

You will see:



Result

$ git commit -m "Added standard HTML page tags"

\[main 46afaff] Added standard HTML page tags

&nbsp;1 file changed, 5 insertions(+), 1 deletion(-)

$ git status

On branch main

Changes not staged for commit:

&nbsp; (use "git add <file>..." to update what will be committed)

&nbsp; (use "git restore <file>..." to discard changes in working directory)

&nbsp;	modified:   hello.html



no changes added to commit (use "git add" and/or "git commit -a")

The status command suggests that hello.html still has unrecorded changes, but the staging area is already clear.



06Adding the second change

Add the second change to the staging area, after that run the git status command.



Run

git add .

git status

We have used the current directory (.) as the argument for the add command. This is the shortest and most convenient way to add all changes in the current directory. But since Git adds everything to the index, it's a good idea to check the state of the repository before running add, just to make sure you haven't added a file you shouldn't have.



I just wanted to show you the trick with add ., from now on we will add all files explicitly.



You will see:



Result

$ git add .

$ git status

On branch main

Changes to be committed:

&nbsp; (use "git restore --staged <file>..." to unstage)

&nbsp;	modified:   hello.html



The second change has been staged and is ready for a commit.



07Commit the second change

Run

git commit -m "Added HTML header"

Result

$ git commit -m "Added HTML header"

\[main b7614c1] Added HTML header

&nbsp;1 file changed, 2 insertions(+)



