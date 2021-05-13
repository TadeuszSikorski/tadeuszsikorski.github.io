+++
title="Wprowadzenie do baz danych"
date=2021-05-12

[taxonomies]
tags = ["databases"]
+++

W tym poście odpowiemy sobie na następujące pytania:
1. Czym jest baza danych? 
2. Do czego służy? 
3. Jakie są typy baz danych? 

## 1. Definicja bazy danych

**Baza danych** to uporządkowany zbiór informacji przechowywany w formie elektronicznej w pamięci trwałej urządzenia. Wykorzystywany przez programy użytkowe wraz z oprogramowaniem umożliwiającym definiowanie, wykorzystywanie i modyfikowanie danych. Do zarządzania bazą danych służy **System zarządzania bazą danych** (**D**ata**b**ase **M**anagement **S**ystem, **DBMS**). Najprostszym i najstarszym sposobem fizycznej realizacji bazy danych jest zapisanie jej w postaci plików. 

Informacje zapisane w bazie danych modelują przedmioty, pojęcia lub zjawiska występujące w otaczającym nas świecie. Tak jak ma to miejsce w programowaniu zorientowanym obiektowo. Dla każdego przedmiotu, pojęcia lub zjawiska tworzy się nowy obiekt z odpowiednimi atrybutami.

## 2. Do czego służy baza danych?

Zazwyczaj baza danych zawiera całość informacji wykorzystywanych w pewnym obszarze działania, np. baza danych systemu zarządzania przedsiębiorstwem zawiera wszystkie informacje związane z finansami i księgowością, zaopatrzeniem, kadrami i płacami. Tak więc odgrywają one istotną rolę we wszystkich działaniach gospodarczych. Stosuje się je w różnego rodzaju badaniach naukowych, biznesie, analizie i eksploracji danych. 

## Typy baz danych

Bazy można podzielić na:
- **re­la­cyj­ne** – dane są po­wią­za­ne, tabele powiązane są ze sobą relacjami. Przykładowe bazy danych: **MySQL**, **SQLi­te**.
- **obiek­to­we** – dane są prze­cho­wy­wa­ne w struk­tu­rze obiek­to­wej, cechą cha­rak­te­ry­stycz­ną ta­kiej bazy jest to, że prze­cho­wu­je obiek­ty o do­wol­nych struk­tu­rach wraz z przy­pi­sa­ny­mi do nich pro­ce­du­ra­mi
- **re­la­cyj­no-obiek­to­we** – dane są prze­cho­wy­wa­ne w struk­tu­rze obiek­to­wej, ale są po­wią­za­ne ze sobą tak jak w ba­zach re­la­cyj­nych. Przykładowe bazy danych: **Post­gre­SQL**, **Oracle**, **Microsoft SQL Server**. 
- **stru­mie­nio­we** – dane są prze­twa­rza­ne jako stru­mie­nie da­nych, model za­kła­da, że nie­któ­re lub wszyst­kie na­pły­wa­ją­ce do sys­te­mu dane nie są do­stęp­ne w do­wol­nej chwi­li
- **tem­po­ral­ne** – są po­dob­ne do baz re­la­cyj­nych, z tą róż­ni­cą, że każdy re­kord po­sia­da swój znacz­nik cza­so­wy, tzw. stem­pel okre­śla­ją­cy, czy w danym cza­sie za­pi­sa­na war­tość jest praw­dzi­wa
- **nie­re­la­cyj­ne** – dane są za­pi­sy­wa­ne w for­mie klucz-war­tość i nie są ze sobą po­wią­za­ne, w ta­kiej bazie naj­czę­ściej nie ma wy­ma­ga­nia, żeby obiek­ty były jed­no­rod­ne pod wzglę­dem struk­tu­ry. Przykładowe bazy danych: **Mon­goDB**.

## Poziomy modelowania baz danych

Przy definiowaniu bazy danych wyróżnia się trzy poziomy modelowania: 
- zewnętrzny (sposób postrzegania danych przez konkretnego użytkownika bazy danych), 
- pojęciowy (sposób organizacji danych, wspólny dla wszystkich użytkowników),
- wewnętrzny (sposób zapamiętania danych w pamięci zewnętrznej).

## Podsumowanie

Z tego posta dowiedziałeś się co to są bazy danych, po co są używane i jakie są typy baz oraz poziomy ich modelowania. 

W kolejnym wpisach dowiesz się więcej o [relacyjnych](https://tadeuszsikorski.github.io/blog/relacyjne-bazy-danych/) i [nierelacyjnych](https://tadeuszsikorski.github.io/blog/nierelacyjne-bazy-danych/) bazach danych.

## Źródła

1. [Baza danych - Encyklopedia PWN](https://encyklopedia.pwn.pl/haslo/baza-danych;3875256.html)
2. [Chcę na wcoraj - Co to jest baza danych? Jakie rodzaje baz warto znać?](https://chcenawczoraj.pl/software/co-to-jest-baza-danych-jakie-rodzaje-baz-warto-znac)