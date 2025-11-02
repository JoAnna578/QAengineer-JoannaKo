16\. Removing the oops tag

Goals

Removing the oops tag.

01Removal of the oops tag

The oops tag has performed its function. Let us remove that tag and permit the garbage collector to delete referenced commit.



Run

git tag -d oops

git log --all

Result

$ git tag -d oops

Deleted tag 'oops' (was 86364a1)

$ git log --all

b7614c1 2023-11-28 | Added HTML header (HEAD -> main, tag: v1) \[Alexander Shvets]

46afaff 2023-11-28 | Added standard HTML page tags (tag: v1-beta) \[Alexander Shvets]

78433de 2023-11-28 | Added h1 tag \[Alexander Shvets]

5836970 2023-11-28 | Initial commit \[Alexander Shvets]

The oops tag will no longer appear in the repository.

