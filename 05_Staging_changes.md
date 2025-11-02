\# Temat 5 – Staging the changes



\## Cel

Nauczyć się stage’ować zmiany w Git przed commitem.



\## Kroki wykonane



\### 1. Dodanie zmian do stage

Zmieniliśmy plik `hello.html` w poprzednim zadaniu. Teraz należy poinformować Git, że zmiana jest gotowa do commita:



```bash

git add hello.html

git status

```



\### 2. Wynik

Po wykonaniu poleceń zobaczysz:



```

$ git add hello.html

$ git status

On branch GitHowTo

Changes to be committed:

&nbsp; (use "git restore --staged <file>..." to unstage)

&nbsp;	modified:   hello.html

```



Zmiany w pliku `hello.html` zostały dodane do stage. Oznacza to, że Git zna zmiany, ale nie są one jeszcze zapisane w repozytorium. Następny commit obejmie te zmiany.



Jeśli zdecydujesz, że nie chcesz zatwierdzać zmian, komenda `git status` przypomni Ci, że możesz użyć:



```bash

git restore --staged hello.html

```



aby usunąć plik z stage.



