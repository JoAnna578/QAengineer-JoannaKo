17\. Amending commits

Goals

Learn how to modify an existing commit.

01Change the page and commit

Put an author comment on the page.



File: hello.html

<!-- Author: Alexander Shvets -->

<html>

&nbsp; <head>

&nbsp; </head>

&nbsp; <body>

&nbsp;   <h1>Hello, World!</h1>

&nbsp; </body>

</html>

Run

git add hello.html

git commit -m "Added copyright statement"

git log

Result

$ git add hello.html

$ git commit -m "Added copyright statement"

\[main e641c0e] Added copyright statement

&nbsp;1 file changed, 1 insertion(+)

$ git log

e641c0e 2023-11-28 | Added copyright statement (HEAD -> main) \[Alexander Shvets]

b7614c1 2023-11-28 | Added HTML header (tag: v1) \[Alexander Shvets]

46afaff 2023-11-28 | Added standard HTML page tags (tag: v1-beta) \[Alexander Shvets]

78433de 2023-11-28 | Added h1 tag \[Alexander Shvets]

5836970 2023-11-28 | Initial commit \[Alexander Shvets]

02Oops... email required

After making the commit you understand that every good commit should include the author's email. Edit the hello.html page to provide an email.



File: hello.html

<!-- Author: Alexander Shvets (alex@githowto.com) -->

<html>

&nbsp; <head>

&nbsp; </head>

&nbsp; <body>

&nbsp;   <h1>Hello, World!</h1>

&nbsp; </body>

</html>

03Change the previous commit

We do not want to create another commit for adding the email address. Let us change the previous commit and add an email address.



Run

git add hello.html

git commit --amend -m "Added copyright statement with email"

Result

$ git add hello.html

$ git commit --amend -m "Added copyright statement with email"

\[main 9288a33] Added copyright statement with email

&nbsp;Date: Tue Nov 28 05:51:38 2023 -0600

&nbsp;1 file changed, 1 insertion(+)

04View history

Run

git log

Result

$ git log

9288a33 2023-11-28 | Added copyright statement with email (HEAD -> main) \[Alexander Shvets]

b7614c1 2023-11-28 | Added HTML header (tag: v1) \[Alexander Shvets]

46afaff 2023-11-28 | Added standard HTML page tags (tag: v1-beta) \[Alexander Shvets]

78433de 2023-11-28 | Added h1 tag \[Alexander Shvets]

5836970 2023-11-28 | Initial commit \[Alexander Shvets]

The new "author/email" commit replaces the original "author" commit. The same effect can be achieved by resetting the last commit in the branch, and recommitting new changes.

