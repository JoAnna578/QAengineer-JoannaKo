11\. Tagging versions

Goals

Learn how to tag commits for future references.

For most people working with hashes directly is annoying at best. Wouldn't it be great if you could label specific commits with human-readable names? This way you could clearly see important milestones in the project history. Moreover, you could easily check out to a specific version of the project by its name. For this reason, Git has a feature called "tags".



Let's call the current version of the hello.html page as version 1: v1.



01Creating a tag for the first version

Run

git tag v1

git log

Result

$ git tag v1

$ git log

b7614c1 2023-11-28 | Added HTML header (HEAD -> main, tag: v1) \[Alexander Shvets]

46afaff 2023-11-28 | Added standard HTML page tags \[Alexander Shvets]

78433de 2023-11-28 | Added h1 tag \[Alexander Shvets]

5836970 2023-11-28 | Initial commit \[Alexander Shvets]

Now, the current version of the page is referred to as v1.



02Tags for previous versions

Let's tag the version prior to the current version with the name v1-beta. First of all we will check out the previous version. Instead of looking up the hash of the commit, we are going to use the ^ notation, specifically v1^, indicating the commit previous to v1.



If the v1^ notation gives you any trouble, you can also try v1~1, which will reference the same version. The V~N notation means "the N-th version prior to V", or in case of v1~1, first version prior to v1.



Run

git checkout v1^

cat hello.html

Result

$ git checkout v1^

Note: switching to 'v1^'.



You are in 'detached HEAD' state. You can look around, make experimental

changes and commit them, and you can discard any commits you make in this

state without impacting any branches by switching back to a branch.



If you want to create a new branch to retain commits you create, you may

do so (now or later) by using -c with the switch command. Example:



&nbsp; git switch -c <new-branch-name>



Or undo this operation with:



&nbsp; git switch -



Turn off this advice by setting config variable advice.detachedHead to false



HEAD is now at 46afaff Added standard HTML page tags

$ cat hello.html

<html>

&nbsp; <body>

&nbsp;   <h1>Hello, World!</h1>

&nbsp; </body>

</html>

This is the version with <html> and <body> tags, but without <head>. Let's make it’s the v1-beta version.



Run

git tag v1-beta

git log

Result

$ git tag v1-beta

$ git log

46afaff 2023-11-28 | Added standard HTML page tags (HEAD, tag: v1-beta) \[Alexander Shvets]

78433de 2023-11-28 | Added h1 tag \[Alexander Shvets]

5836970 2023-11-28 | Initial commit \[Alexander Shvets]

03Check out by the tag name

Now try to check out between the two tagged versions.



Run

git checkout v1

git checkout v1-beta

Result

$ git checkout v1

Previous HEAD position was 46afaff Added standard HTML page tags

HEAD is now at b7614c1 Added HTML header

$ git checkout v1-beta

Previous HEAD position was b7614c1 Added HTML header

HEAD is now at 46afaff Added standard HTML page tags

04Viewing tags with the tag command

You can see the available tags using the git tag command.



Run

git tag

Result

$ git tag

v1

v1-beta

05Viewing tags in logs

You can also check for tags in the log.



Run

git log main --all

Result

$ git log main --all

b7614c1 2023-11-28 | Added HTML header (tag: v1, main) \[Alexander Shvets]

46afaff 2023-11-28 | Added standard HTML page tags (HEAD, tag: v1-beta) \[Alexander Shvets]

78433de 2023-11-28 | Added h1 tag \[Alexander Shvets]

5836970 2023-11-28 | Initial commit \[Alexander Shvets]

You can see tags (v1 and v1-beta) listed in the log together with the name of the branch (main). The HEAD marker shows the commit you checked out (currently v1-beta).

