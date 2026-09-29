# Arkusz kalkulacyjny: Twoje Narzędzie do Analityki Danych

Wielu osobom arkusz kalkulacyjny (taki jak Microsoft Excel czy Google Sheets) kojarzy się wyłącznie z księgowością. Prawda jest jednak taka, że arkusze to najpopularniejsze narzędzia do obróbki danych na świecie. Używają ich analitycy gier wideo, specjaliści od marketingu, naukowcy i inżynierowie. Dlaczego? Bo to w zasadzie prosty język programowania z wbudowanym interfejsem.

## Obróbka "brudnych danych"

Gdy pobierasz dane z Internetu lub logi ze szkolnej strony internetowej, są one zazwyczaj uszkodzone lub nieestetyczne. Ktoś wpisał swoje imię z małej litery, gdzie indziej są dwa numery telefonów nałożone na siebie, a wiele wierszy to zduplikowane zgłoszenia (np. ktoś kliknął przycisk "Wyślij" dwa razy).

Pierwszym krokiem każdej analizy jest proces **oczyszczania danych** (Data Cleaning). Najczęściej wykorzystuje się do tego wbudowane w arkusz funkcje:
- **Usuń duplikaty:** Automatycznie skanuje wybrane kolumny i usuwa powtarzające się wiersze, zostawiając tylko jeden unikatowy wpis.
- **Znajdź i zamień (Ctrl+H):** Szybki sposób na ujednolicenie danych (np. zamiana "Krk" i "Cracow" na poprawne "Kraków").
- Pamiętaj: Nawet najmądrzejsze formuły podadzą zły wynik (np. nie policzą dobrze średniej), jeśli w jednej z komórek będzie ukryta, niewidoczna spacja przed liczbą!

## Kluczowe formuły

Formuły w arkuszach zawsze zaczynają się od znaku równości `=`. Najpopularniejsze z nich to:

1. **SUMA(A1:A10)** – Zlicza wartość komórek w zakresie.
2. **ŚREDNIA(A1:A10)** – Oblicza średnią arytmetyczną z liczb.
3. **JEŻELI (IF)** – Podstawowa logika. Narzędzie sprawdza warunek i zwraca inny tekst w zależności od wyniku.
   *Przykład:* `=JEŻELI(B2>=50; "Zdał"; "Nie zdał")` oznacza: jeśli wartość w komórce B2 jest większa lub równa 50, wpisz "Zdał", w przeciwnym wypadku wpisz "Nie zdał".
4. **LICZ.JEŻELI (COUNTIF)** – Błyskawiczne zliczanie, jeśli warunek jest spełniony.
   *Przykład:* `=LICZ.JEŻELI(C2:C100; "Apple")` policzy, w ilu wierszach w kolumnie C znajduje się dokładnie słowo "Apple". To idealne do podsumowywania wyników ankiet.

## Król arkuszy: VLOOKUP (WYSZUKAJ.PIONOWO)

Prawdziwa moc arkusza objawia się, gdy musisz połączyć dane z dwóch różnych tabel. Załóżmy, że z systemu pobrałeś raport sprzedaży, gdzie znajduje się jedynie ID produktu (np. 101, 102). W osobnym pliku masz cennik (ID, Nazwa, Cena). Chcesz poznać pełny koszt koszyka zakupowego.

Zamiast przeklejać wszystko ręcznie, używasz funkcji VLOOKUP (WYSZUKAJ.PIONOWO).
Algorytm działa prosto: **Bierze wartość (ID 101), idzie do innej wskazanej tabeli, odszukuje ID 101 w jej pierwszej kolumnie, a następnie zwraca nam wynik z wybranej kolumny z tego wiersza (np. cenę).** Opanowanie tej funkcji czyni z Ciebie pracownika o wiele bardziej wydajnego w biurze.

## Wykresy: Pozwól liczbom przemówić

Ludzki mózg ma problem z szybką analizą 500 wierszy z liczbami. Przekształcenie danych w grafikę to kluczowy element analityki danych. Arkusze kalkulacyjne potrafią tworzyć profesjonalne wykresy w kilka kliknięć:
- **Wykresy kołowe (Pie chart):** Najlepsze do pokazywania udziału w całości (np. procentowy podział ról postaci wybieranych w grze MOBA, głosy na partie polityczne). Warunek: całość powinna sumować się do 100%.
- **Wykresy słupkowe (Bar chart):** Optymalne do porównywania oddzielnych kategorii między sobą, np. wielkości sprzedaży w różnych oddziałach firmy.
- **Wykresy liniowe (Line chart):** Obowiązkowe przy prezentacji trendów i zmian w czasie (np. jak zmieniała się popularność danej piosenki przez poszczególne tygodnie roku).

Wystarczy zaznaczyć oczyszczoną tabelę, kliknąć "Wstaw wykres" i odrobinę go sformatować, nadając odpowiedni tytuł i opisując osie. Gotowe!
