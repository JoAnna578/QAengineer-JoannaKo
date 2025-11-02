\# Temat 1 – Git credentials



\## Cel

Skonfigurować Git: imię, email, domyślna gałąź main, końce linii.



\## Kroki wykonane

1\. Ustawiono imię i email:

&nbsp;  ```

&nbsp;  git config --global user.name "Joanna Ko"

&nbsp;  git config --global user.email "joannakoloczek1@gmail.com"

&nbsp;  ```

2\. Ustawiono domyślną gałąź na main:

&nbsp;  ```

&nbsp;  git config --global init.defaultBranch main

&nbsp;  ```

3\. Ustawiono końce linii:

&nbsp;  ```

&nbsp;  git config --global core.autocrlf true

&nbsp;  git config --global core.safecrlf warn

&nbsp;  ```

4\. Sprawdzono konfigurację:

&nbsp;  ```

&nbsp;  git config --list

&nbsp;  ```



\## Zrzuty ekranów

\- Zrzut terminala pokazuje wszystkie ustawienia Git

s

