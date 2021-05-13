+++
title="Relacyjne bazy danych"
date=2021-05-12
[taxonomies]
tags = ["databases", "sql"]
+++

## Relacyjny model danych

W **relacyjnym modelu danych** modele pojęciowy i zewnętrzny - opisane w poprzednim poście - składają się z tzw. **encji** (ang. entity) i ich związków. **Encje** odpowiadają obiektom lub pojęciom istniejącym w modelowanej rzeczywistości. **Typ encji** określa rodzaj modelowanego obiektu lub pojęcia, a zarazem zestaw jego atrybutów. Związki encji odpowiadają powiązaniom występującym w modelowanej rzeczywistości. Zbiór typów encji i związków pomiędzy nimi tworzy tzw. **schemat bazy danych**.

W najprostszym ujęciu w modelu relacyjnym dane grupowane są w **relacje**, które reprezentowane są przez **tablice**. **Relacje** są pewnym **zbiorem rekordów** o identycznej strukturze wewnętrznie powiązanych za pomocą związków zachodzących pomiędzy danymi. **Relacją** może być **tabela** zawierająca dane teleadresowe pracowników, zaś **schemat** może zawierać wszystkie dane dotyczące firmy. Takie podejście w porównaniu do innych modeli danych **ułatwia wprowadzanie zmian**, **zmniejsza możliwość pomyłek**, ale dzieje się to **kosztem wydajności**.

**Model relacyjny** jest powszechnie uznawany za jedno z największych osiągnięć technicznych XX wieku. Zrewolucjonizował on sposób postrzegania baz danych. Na modelu relacyjnym oparta jest **relacyjna baza danych** (ang. *relational database*), w której dane są przedstawione w postaci relacyjnej.

## Algebra relacji

**[Algebra relacji](http://mst.mimuw.edu.pl/lecture.php?lecture=bad&part=Ch2)** to model teoretyczny do opisywania semantyki **relacyjnych baz danych**. Zaproponowany został przez [Edgara Franka Codda](https://pl.wikipedia.org/wiki/Edgar_Frank_Codd), twórcę koncepcji relacyjnego modelu danych. Swoje postulaty zawarł w pracy pt. "*A Relational Model of Data for Large Shared Data Banks*" z 1970 roku. A w pracy pt. "*Relational Completeness of Data Base Sublanguages*" z 1972 roku uszczegółowił opis modelu oraz przedstawił dwa modele formalne odpytywania czyli przeszukiwania danych. Tu właśnie po raz pierwszy pojawiły się terminy **algebra relacji** oraz **rachunek relacyjny**.

Jest to algebra, w której dziedzinę stanowią **relacje**. Zmienne występujące w wyrażeniach tej algebry odpowiadają pojedynczym relacjom. Operatory **algebry relacji** zostały dobrane tak, aby odpowiadały typowym operacjom występującym w zapytaniach podczas **wyszukiwania informacji** z tabel w bazie danych.

Tak określona algebra miała być *językiem zapytań* (*query language*) dla relacyjnych baz danych. Dzięki tej algerze powstał język **SQL** (ang. **Structured Query Language**), strukturalny język zapytań.

## Relacyjne bazy danych

Występuje wiele implementacji relacyjnych baz danych. Najpopularniejszymi są:
- MySQL (MariaDB),
- SQLite,
- PostgreSQL,
- Oracle Database,
- Microsoft SQL Server,
- HyperSQL

Różnią się one między sobą wersją standardu SQL, którą obsługują, a także dedykowanymi dialektami języka SQL. Dla PostgreSQL jest to język [PL/pgSQL](https://pl.wikipedia.org/wiki/PL/pgSQL). Dla Oracle jest to [PL/SQL](https://pl.wikipedia.org/wiki/PL/SQL). Dla Microsoft SQL Server jest to [Transact-SQL, (T-SQL)](https://pl.wikipedia.org/wiki/Transact-SQL). Łączy je to, że są to języki proceduralne. Są rozszerzeniem języka SQL pozwalającym na tworzenie konstrukcji takich jak pętle, instrukcje warunkowe oraz zmienne.

## Operacje w relacyjnej bazie danych

Relacyjna baza danych umożliwia przeprowadzenie operacji takich jak definiowanie, wyszukiwanie czy manipulacja danymi. Pozwala to na:
- utworzenie nowej bazy danych i określenia jej schematu (logicznej struktury danych) za pomocą wyspecjalizowanego *języka definiowania danych*(*Data Definition Language*, *DDL*)
- możliwość tworzenia zapytań o dane (*kwerendy*) za pomocą wyspecjalizowanego *języka zapytań*(*Data Query Language*, *DQL*)
- możliwość aktualiacji danych za pomocą wyspecjalizowanego *języka operowania danymi*(*Data Manipulation Language*, *DML*)
- kontrolowanie dostępu do danych przechowywanych w bazie danych (autoryzacja) za pomocą wyspecjalizowanego *języka kontroli danych*(*Data Control Language*, *DCL*)

Wymienione tu języki są podstawową grupą języków podrzędnych języka SQL.

## Podsumowanie

Z tego wpisu dowiedziałeś się o relacyjnym modelu danych, algebrze relacji i relacyjnych bazach danych. 

W kolejnym wpisie dowiesz się więcej o nierelacyjnym modelu danych i nierelacyjnych bazach danych.

## Źródła

1. [Baza danych - Encyklopedia PWN](https://encyklopedia.pwn.pl/haslo/baza-danych;3875256.html)
2. [Model relacyjny - Wikipedia](https://pl.wikipedia.org/wiki/Model_relacyjny)
3. [Bazy danych - Uniwersytet Warszawski](http://wazniak.mimuw.edu.pl/index.php?title=Bazy_danych)
4. 
5. [Wstęp do relacyjnych baz danych](https://www.samouczekprogramisty.pl/wstep-do-relacyjnych-baz-danych/)
6. [Algebra relacji](http://mst.mimuw.edu.pl/lecture.php?lecture=bad&part=Ch2)
7. [Edgar Frank Codd - Wikipedia](https://pl.wikipedia.org/wiki/Edgar_Frank_Codd)