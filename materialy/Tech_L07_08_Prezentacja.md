## Arkusz Kalkulacyjny w Analizie Danych

* Arkusz to nie tylko tabele – to potężne narzędzie analityczne
* Kiedy używać arkuszy (szybka analiza) vs kiedy Pythona (Big Data)
* Umiejętności DevOps i analityka w pracy z brudnymi danymi
* Ekstrakcja wiedzy z surowych logów i statystyk

---

## Import i czyszczenie danych

* Importowanie danych zewnętrznych: CSV, TSV
* Częste problemy: różne separatory, formaty dat, białe znaki
* Czyszczenie danych - przydatne funkcje:
  * `TRIM()` (usuwanie spacji)
  * `CLEAN()` (usuwanie znaków niedrukowanych)
  * Znajdź i zamień / Usuwanie duplikatów

---

## Funkcje analityczne i logiczne

* **IF (JEŻELI)**: Podstawowa logika decyzyjna
* **COUNTIF (LICZ.JEŻELI)**: Zliczanie wystąpień spełniających warunek
* **SUMIF (SUMA.JEŻELI)**: Sumowanie wartości spełniających kryterium
* Idealne do szybkiego sprawdzania ilości np. błędów 404 w logach lub statusów płatności

---

## Łączenie danych - WYSZUKAJ.PIONOWO (VLOOKUP)

* Cel: Pobieranie danych z innych tabel na podstawie wspólnego klucza
* Składnia VLOOKUP (wartość, zakres, kolumna, dokładność)
* Alternatywy: INDEX + MATCH (INDEKS + PODAJ.POZYCJĘ) - większa elastyczność
* Zastosowanie: np. przypisanie nazwy błędu do kodu HTTP

---

## Tabele przestawne (Pivot Tables)

* Najpotężniejsze narzędzie arkusza do analizy
* Szybkie agregowanie i grupowanie dużych zbiorów danych
* Przeciągnij i upuść: kolumny, wiersze, wartości
* Przykład: Zliczenie liczby logowań dla każdego adresu IP w ciągu miesiąca

---

## Wizualizacja i Formatowanie Warunkowe

* Wyróżnianie istotnych danych (np. czerwony kolor dla błędów serwera)
* Skale kolorów do wykrywania anomalii w danych liczbowych
* Sparklines - małe wykresy wewnątrz pojedynczej komórki
* Wykresy Combo - łączenie wykresu słupkowego (np. liczba wizyt) z liniowym (np. czas odpowiedzi serwera)

---

## Analiza logów serwera - Studium Przypadku

* Struktura typowego loga: IP, Data/Czas, Metoda, URL, Status HTTP, Rozmiar
* Proces analizy:
  1. Import CSV
  2. Wydzielenie daty i czasu (Tekst jako kolumny)
  3. Formatowanie warunkowe na statusach (np. >= 400)
  4. Tabela przestawna - top 5 najczęstszych IP (szukanie botów)
* Wyciąganie wniosków na podstawie suchych danych

---

## Arkusz vs Skrypt (Python/Pandas)

* **Arkusz (Sheets/Excel)**:
  * Szybki podgląd i wizualizacja
  * Dane do miliona wierszy (Excel)
  * Łatwe udostępnianie raportów biznesowi
* **Skrypt (Python)**:
  * Przetwarzanie gigabajtów danych
  * Automatyzacja powtarzalnych zadań
  * Zaawansowane przekształcenia (machine learning)
