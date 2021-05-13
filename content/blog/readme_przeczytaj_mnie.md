+++
title="README.md - Przeczytaj mnie"
date=2021-05-13

[taxonomies]
tags = ["git", "markdown"]
+++

Dzisiejszy wpis rozpoczniemy sobie od odpowiedzi na kilka pytań.

## Co to jest **README.md**?
**README** to plik tekstowy, który wprowadza i wyjaśnia **projekt**. Zawiera informacje, które są powszechnie **wymagane**, aby zrozumieć, o czym jest projekt. Jest pierwszym plikiem, który **powinno się** czytać otwierając **nowy projekt**.

## Po co tworzymy **README**?

Jest to łatwy sposób na udzielenie odpowiedzi na pytania, które prawdopodobnie będą miały osoby, które chcą wykorzystać Twój projekt. Dotyczyć one będą instalacji i korzystania z projektu, a także tego jak rozpocząć współpracę z Tobą przy projekcie.

**Powinnieś\Powinnaś rozpocząć tworzenie nowego projektu od pliku README zwłaszcza jeśli chcesz, aby inni z niego korzystali lub go współtworzyli.**

## Gdzie ma znajdować się plik README?

W katalogu najwyższego poziomu projektu. 

Usługi hostingu kodu, takie jak [**GitHub**](https://github.com/), [**Bitbucket**](https://bitbucket.org/) i [**GitLab**](https://about.gitlab.com/), również będą szukać pliku **README** i wyświetlać go wraz z listą plików i katalogów w projekcie.

## Jak napisać plik README?

Chociaż pliki README można zapisać w dowolnym formacie pliku tekstowego, najpopularniejszym obecnie używanym jest **Markdown**. Pozwala na dodanie lekkiego formatowania. Możesz dowiedzieć się więcej na ten temat [tutaj](https://tadeuszsikorski.github.io/tags/markdown/). 

Niektóre inne formaty, które możesz zobaczyć, to [**zwykły tekst**](https://pl.wikipedia.org/wiki/Plik_tekstowy), [**reStructuredText**](https://pl.wikipedia.org/wiki/ReStructuredText) (powszechne w projektach języka Python) i [**Textile**](https://pl.wikipedia.org/wiki/Textile).

Możesz użyć dowolnego edytora tekstu. Istnieją wtyczki dla wielu edytorów: 
- [**Atom**](https://github.com/atom/markdown-preview), 
- [**Emacs**](https://github.com/jrblevin/markdown-mode), 
- [**Sublime Text**](https://github.com/facelessuser/MarkdownPreview), 
- [**Vim**](https://github.com/instant-markdown/vim-instant-markdown)
- [**Visual Studio Code**](https://code.visualstudio.com/docs/languages/markdown#_markdown-preview).

Umożliwiają one podgląd plików **Markdown** podczas ich edycji.

Możesz także użyć dedykowanego edytora **Markdown**, takiego jak [**Typora**](https://typora.io/) lub internetowych, takich jak [**StackEdit**](https://stackedit.io/) lub [**Dillinger**](https://dillinger.io/).

## Jak napisać dobre README?

Każdy projekt jest inny, więc zastanów się, które z tych sekcji dotyczą Twojego. Sekcje użyte w szablonie są sugestiami dla większości projektów open source. Należy również pamiętać, że podczas gdy plik README może być zbyt długi i szczegółowy, za długi jest lepszy niż za krótki. Jeśli uważasz, że plik README jest zbyt długi, rozważ skorzystanie z innej formy dokumentacji zamiast wycinania informacji.

### **Nazwa**
Wybierz zrozumiałą nazwę dla swojego projektu.

### **Opis** (*Description*)
Udziel informacji odnośnie tego, co konkretnie robi Twój projekt. 

Podaj kontekst powstania i dodaj link do strony z projektem, jeżeli taką chcesz dla niego stworzyć. W tym miejscu możesz również dodać sekcję **Funkcje** (*Features*) jak też sekcję **Tło** (*Background*). 

Jeśli istnieją alternatywy dla twojego projektu, jest to dobre miejsce na wymienienie czynników, które odróżniają go na tle innych projektów.

### **Odznaki**
W niektórych plikach README możesz zobaczyć małe obrazki, które przekazują metadane, takie jak informacje o tym, czy wszystkie testy przeszły pomyślnie. Możesz użyć [**Shields**](https://shields.io/), aby dodać ich trochę do swojego **README**.

### **Wizualizacje**
W zależności od tego, czego dotyczy projekt, dobrym pomysłem może być dołączenie zrzutów ekranu lub nawet wideo (często będziesz widzieć GIF-y zamiast rzeczywistych filmów). Narzędzia takie jak [**ttygif**](https://github.com/icholy/ttygif) mogą pomóc, ale sprawdź też [**Asciinema**](https://asciinema.org/), aby uzyskać bardziej wyrafinowaną metodę.

### **Instalacja** (*Installation*)
W ramach określonego ekosystemu może istnieć typowy sposób instalcji projektu, na przykład za pomocą [**Yarn**](), [**NuGet**]() lub [**Homebrew**](). Jednak rozważ możliwość, że ktoś kto czyta Twój plik README, jest nowicjuszem i chciałby uzyskać więcej wskazówek. Wymienienie konkretnych kroków pomaga usunięcia niejednoznaczności i zachęca ludzi do jak najszybszego korzystania z Twojego projektu. 

Jeśli działa tylko w określonym kontekście, takim jak *określona wersja* **języka programowania** lub **system operacyjny** albo ma **zależności**, które należy zainstalować ręcznie, dodaj również sekcję **Wymagania**(*Requirements*).

### **Zastosowanie** (*Usage*)
Zaprezentuj przykłady zastosowania projektu, jeśli możesz, pokaż oczekiwane wyniki działania danej funkcji. 

Pomocne jest umieszczenie w wierszu najmniejszego przykładu użycia, który można zademonstrować, jednocześnie udostępniając linki do bardziej wyrafinowanych przykładów, jeśli są one zbyt długie, aby można je było zamieścić w **pliku README**.

### **Wsparcie** (*Support*)
Powiedz innym, jak mogą zwrócić się do Ciebie o pomoc, gdy napotkają problem z Twoim projektem. 

Może to być dowolna kombinacja narzędzia do śledzenia problemów, adresu e-mail itp.

### **Mapa drogowa** (*Roadmap*)
Jeśli masz pomysły na przyszłe wydania, dobrym pomysłem jest spisanie ich w **README**.

### **Współtworzenie** (*Contributing*)
Napisz, czy jesteś otwarty na wprowadzanie zmian przez innych w projekcie i jakie są Twoje wymagania dotyczące ich przyjmowania.

Dla osób, które chcą wprowadzić zmiany w projekcie, warto stworzyć dokumentację dotyczącą rozpoczęcia współpracy. 

Być może istnieje skrypt, który powinni uruchomić lub jakieś zmienne środowiskowe, które muszą ustawić. Wyraźnie przedstaw te kroki. Te instrukcje mogą być również przydatne dla Ciebie w przyszłości.

Możesz również udokumentować polecenia, aby **lintować kod** lub **uruchamiać testy**. Te kroki pomagają zapewnić wysoką jakość kodu i zmniejszyć prawdopodobieństwo, że zmiany nieumyślnie coś zepsują. Posiadanie **instrukcji do uruchamiania testów** jest szczególnie przydatne, jeśli wymaga zewnętrznej konfiguracji, takiej jak uruchomienie serwera Selenium do testowania w przeglądarce.

### **Autorzy i podziękowania**
Okaż swoje uznanie tym, którzy przyczynili się do powstania projektu.

### **Licencja** (License)
W przypadku projektów typu open source opisz, w jaki sposób jest on licencjonowany.

### **Stan projektu** (*Project status*)
Jeśli zabrakło Ci energii lub czasu na projekt, umieść notatkę na górze pliku README, mówiącą, że rozwój zwolnił lub całkowicie się zatrzymał. Ktoś może zdecydować się na rozwidlenie twojego projektu lub zgłoszenie się jako ochotnik, aby wkroczyć jako opiekun lub właściciel, umożliwiając kontynuowanie projektu. 

Możesz również skierować wyraźną prośbę do opiekunów.

## Podsumowanie

W tym wpisie dowiedziałeś się co to jest **plik README**, dlaczego jest on istotny dla projektu i jakie rzeczy uwzględnić, aby stworzyć dobre README.

## Źródła

1. [Make a README](https://www.makeareadme.com/#what-is-it)
2. [Jak napisać dobre README projektu na GitHubie?](https://www.flynerd.pl/2018/06/jak-napisac-dobre-readme-projektu-na-githubie.html)