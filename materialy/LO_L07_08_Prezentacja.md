## Arkusz kalkulacyjny: Wstęp do analityki danych
- Wprowadzenie do Google Sheets / Microsoft Excel
- Do czego w IT (i nie tylko) używa się arkuszy kalkulacyjnych?
- Podstawowa składnia formuł i adresowanie komórek
- Magia danych w zasięgu ręki

---
## Czyste dane to podstawa
- Prawdziwe dane są "brudne" – zawierają literówki, podwójne spacje, braki
- Oczyszczanie to pierwszy krok analityka danych
- Narzędzia: Usuń duplikaty, Znajdź i Zamień
- Puste wiersze lub błędnie sformatowane daty psują każdy wykres!

---
## Formuły i funkcje matematyczne
- Formułę zawsze zaczynamy znakiem = (równa się)
- `SUMA(A1:A10)` - sumuje liczby we wskazanym zakresie
- `ŚREDNIA(A1:A10)` - wyciąga średnią arytmetyczną
- Adresowanie względne (A1) vs bezwzględne ($A$1 - nie przesuwa się przy kopiowaniu formuły!)

---
## Podejmowanie decyzji w komórkach
- Funkcja `JEŻELI` (IF) działa jak instrukcja warunkowa w programowaniu
- `=JEŻELI(A1>50; "Zdał"; "Nie zdał")`
- `LICZ.JEŻELI(B1:B100; "Warszawa")` - liczy komórki, które spełniają konkretny warunek
- Bardzo przydatne przy segmentacji klientów lub sprawdzaniu list obecności

---
## Wyszukiwanie danych (VLOOKUP)
- Król arkuszy kalkulacyjnych: `WYSZUKAJ.PIONOWO` (VLOOKUP)
- Pozwala łączyć dane z różnych tabel (np. cennik w jednym arkuszu, zamówienia w drugim)
- Działanie: "Znajdź to ID produktu w tamtej tabeli i podaj mi jego cenę"
- Zastępuje godziny żmudnego, ręcznego przypisywania wartości

---
## Wizualizacja danych (Wykresy)
- Liczby w tabelach nie mówią nic ludzkiemu oku. Potrzebujemy obrazu!
- Wykres kołowy (Pie chart): pokazuje procentowy udział w całości (np. udział rynku)
- Wykres słupkowy/kolumnowy (Bar chart): świetny do porównywania wartości (np. sprzedaż między miesiącami)
- Wykres liniowy (Line chart): idealny do prezentowania trendów w czasie

---
## Filtrowanie i sortowanie
- Chcesz zobaczyć tylko klientów z Krakowa? Użyj Filtra!
- Filtry (ikona lejka) pozwalają ukryć wiersze niespełniające kryteriów bez ich usuwania
- Sortowanie A-Z lub od największej do najmniejszej błyskawicznie pokazuje liderów rankingu
- Błędy przy sortowaniu: ZAWSZE upewnij się, że zaznaczyłeś wszystkie kolumny tabeli (inaczej pomieszasz dane!)
