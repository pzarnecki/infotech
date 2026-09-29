# Arkusz kalkulacyjny w pracy Analityka / DevOpsa

Arkusz kalkulacyjny (Google Sheets, Microsoft Excel) to znacznie więcej niż narzędzie do tworzenia list obecności czy zestawień wydatków. W branży IT jest to potężne, pierwsze w kolejności środowisko do szybkiej analizy danych, pracy z logami czy raportowania.

## 1. Import i obróbka "brudnych danych"

W codziennej pracy IT często otrzymujemy tzw. "surowe dane" (np. logi z serwera, wyciągi bazy danych) w formatach takich jak CSV (Comma-Separated Values). 

Pierwszym krokiem jest import takich danych do arkusza. Należy uważać na separator – systemy mogą używać przecinka, średnika lub znaku tabulacji.
Po imporcie dane często wymagają oczyszczenia:
- **`TRIM(tekst)` (USUŃ.ZBĘDNE.ODSTĘPY)**: Usuwa spacje z początku i końca tekstu. Bardzo ważne przed używaniem formuł wyszukujących, ponieważ " błąd 404" to nie to samo co "błąd 404".
- **`CLEAN(tekst)` (OCZYŚĆ)**: Usuwa niewidoczne znaki kontrolne.
- **Tekst jako kolumny**: Przydatne narzędzie, gdy w jednej komórce mamy zbitkę danych (np. imię i nazwisko), którą chcemy rozdzielić za pomocą spacji lub innego znaku.

## 2. Kluczowe formuły analityczne

Aby wyciągać wnioski z danych, musimy je agregować.

**Funkcje warunkowe:**
- `IF(warunek; wartość_prawda; wartość_fałsz)`: Zwraca wynik w zależności od spełnienia warunku.
  *Przykład:* `=IF(C2 >= 400; "Błąd"; "OK")` - weryfikacja kodu statusu HTTP.
- `COUNTIF(zakres; kryterium)`: Zlicza komórki.
  *Przykład:* `=COUNTIF(A2:A100; "404")` - zlicza ile razy wystąpił kod błędu 404.
- `SUMIF(zakres; kryterium; zakres_sumowania)`: Sumuje wartości, gdy spełniony jest warunek.

**Łączenie danych - VLOOKUP (WYSZUKAJ.PIONOWO):**
Jedna z najważniejszych formuł. Pozwala szukać wartości w pierwszej kolumnie wyznaczonego zakresu i zwracać wartość z innej kolumny w tym samym wierszu.
Składnia: `=VLOOKUP(szukana_wartość; tabela_zakres; nr_kolumny_z_wynikiem; [dokładność])`
*Uwaga:* Zamiast VLOOKUP zaawansowani analitycy często używają kombinacji `INDEX` + `MATCH` (INDEKS + PODAJ.POZYCJĘ), która jest szybsza i pozwala szukać po dowolnej kolumnie, a nie tylko pierwszej.

## 3. Tabele przestawne (Pivot Tables)

Gdy mamy tysiące wierszy, pisanie formuł staje się uciążliwe. Tabele przestawne pozwalają na dynamiczne podsumowanie danych bez pisania kodu.
Wystarczy zaznaczyć zakres i z menu wybrać "Wstaw tabelę przestawną".
Możemy zdefiniować:
- **Wiersze:** np. Adres IP
- **Wartości:** np. zlicz (Count) Adresy IP
Dzięki temu w 3 sekundy wiemy, z jakiego adresu IP było najwięcej żądań do serwera.

## 4. Formatowanie warunkowe i Wykresy

Analiza to jedno, wizualizacja to drugie. Formatowanie warunkowe automatycznie zmienia wygląd komórki na bazie jej wartości (np. zaznacza na czerwono każdy czas odpowiedzi serwera powyżej 1000ms).
- **Sparklines:** Funkcja `=SPARKLINE(zakres)` tworzy mały wykres bezpośrednio wewnątrz pojedynczej komórki, co jest świetne do pokazywania trendu na listach gęstych od danych.

## Podsumowanie: Arkusz vs Skrypt w Pythonie
Kiedy używać arkusza?
- Do szybkiej "ad-hoc" analizy danych (np. plik z 10 tysiącami wierszy).
- Gdy wynikiem analizy ma być interaktywny raport dla biznesu, który nie wymaga znajomości kodu.
Kiedy przejść na Pythona (biblioteka Pandas)?
- Gdy pliki są ogromne (miliony wierszy spowolnią każdy arkusz).
- Gdy proces musi być powtarzany codziennie automatycznie (skrypt można wpiąć w harmonogram zadań).
- Przy skomplikowanych algorytmach i transformacjach.
