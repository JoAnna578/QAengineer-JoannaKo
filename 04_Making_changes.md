temat: "4 – Making changes"

cel: "Nauczyć się monitorować stan katalogu roboczego i wprowadzać zmiany."

kroki:

&nbsp; - krok: "Zmiana pliku hello.html"

&nbsp;   opis: "Dodano tagi HTML do strony powitalnej"

&nbsp;   plik: "hello.html"

&nbsp;   zawartosc: "<h1>Hello, World!</h1>"

&nbsp; - krok: "Sprawdzenie statusu repozytorium"

&nbsp;   komenda: "git status"

&nbsp;   wynik: |

&nbsp;     On branch GitHowTo

&nbsp;     Changes not staged for commit:

&nbsp;       (use "git add <file>..." to update what will be committed)

&nbsp;       (use "git restore <file>..." to discard changes in working directory)

&nbsp;       modified:   hello.html



&nbsp;     no changes added to commit (use "git add" and/or "git commit -a")

&nbsp;   opis\_wyniku: |

&nbsp;     Git wykrywa zmiany w pliku hello.html, ale nie zostały one jeszcze dodane do repozytorium.

&nbsp;     Status podpowiada, co zrobić dalej:

&nbsp;       - Aby dodać zmiany: git add hello.html

&nbsp;       - Aby cofnąć zmiany: git restore hello.html

zrzuty\_ekranow:

&nbsp; - opis: "Pokazują zmiany w pliku hello.html oraz wynik git status"



