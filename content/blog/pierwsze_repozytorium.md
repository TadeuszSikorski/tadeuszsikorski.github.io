+++
title="Pierwsze repozytorium  - wstęp do systemu kontroli Git"
date=2021-05-06

[taxonomies]
tags = ["git"]

+++

Aby rozpocząć pracę z *systemem kontroli wersji* jakim jest **git** od tej praktyczniejszej strony trzeba go najpierw zainstalować. 

## Instalacja git

W zależności od posiadanego systemu operacyjnego można to wykonać za pośrednictwem strony na której znajdują się niezbędne instrukcje służące pomocą jak to zrobić. Oto podana strona:

https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

lub w wersji polskiej:

https://git-scm.com/book/pl/v2/Pierwsze-kroki-Instalacja-Git

## Pierwsze repozytorium

Kiedy już dokonamy instalacji kolejnym krokiem będzie stworzenie katalogu o nazwie first-repo. Na przykład z poziomu linii poleceń:
```bash
mkdir first-repo && cd first-repo
```

Tworzymy *puste* **lokalne repozytorium Git** za pomocą polecenia:
```bash
git init
```

Następnie aby zobaczyć informacje na temat początkowego statusu naszego pierszego repo wystarczy:
```bash
git status
```

Wyświetlą nam się poniższe informacje:
```bash
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```

Oznacza to, że jesteśmy w głównej gałęzi i nie mamy jeszcze wykonanych żadnych zatwierdzeń (*commits*). A także nie mamy żadnych plików, które możemy zatwierdzić. Mamy za to małą podpowiedź w nawiasach, która informuje nas o tym, że gdy dodamy lub skopiujemy pliki do naszego katalogu możemy je dodać do śledzenia za pomocą:
```bash
git add 
```

## Dodawanie i zatwierdzenie pierwszego pliku do repozytorium

Tak więc tworzymy przykładowy plik o nazwie *file.txt*. Następnie znów wykonujemy polecenie **git status**. Naszym oczom powinny ukazać się następujące informacje:
```bash
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        file.txt

nothing added to commit but untracked files present (use "git add" to track)
```

Mamy plik, który możemy dodać do zatwierdzenia i utworzyć nasze pierwsze zatwiedzenie następującymi poleceniami:
```bash
git add file.txt && git commit -m "Initial commit"
```

Po wykonaniu powyższych komend dostaniemy podobną do tej informację:
```bash
[master (root-commit) 0915b29] Initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 file.txt
```

Zatwierdzenie z jednym plikiem zostało poprawnie dodane. A po ponownym wyświetleniu statusu dostaniemy taką oto informację:
```bash
On branch master
nothing to commit, working tree clean
```

Oznacza to, że w gałęzi w której aktualnie jesteśmy, w tym przypadku gałęzi głównej nie ma nic do zatwierdzenia, bo pliki znajdujące się w naszym katalogu zostały już zatwierdzone i drzewo jest czyste.

Gdy zakładamy puste repozytorium git w katalogu w którym mamy już pliki lub katalogi i nie chcemy je dodawać pojedyńczo tylko od razu wszystko za jednym razem można to zrobić za pomocą komendy:
```bash
git add .
```

## Podsumowanie
Tyle tytułem praktycznego wstępu. Nauczyłeś się właśnie tworzyć pierwsze **lokalne repozytorium Git** i dodawać do niego pliki i katalogi, a także je zatwierdzać.  

Część teoretyczna zawierająca odpowiedzi na pytania:
- co to jest system kontroli wersji?
- czym jest git i dlaczego powstał?
- po co jest nam potrzebny?

Zawarta jest w tym [poście](https://tadeuszsikorski.github.io/blog/git-system-kontroli-wersji/).

W następnej części opowiem o klonowaniu repozytorium, preglądaniu historii zatwierdzeń, a także tworzeniu zdalnego repozytorium i wysyłaniem do niego zatwierdzonych plików i katalogów z naszego lokalnego repozytorium. 

Dla tych który chcą uzupełnić i poszerzyć swoją wiedzę odsyłam do źródeł.

## Źródła

1. [Getting Started - Installing Git](http://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
2. [Git Basics - Getting a Git Repository](http://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)
3. [Git Basics - Recording Changes to the Repository](http://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository)