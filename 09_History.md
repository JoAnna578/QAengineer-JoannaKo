99\. History

Goals

Learn to view the project’s history.

Getting a list of changes made is a function of the git log command.



Run

git log

You will see:



Result

$ git log

commit b7614c1aea1ffbc46400fe1a163842d6ec620a43

Author: Alexander Shvets <alex@githowto.com>

Date:   Tue Nov 28 05:51:38 2023 -0600



&nbsp;   Added HTML header



commit 46afaff2232fc3d564c40f65cb82e7e94839a1bb

Author: Alexander Shvets <alex@githowto.com>

Date:   Tue Nov 28 05:51:38 2023 -0600



&nbsp;   Added standard HTML page tags



commit 78433de967102f2b59d0a8a60eb397b2663ed282

Author: Alexander Shvets <alex@githowto.com>

Date:   Tue Nov 28 05:51:38 2023 -0600



&nbsp;   Added h1 tag



commit 58369706affbc1c27fa03a65fc7a05847278045f

Author: Alexander Shvets <alex@githowto.com>

Date:   Tue Nov 28 05:51:38 2023 -0600



&nbsp;   Initial commit

Here is a list of all the four commits to the repository, which we were able to make so far.



01One line history

You fully control what the log shows. I like the single line format:



Run

git log --oneline

You will see:



Result

$ git log --oneline

b7614c1 Added HTML header

46afaff Added standard HTML page tags

78433de Added h1 tag

5836970 Initial commit

02Controlling the display of entries

Here are some other interesting options for viewing history:



git log --oneline --max-count=2

git log --oneline --since="5 minutes ago"

git log --oneline --until="5 minutes ago"

git log --oneline --author="Your Name"

git log --oneline --all

There is a huge variety of log viewing options, you can poke around the git-log manual page to see them all.



03Getting fancy

This is what I use to review the changes made within the last week. I will add --author=Alexander if I want to see only the changes made by me.



git log --all --pretty=format:"%h %cd %s (%an)" --since="7 days ago"

04The ultimate format of the log

Over time, I found the following log format to be the most suitable.



Run

git log --pretty=format:"%h %ad | %s%d \[%an]" --date=short

It looks like this:



Result

$ git log --pretty=format:"%h %ad | %s%d \[%an]" --date=short

b7614c1 2023-11-28 | Added HTML header (HEAD -> main) \[Alexander Shvets]

46afaff 2023-11-28 | Added standard HTML page tags \[Alexander Shvets]

78433de 2023-11-28 | Added h1 tag \[Alexander Shvets]

5836970 2023-11-28 | Initial commit \[Alexander Shvets]

Let's look at it in detail:



--pretty="..." defines the output format.

%h is the abbreviated hash of the commit.

%ad is the commit date.

| is just a visual separator.

%s is the comment.

%d commit decorations (e.g. branch heads or tags).

%an is the name of the author.

--date=short keeps the date format short and nice.

So, every time you want to see a log, you'll have to do a lot of typing. Fortunately, there are several Git config options to adjust the default log output format:



Run

git config --global format.pretty '%h %ad | %s%d \[%an]'

git config --global log.date short

05Other tools

Both gitx (for Mac) and gitk (for any platform) can help to explore log history.



. History

Goals

Learn to view the project’s history.

Getting a list of changes made is a function of the git log command.



Run

git log

You will see:



Result

$ git log

commit b7614c1aea1ffbc46400fe1a163842d6ec620a43

Author: Alexander Shvets <alex@githowto.com>

Date:   Tue Nov 28 05:51:38 2023 -0600



&nbsp;   Added HTML header



commit 46afaff2232fc3d564c40f65cb82e7e94839a1bb

Author: Alexander Shvets <alex@githowto.com>

Date:   Tue Nov 28 05:51:38 2023 -0600



&nbsp;   Added standard HTML page tags



commit 78433de967102f2b59d0a8a60eb397b2663ed282

Author: Alexander Shvets <alex@githowto.com>

Date:   Tue Nov 28 05:51:38 2023 -0600



&nbsp;   Added h1 tag



commit 58369706affbc1c27fa03a65fc7a05847278045f

Author: Alexander Shvets <alex@githowto.com>

Date:   Tue Nov 28 05:51:38 2023 -0600



&nbsp;   Initial commit

Here is a list of all the four commits to the repository, which we were able to make so far.



01One line history

You fully control what the log shows. I like the single line format:



Run

git log --oneline

You will see:



Result

$ git log --oneline

b7614c1 Added HTML header

46afaff Added standard HTML page tags

78433de Added h1 tag

5836970 Initial commit

02Controlling the display of entries

Here are some other interesting options for viewing history:



git log --oneline --max-count=2

git log --oneline --since="5 minutes ago"

git log --oneline --until="5 minutes ago"

git log --oneline --author="Your Name"

git log --oneline --all

There is a huge variety of log viewing options, you can poke around the git-log manual page to see them all.



03Getting fancy

This is what I use to review the changes made within the last week. I will add --author=Alexander if I want to see only the changes made by me.



git log --all --pretty=format:"%h %cd %s (%an)" --since="7 days ago"

04The ultimate format of the log

Over time, I found the following log format to be the most suitable.



Run

git log --pretty=format:"%h %ad | %s%d \[%an]" --date=short

It looks like this:



Result

$ git log --pretty=format:"%h %ad | %s%d \[%an]" --date=short

b7614c1 2023-11-28 | Added HTML header (HEAD -> main) \[Alexander Shvets]

46afaff 2023-11-28 | Added standard HTML page tags \[Alexander Shvets]

78433de 2023-11-28 | Added h1 tag \[Alexander Shvets]

5836970 2023-11-28 | Initial commit \[Alexander Shvets]

Let's look at it in detail:



--pretty="..." defines the output format.

%h is the abbreviated hash of the commit.

%ad is the commit date.

| is just a visual separator.

%s is the comment.

%d commit decorations (e.g. branch heads or tags).

%an is the name of the author.

--date=short keeps the date format short and nice.

So, every time you want to see a log, you'll have to do a lot of typing. Fortunately, there are several Git config options to adjust the default log output format:



Run

git config --global format.pretty '%h %ad | %s%d \[%an]'

git config --global log.date short

05Other tools

Both gitx (for Mac) and gitk (for any platform) can help to explore log history.





