+++
title="Git - Zdalne repozytorium"
date=2021-05-08

[taxonomies]
tags = ["git"]
+++

Na samym początku musimy odpowiedzieć sobie na pytanie: Po co nam **zdalne repozytorium**? 

Służy ono do współdzielenia pracy między osobami pracującymi nad jednym projektem, ale może także być wykorzystane do tworzenia kopii zapasowej lokalnego repozytorium.

## Dodanie zdalnego repozytorium

Aby podpiąć zdalne repozytorium do naszego zdalnego repoytorium trzeba w konsoli wpisać następującą komendę:

```bash
git remote add origin https://github.com/TadeuszSikorski/fresh-evergreen.git
```

Mamy tutaj **git remote add** odpowiadający za dodanie zdalnego repozytorium do naszego lokalnego repo. 

Słowo *origin* jest aliasem, czyli krótką nazwą, która identyfikuje nasze zdalne repo. Może to być dowolna inna nazwa, jednak w przykładach najczęściej pojawia się właśnie słowo *origin*.  

Na samym końcu musimy podać adres url do zdalnego repozytorium.

Gdy wykonamy powyższą komendę nic nie zostanie zwrócone. Jak więc sprawdzić czy wszystko przebiegło poprawnie? Służy do tego polecenie:

```bash
git remote -v
```

Po jego wykonaniu otrzymamy taką oto odpowiedź:

```bash
origin  https://github.com/TadeuszSikorski/fresh-evergreen.git (fetch)
origin  https://github.com/TadeuszSikorski/fresh-evergreen.git (push)
```

Podany jest alias, url i w nawiasach informacja od czego jest poszczególne repozytorium. Tutaj mamy jedno, więc służy zarówno do wysyłania do niego plików i daje możliwość ich póżniejszego pobrania.

## Jak utworzyć zdalne repozytorium?

W większości kursów **git** uwagę poświęca się tylko na dodaniu zdalnego repozytorium do lokalnego repo. A pierwszym pytaniem powinno być właśnie jak takie zdalne repozytorium można utworzyć, aby potem można je było podpiąć do lokalnego repozytorium. 

Zdalne repozytorium można utworzyć np. w serwisach takich jak **Github**, **GitLab**, **Bitbucket**. 

Aby to zrobić w serwisie **Github** najpierw trzeba utworzyć sobie na nim konto lub jeżeli już takowe posiadamy wygodnym jest zainstalowanie sobie narzędzia o nazwie [**GitHub CLI**](https://github.com/cli/cli).

Gdy już to zrobimy musimy je skonfigurować. Pomoże nam w tym [oficjalna dokumentacja](https://cli.github.com/manual/).

Gdy już się z tym uwiniemy możemy w wierszu poleceń otworzyć nasze lokalne repozytorium i wykonać następującą komendę:
```bash
gh repo create fresh-evergreen
```

To spowoduje wyświetlenie wyboru ustawień dla naszego zdalnego repozytorium takich jak widoczność, które odpowiada za to czy nasze repo ma być:
- dostępne publicznie, 
- prywatne, widoczne tylko dla naszego
- wewnętrzne, prywatne repozytorium współdzielone dla organizacji
  
```bash
? Visibility  [Use arrows to move, type to filter]
> Public
  Private
  Internal
```

Następnie pojawia się pytanie czy wyrażamy zgodę na to by podpiąć tworzone zdalne repozytorium do naszego lokalnego repozytorium czyli krok, który opisałem powyżej. Redukuje to nam ręczne podpinanie zdalnego repozytorium. W tym więc przypadku zaznaczamy **Y**.

```bash
 This will add an "origin" git remote to your local repository. Continue? (Y/n)
```

Na końcu mamy taki oto komunikat, który informuje nas, że wszystko przebiegło pomyślnie: 

```bash
? Visibility Public
? This will add an "origin" git remote to your local repository. Continue? Yes
✓ Created repository TadeuszSikorski/fresh-evergreen on GitHub
✓ Added remote https://github.com/TadeuszSikorski/fresh-evergreen.git
```

Moim zdaniem łatwa konfiguracja pozwala na załatwienie od razu dwóch rzeczy za jednym razem.

## Wysyłanie zatwierdzonych plików do zdalnego repozytorium

Gdy mamy już podpięte zdalne repozytorium można do niego rozpocząć wysyłanie plików. Uprzednio muszą ode być zatwierdzone, czyli zakomitowane. O czym było w poprzednim [poście](https://tadeuszsikorski.github.io/blog/pierwsze-repozytorium/). Aby to zrobić wystarczy proste polecenie:
```bash
git push origin master
```
Co oznacza wysłanie zatwierdzonych plików (zmian w tych plikach) z głównej gałęzi (**master**) do zdalnego repozytorium oznaczonego odpowiednim aliasem (**origin**). A

Po wykonaniu tej komendy otrzymamy taką oto odpowiedź: 
```bash
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 290 bytes | 15.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/TadeuszSikorski/fresh-evergreen.git
 * [new branch]      master -> master
```
Obiekty (pliki) zostały dodane i w naszym pustym zdalnym repozytorium utworzona została nowa gałęź (**master**), czyli gałęź główna z naszego lokalnego repozytorium.

## Podsumowanie

W tej części nauczyłeś się jak podpinać i tworzyć zdalne repozytorium dla lokalnego repozytorium oraz jak w prosty sposób wysyłać zatwierdzone pliki (zmiany) do zdalnego repozytorium.

W następnej części opowiem o klonowaniu repozytorium, przeglądaniu historii zatwierdzeń.

## Źródła

1. [itcraftsman.pl - KONTROLA WERSJI Z GIT CZ. 4 – ZDALNE REPOZYTORIA](http://itcraftsman.pl/kontrola-wersji-z-git-cz-4-zdalne-repozytoria/)
2. [Github CLI](https://cli.github.com/manual/)