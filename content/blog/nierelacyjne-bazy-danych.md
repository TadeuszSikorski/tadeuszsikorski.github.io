+++
title="Nierelacyjne bazy danych"
date=2021-05-13
[taxonomies]
tags = ["databases", "nosql"]
+++

## Definicja 

**Nierelacyjna baza danych** (**NoSQL**, *Non SQL* lub *Non Relational*) to taka baza danych zapewniająca mechanizm do przechowywania i wyszukiwania danych modelowanych w inny sposób niż relacje tabelaryczne używane w relacjach baz danych SQL.

NoSQL umożliwia tworzenie prostych projektów, lepszą kontrolę nad dostępnością oraz **horyzontalne skalowanie do klastrów maszyny**, co jest *problemem dla relacyjnych baz danych*. Bazy NoSQL wykorzystywane są coraz częściej w **big data** działających w czasie rzeczywistym. 

NoSQL stworzony został z potrzeby obsługiwania większych wolumenów danych, która wymusiła przejście na model budowania platform na klastrach mniej wydajnych serwerów. Ta zmiana wzbudziła także wątpliwości w sprawie łatwości tworzenia kodu dobrze współpracującego z bazami relacyjnymi.

Innymi cechami wspólnymi dla baz NoSQL są:
- otwarty kod (open source), 
- dopasowanie do potrzeb standardu Web 2.0, 
- brak schematu danych,
- możliwość wyboru sposobu przechowywania danych w zależności od ich specyfiki.

## Struktury danych używane w bazach NoSQL

Struktury danych używane przez NoSQL różnią się od tych używanych domyślnie w [relacyjnych bazach danych](), dzięki czemu niektóre operacje NoSQL są szybsze. Najczęściej spotykanymi strukturami są:
- klucz–wartość (Aerospike, Apache Ignite, ArangoDB, BerkeleyDB, Couchbase, Dynamo, FairCom c-treeACE, FoundationDB, InfinityDB, LevelDB, MemcacheDB, MUMPS, Oracle NoSQL Database, OrientDB, Project Voldemort, Redis, Riak, SDBM/Flat File dbm, ZooKeeper), 
- graf (AllegroGraph, ArangoDB, InfiniteGraph, Apache Giraph, MarkLogic, Neo4J, OrientDB, Virtuoso), 
- dokument (Apache CouchDB, ArangoDB, BaseX, Clusterpoint, Couchbase, Cosmos DB, IBM Domino, MarkLogic, MongoDB, OrientDB, Qizx, RethinkDB), 
- szerokokolumnowe (Amazon DynamoDB, Bigtable, Cassandra, Druid, HBase, Hypertable, KAI, KDI, OpenNeptune, Qbase)
- obiektowe (DB4O, Objectivity/DB, Perst, Shoal, ZopeDB).

Wybór konkretnej bazy danych pod względem formy przechowywania danych zależy od problemu, który musi rozwiązać. Czasami struktury danych używane przez bazy danych NoSQL są również postrzegane jako bardziej elastyczne niż relacyjne bazy danych.

## Rodzaje baz NoSQL
### Bazy danych typu klucz-wartość
Bazy klucz–wartość korzystają z asocjacyjnej tablicy znanej również jako mapa lub słownik. Jest to podstawowy model danych. 

W tym modelu dane są reprezentowane jako zbiór par klucz–wartość. Każdy klucz może pojawić się tylko raz w bazie. 

Model klucz–wartość jest jednym z najprostszych nietrywialnych modeli danych. Bogatsze modele danych są często implementowane jako jego rozszerzenie. Model klucz–wartość może zostać rozszerzony na dyskretnie uporządkowany model, który utrzymuje klucze w porządku leksykograficznym. Przez to, że bazy klucz–wartość zawsze wykorzystują klucz główny, przeważnie cechują się wysoką wydajnością i są łatwo skalowalne. W takich bazach wyszukiwanie odbywa się po kluczu.

Mogą one wykorzystywać modele spójności od spójności ostatecznej (wartość zreplikowana na inne serwery) do możliwości serializacji. Niektóre bazy danych obsługują porządkowanie kluczy. Sposobem na rozwiązanie konfliktu aktualizacji może być faworyzowanie najnowszego wpisu lub zwrócenie wszystkich wartości w celu dokonania wyboru. Istnieją różne implementacje sprzętowe.

Taka baza wykorzystywana jest do przechowywania: 
- obrazów, 
- danych sesji, 
- koszyka zakupów, 
a także: 
- tworzenia wyspecjalizowanych systemów plików, 
- jako pamięci podręcznych obiektów, 
- systemów zaprojektowanych pod kątem skalowalności.

### Bazy danych zorientowane na dokumenty

Dokument jest podstawowym zbiorem danych dla baz dokumentów. Dokumenty zawierają i kodują dane w niektórych standardowych formatach lub kodowaniach: 
- **XML**, 
- **JSON**, 
- **YAML**,
- **BSON** (format binarny). 

Dokumenty są adresowane w bazie danych za pomocą unikalnego klucza, który reprezentuje ten dokument. Jedną z innych cech charakterystycznych bazy danych zorientowanej na dokumenty jest to, że oprócz wyszukiwania klucza przeprowadzanego przez bazy danych typu klucz–wartość, baza danych oferuje również *interfejs API* lub *język zapytań*, który pobiera dokumenty na podstawie ich zawartości. 

Różne implementacje oferują różne sposoby organizowania lub grupowania dokumentów: 
- kolekcje, 
- tagi, 
- niewidoczne metadane, 
- hierarchie katalogów, 
- wiadra.

W tabelarycznych relacyjnych bazach danych każda kolumna musi zawierać taką samą sekwencję pól definiowana przez wartość lub oznaczona jako *null*, podczas gdy dokumenty w kolekcji mogą mieć zupełnie inne pola.

Baza danych zorientowana na dokumenty jest używana do:
- logowania zdarzeń, 
- analizy stron internetowych,
- analizy w czasie rzeczywistym, 
- aplikacjach e-commerce.

### Bazy danych typu rodzina kolumn

Analogicznie do relacyjnych baz danych, rodzina kolumn jest tabelą, a każda para klucz–wartość jest rekordem. Każda kolumna to krotka (*triplet*) składająca się z nazwy kolumny, wartości i stempla czasu. Stempel czasu jest odpowiedzią na problem aktualizacji. 

Istnieją dwa typy rodziny kolumn: 
- standardowa rodzina kolumn
-  super rodzina kolumn. 
  
Bazy danych typu rodzina kolumn są używane do:
- logowania zdarzeń, 
- zarządzania treścią, 
- jako liczniki, 
- do wygasających danych.

### Bazy danych typu graf

Ten rodzaj bazy danych jest przeznaczony dla danych, których relacje są dobrze reprezentowane jako wykres składający się z elementów powiązanych ze skończoną liczbą relacji między nimi. 

Rodzajem danych mogą być:
- relacje społeczne, 
- połączenia transportu publicznego, 
- mapy drogowe, 
- topologie sieci itp. 

Baza grafów jest oparta na **węzłach** (*encje*), **krawędziach** (*relacje*), **właściwościach**, **teorii grafów**. 

Bazy danych typu graf są używane:
- w sieciach społecznościowych, 
- do wytyczania tras.

## Obsługa danych relacyjnych

Istnieją trzy główne techniki obsługi danych relacyjnych w bazie danych NoSQL:

### **Wiele zapytań** (*Multiple queries*)

Zamiast odzyskiwać wszystkie dane za pomocą jednego zapytania, często wykonuje się kilka zapytań w celu uzyskania pożądanych danych. 

Zapytania NoSQL są często szybsze niż tradycyjne zapytania SQL, więc koszt konieczności wykonania dodatkowych zapytań jest akceptowalny.

### **Buforowanie** (*Caching*), **replikacja** (*replication*) i **nienormalizowane dane** (*non-normalized data*)

Zamiast tylko przechowywać klucze obce, często zachowuje się rzeczywiste obce wartości wraz z danymi modelu. 

Na przykład każdy komentarz do bloga może zawierać oprócz identyfikatora użytkownika także nazwę użytkownika, zapewniając w ten sposób łatwy dostęp do nazwy użytkownika bez konieczności ponownego wyszukiwania. 

Kiedy jednak zmieni się nazwa użytkownika, będzie ona musiała zostać zmieniona w wielu miejscach w bazie danych. Tak więc podejście to działa lepiej w przypadku, gdy odczyty są znacznie częstsze niż zapisy.

### **Zagnieżdżanie danych** (*Nesting data*)

W bazach danych dokumentów, takich jak **MongoDB**, często umieszcza się więcej danych w mniejszej liczbie dokumentów. 

Na przykład w aplikacji do blogowania można wybrać przechowywanie komentarzy w dokumencie posta na blogu, tak aby po pojedynczym pobieraniu otrzymywano wszystkie komentarze. 

Tak więc w tym podejściu pojedynczy dokument zawiera wszystkie dane potrzebne do określonego zadania.

## Podsumowanie 

W tym wpisie dowiedziałeś się o nierelacyjnych bazach danych NoSQL, jakich struktur danych używają, gdzie są wykorzystywane. 

## Źródła

1. [NoSQL - Wikipedia](https://pl.wikipedia.org/wiki/NoSQL)