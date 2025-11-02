7\. Committing the changes

Goals

Learn to commit to the repository.

01Committing changes

Well, enough about staging. Let's commit the staged changes to the repository.



When you previously used git commit for committing the first hello.html version to the repository, you included the -m flag that gives a comment on the command line. The commit command allows interactively editing comments for the commit. And now, let's see how it works.



If you omit the -m flag from the command line, Git will pop you into the editor of your choice from the list (in order of priority):



GIT\_EDITOR environment variable;

core.editor configuration setting;

VISUAL environment variable;

EDITOR environment variable.

I have the EDITOR variable set to vim. If you prefer GUI editor, it's now possible to use VS Code as a Git editor.



Let us commit now and check the status.



Run

git commit

You will see the following in your editor:



Result

|

\# Please enter the commit message for your changes. Lines starting

\# with '#' will be ignored, and an empty message aborts the commit.

\#

\# On branch main

\# Changes to be committed:

\#       modified:   hello.html

\#

On the first line, enter the comment: Added h1 tag. Save the file and exit the editor (to do it in default editor, press ESC and then type :wq and hit Enter). You should see:



Result

$ git commit

\[main 78433de] Added h1 tag

&nbsp;1 file changed, 1 insertion(+), 1 deletion(-)

"Waiting for Emacs…" is obtained from the emacsclient program sending the file to a running emacs program and waiting for it to be closed. The rest of the data is the standard commit messages.



02Checking the status

At the end let us check the status.



Run

git status

You will see:



Result

$ git status

On branch main

nothing to commit, working tree clean

The working directory is clean, you can continue working.

