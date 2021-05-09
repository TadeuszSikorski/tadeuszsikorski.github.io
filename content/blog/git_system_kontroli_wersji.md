+++
title="Git - System kontroli wersji"
date=2021-05-06

[taxonomies]
tags = ["git"]
+++

W tym poście odpowiemy sobie na kilka pytań, które dotyczą systemu kontroli wersji **Git**. Odpowiedzi na te pytania pozwolą nam poznać bliżej czym jest *system kontroli wesji* i przede wszystkim czym jest **git**.

Jeżeli znane Ci już są poniższe informacje lub chcesz rozpocząć poznawanie gita od praktyczniejszej strony zapraszam Cię [**tutaj**](https://tadeuszsikorski.github.io/blog/pierwsze-repozytorium/).

## Co to jest *system kontroli wersji*?

Według [Wikipedii](https://pl.wikipedia.org/wiki/System_kontroli_wersji) to oprogramowanie służące do śledzenia zmian głównie w kodzie źródłowym oraz pomocy programistom w łączeniu zmian dokonanych w plikach przez wiele osób w różnym czasie.

Ze względu na architekturę można je podzielić na:

- lokalne, pozwalające na zapisanie danych jedynie na lokalnym komputerze
- scentralizowane, oparte na architekturze klient-serwer 
- rozproszone, oparte na architekturze P2P.

Do ostatniej z tych grup należy **git**.

## Czym jest git i dlaczego powstał?

Git to rozproszony system kontroli wersji, który stanowi on wolne oprogramowanie.

Stworzył go **Linus Torvalds**, twórca Linuksa jako narzędzie wspomagające rozwój *jądra Linux*. Powstał on po tym, jak *BitKeeper*, używany wtedy do rozwoju Linuksa, przestał być darmowy dla projektów o otwartym kodzie źródłowym. **Linus** początkowo szukał systemu, który spełni jego oczekiwania, jednak jego posukiwania nie przyniosły poądanego rezultatu. Zmuszony więc był do stworzenia własnego systemu kontroli wersji. 

## Cechy gita

- wsparcie dla rozgałęzionego procesu tworzenia oprogramowania
- wsparcie dla istniejących protokołów sieciowych
- efektywna praca z dużymi projektami
- praca nad projektem w trybie offline
- każda rewizja to obraz całego projektu

## Po co git jest nam potrzebny?

Najważniejsze pytanie. System kontroli wersji jakim jest **git** będzie nam potrzebny do zapisywania zmian kodu źródłowego naszych aplikacji, abyśmy potem mogli je śledzić. 

Aby móc łatwiej wersjonować tworzony kod, nie musząc ręcznie tworzyć jego migawek, co na dłuższą metę może powodować pogubienie się w tym, w której migawce była żądana funkcjonalność. Nie wspominając już o tworzeniu projektów zespołowych.

Pozwala nam rozgałęziać drzewo projektu, poprzez tworzenie nowych gałęzi dla nowych pobocznych funkcjonalności. 

Ułatwia pracę nad projektem zespołowi programistów. Każdy może pracować nad własną kopią projektu i zarządzać daną gałęzią.

Wieloplatformowość gita i możliwość stworzenia zdalnego repozytorium pozwala na pracę nad projektem zarówno w systemach GNU/Linux, MacOS jak i Windows.

## Podsumowanie

Jak łatwo jest zauważyć obecnie znajomość **gita** powinna być i jest podstawową umiejętnością większości programistów tworzących kod, a także architektów i team leaderów. Redukuje dużą ilość potencjalnych problemów na które można się narazić bez korzystania z niego.

## Źródła

1. [Oficjalna strona Gita](http://git-scm.com/)
2. [Oficjalna dokumentacja Gita](http://git-scm.com/doc)
3. [Pierwsze kroki - Wprowadzenie do kontroli wersji](http://git-scm.com/book/pl/v2/Pierwsze-kroki-Wprowadzenie-do-kontroli-wersji)
4. [Pierwsze kroki - Krótka historia Git](http://git-scm.com/book/pl/v2/Pierwsze-kroki-Kr%C3%B3tka-historia-Git)
5. [Pierwsze kroki - Podstawy Git](http://git-scm.com/book/pl/v2/Pierwsze-kroki-Podstawy-Git)
6. [System kontroli wersji - Wikipedia](https://pl.wikipedia.org/wiki/System_kontroli_wersji)
7. [Git - Wikipedia](https://pl.wikipedia.org/wiki/Git_(oprogramowanie))