\# 6. Staging and committing



\## Goals

Learn to separate staging from committing in Git to create logical commits.



\## 01 Conceptual example

Suppose you have edited three files: `a.html`, `b.html`, and `c.html`. You want changes in `a.html` and `b.html` to go into one commit, and changes in `c.html` into a separate commit.



\### Commands



```bash

git add a.html

git add b.html

git commit -m "Changes for a and b"



git add c.html

git commit -m "Unrelated change to c"



