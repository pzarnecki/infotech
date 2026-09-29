# Vademecum Praktyczne: Profesjonalny Edytor Tekstu, Chmura i Google NotebookLM
## Podręcznik Warsztatowy dla Liceum Ogólnokształcącego
**Autor:** Przemysław Żarnecki • Standard INFOTECH / Certyfikacja ECDL Module B3

---

## 1. Wprowadzenie: Po co informatykowi procesor tekstu?
W powszechnym wyobrażeniu praca w IT to wyłącznie pisanie kodu w IDE. W rzeczywistości inżynierowie oprogramowania, analitycy biznesowi i kierownicy projektów spędzają do 40% swojego czasu na tworzeniu, recenzowaniu i aktualizowaniu dokumentacji:
* **Briefów projektowych** (uzgadnianie z klientem, co właściwie ma powstać),
* **Specyfikacji wymagań** (precyzyjne definicje działania systemów),
* **Raportów z audytów bezpieczeństwa i testów**,
* **Pism urzędowych, wniosków grantowych i ofert handlowych**.

Dokument niesformatowany, ze skaczącymi czcionkami, pustymi linijkami i ręcznym spisem treści natychmiast dyskwalifikuje autora jako profesjonalistę. W tym poradniku poznasz reguły rzemiosła edytorskiego oparte na międzynarodowym standardzie ECDL oraz nowoczesne narzędzia pracy zespołowej w chmurze i asysty AI.

---

## 2. Żelazne Reguły Typografii i Edycji Tekstu (Standard ECDL)

### 2.1. Złota Zasada Klawisza ENTER
* **ENTER = NOWY AKAPIT:** Klawisz `Enter` naciskamy **wyłącznie** wtedy, gdy kończymy jedną myśl logiczną i zaczynamy zupełnie nowy akapit.
* **Zawijanie wierszy:** Gdy tekst dochodzi do prawego marginesu, procesor tekstu przenosi wyrazy automatycznie. Wciskanie Entera na końcu linijki w środku zdania to kardynalny błąd!
* **Miękki podział wiersza (`Shift + Enter`):** Jeśli w obrębie tego samego akapitu chcesz przejść do nowej linijki (np. w wersach wiersza lub danych adresowych firmy), użyj `Shift + Enter`.
* **Puste linijki to grzech:** Nigdy nie rób odstępów między akapitami wielokrotnym wciskaniem Entera. Używa się do tego parametru *Odstęp po akapicie* (np. 8-10 pt) w menu formatowania akapitu.

### 2.2. Usuwanie "Sierotek" – Twarda Spacja (Nierozdzielająca)
W języku polskim spójniki i przyimki jednoliterowe (*a, i, o, u, w, z*) nie powinny pozostawać na samym końcu linijki tekstu.
* Zamiast zwykłej spacji wstaw między spójnik a następujący wyraz **twardą spację**:
  * Skrót klawiszowy: `Ctrl + Shift + Spacja` (w Wordzie) lub `Ctrl + Shift + Spacja` / `Alt + Spacja` (w zależności od systemu i edytora).
  * Efekt: Wyraz i spójnik zostaną potraktowane jako nierozerwalna całość i przeniosą się razem do nowej linijki.

### 2.3. Włączanie Znaków Niewidocznych (¶)
Gdy coś "rozjeżdża się" w dokumencie, włącz podgląd znaków formatowania (ikona odwróconego P: `¶` na wstążce lub skrót `Ctrl + *`):
* Kropka na wysokości środka litery (`·`) = zwykła spacja,
* Symbol kółka stopnia (`°`) = twarda spacja,
* Symbol `¶` = znak końca akapitu (klawisz Enter),
* Zakrzywiona strzałka (`↵`) = miękki podział wiersza (`Shift + Enter`).
Dzięki temu natychmiast wykryjesz podwójne spacje, przypadkowe entery i błędy justowania.

### 2.4. Malarz Formatów (Kopiowanie Stylu)
Gdy sformatujesz fragment tekstu (np. określony kolor, pogrubienie i krój pisma):
1. Zaznacz sformatowany fragment.
2. Kliknij ikonę **Malarza formatów** (symbol pędzla lub wałka malarskiego):
   * *Pojedyncze kliknięcie:* pozwala skopiować styl na jedno zaznaczenie.
   * *Podwójne kliknięcie:* blokuje pędzel – możesz klikać kolejne fragmenty dokumentu, a narzędzie pozostaje aktywne, dopóki nie naciśniesz klawisza `Esc`.

---

## 3. Style Akapitowe i Automatyczny Spis Treści

### 3.1. Dlaczego ręczne powiększanie fontu to błąd?
Początkujący użytkownik tworzy nagłówek tak: zaznacza tekst, klika rozmiar `18 pt` i wciska pogrubienie (`Ctrl + B`). Dla procesora tekstu jest to nadal **zwykły tekst** o zmodyfikowanym wyglądzie. Taki dokument:
* Nie potrafi wygenerować automatycznego spisu treści,
* Nie jest dostępny dla czytników osób niewidomych (naruszenie standardu WCAG),
* Wymaga ręcznej poprawki w 40 miejscach, jeśli promotor lub szef zażąda zmiany czcionki nagłówków.

### 3.2. Hierarchia Stylów (Heading 1, 2, 3)
* **Tytuł (Title):** Nazwa główna dokumentu (używana tylko raz na pierwszej stronie).
* **Nagłówek 1 (Heading 1 / H1):** Główne działy (np. *1. Wprowadzenie*, *2. Analiza Rynku*, *3. Kosztorys*).
* **Nagłówek 2 (Heading 2 / H2):** Podrozdziały (np. *2.1. Konkurencja bezpośrednia*, *2.2. Grupa docelowa*).
* **Nagłówek 3 (Heading 3 / H3):** Drobniejsze sekcje szczegółowe.
* **Tekst zwykły (Normal):** Właściwa treść akapitów.

### 3.3. Błyskawiczna modyfikacja stylu
Chcesz, aby wszystkie Nagłówki 1 były ciemnoniebieskie, miały font Trebuchet MS i linię od dołu?
1. Sformatuj w ten sposób jeden nagłówek w dokumencie.
2. W panelu Stylów kliknij prawym przyciskiem myszy na **Nagłówek 1** (lub w menu rozwijanym stylów w Google Docs).
3. Wybierz opcję: **Zaktualizuj Nagłówek 1 zgodnie z zaznaczeniem** (*Update Heading 1 to match*).
4. Wszystkie nagłówki poziomu 1 w całym dokumencie zaktualizują się w ułamku sekundy!

### 3.4. Generowanie i Odświeżanie Spisu Treści
1. Ustaw kursor w miejscu, gdzie ma znaleźć się spis (zwykle strona 2).
2. Wybierz: **Wstawianie -> Spis treści** (wybierz wersję z numerami stron).
3. Program automatycznie zbierze wszystkie teksty ze stylami H1, H2, H3 i utworzy idealny spis z numeracją stron i kropkowanymi wiodącymi liniami.
4. **Zasada aktualizacji:** Jeśli po dopisaniu tekstu przesuną się strony, kliknij w obszar spisu treści i wybierz ikonę **Odśwież spis treści** (ikona obracającej się strzałki).

---

## 4. Architektura Dokumentu: Podziały, Stopki i Tabele

### 4.1. Podział Strony (`Ctrl + Enter`) vs Podziały Sekcji
* **Zwykły podział strony (`Ctrl + Enter`):** Wymusza rozpoczęcie nowego tekstu od kolejnej kartki, niezależnie od tego, ile dopiszesz powyżej.
* **Podział sekcji (Nowa strona):** Dzieli dokument na niezależne strefy geometryczne. Używaj go, gdy:
  * Chcesz, aby jedna strona z dużą tabelą była w orientacji poziomej (Landscape), a pozostałe w pionowej (Portrait).
  * Chcesz, aby strona tytułowa nie miała numeru strony, a numeracja 1 rozpoczęła się dopiero od spisu treści.

### 4.2. Profesjonalna Stopka i Numeracja Stron
1. Kliknij dwukrotnie w dolny margines dokumentu, aby wejść w tryb edycji stopki.
2. Zaznacz opcję: **Inne na pierwszej stronie** (dzięki temu strona tytułowa pozostanie czysta bez numeru).
3. Wstaw pole dynamiczne numeracji: **Wstaw -> Numer strony -> Strona X z Y**.
4. Wyrównaj numer do prawego marginesu, a po lewej stronie stopki wpisz nazwę dokumentu i wersję (np. `Brief Projektowy v1.0 | Poufne`).

### 4.3. Poprawne Formatowanie Tabel
Tabele w dokumentach technicznych i biznesowych muszą być przejrzyste:
* **Wiersz nagłówka:** Wyróżniony tłem (np. ciemnoszare lub granatowe) i białym lub pogrubionym tekstem.
* **Zasada wyrównania danych:**
  * Tekst, opisy i nazwy: Wyrównanie do lewej strony.
  * Liczby, daty, kwoty walutowe: Wyrównanie do prawej strony (ułatwia porównywanie rzędów wielkości!).
  * Krótkie symbole, statusy (np. `OK`, `[X]`): Wyrównanie do środka.
* **Nigdy nie dziel komórki na siłę:** Zamiast pustych spacji dostosuj szerokość kolumn klikając dwukrotnie na granicę kolumny (automatyczne dopasowanie do zawartości).

---

## 5. Praca Współbieżna w Chmurze (Google Docs / M365)

### 5.1. Tryby Pracy: Edycja a Sugerowanie
W prawym górnym rogu pod paskiem narzędzi znajduje się przełącznik trybów:
1. **Tryb edycji (Ołówek):** Twoje zmiany wchodzą natychmiast.
2. **Tryb sugerowania (Dymek / Ołówek z kreskami):** Odpowiednik mechanizmu *Track Changes* (Śledzenie zmian). Gdy coś dopiszesz, pojawi się zielonym kolorem; gdy coś skasujesz, tekst zostanie przekreślony. Autor dokumentu otrzymuje dymek z przyciskami `✓` (Zaakceptuj) oraz `✕` (Odrzuć).

### 5.2. Asynchroniczne Recenzje i Przypisywanie Zadań
Gdy współpracujesz z kolegą z zespołu:
1. Zaznacz wątpliwy akapit.
2. Kliknij ikonę **Dodaj komentarz** (`Ctrl + Alt + M`).
3. Wpisz `@` i wybierz adres kolegi, np. `@mateusz.nowak Zmień ten opis na bardziej konkretny – brakuje technologii`.
4. Zaznacz checkbox **Przypisz do użytkownika Mateusz Nowak**. Mateusz dostanie e-mail z powiadomieniem, a zadanie zniknie dopiero, gdy kliknie "Rozwiązane".

### 5.3. Historia Wersji: Wehikuł Czasu Dokumentu
* Wejdź w **Plik -> Historia wersji -> Wyświetl historię wersji** (`Ctrl + Alt + Shift + H`).
* W prawym panelu widzisz pełną listę zmian z dokładną datą, godziną i imieniem osoby edytującej.
* Każda osoba ma przypisany unikalny kolor podświetlenia tekstu.
* Możesz kliknąć trzy kropki przy dowolnej wersji i wybrać: **Nazwij tę wersję** (np. *Baza do konsultacji z klientem 15.10.2026*).
* W razie pomyłki lub skasowania kluczowych danych klikasz **Przywróć tę wersję**.

---

## 6. Wzorcowy Szablon: Brief Projektowy w IT
Oto oficjalna struktura briefu projektowego, który tworzy każdy profesjonalny Project Manager i analityk IT:

```
[LOGOTYP LUB NAZWA PROJEKTU]
TYTUŁ: Brief Projektowy: System Monitoringu Sprzętu Szkolnego
Wersja dokumentu: 1.0 | Data: 2026-10-15 | Autorzy: Zespół Inżynierski

--- PODZIAŁ STRONY ---
SPIS TREŚCI (Automatyczny)

--- PODZIAŁ STRONY ---
1. Executive Summary (Streszczenie Biznesowe)
[Jeden zwięzły akapit wyjaśniający czym jest projekt, komu ma służyć i jaką wartość wnosi].

2. Definicja Problemu i Grupa Docelowa
2.1. Aktualne wyzwania (As-Is)
[Opis obecnego stanu – np. chaos w zeszycie wypożyczeń laptopów w pracowni].
2.2. Profil użytkowników
[Kto będzie korzystał z systemu: nauczyciele, administratorzy pracowni, uczniowie].

3. Zakres Wymagań Funkcjonalnych (MVP)
[Lista kluczowych funkcjonalności, które muszą znaleźć się w pierwszej wersji]:
- Logowanie przez konto Google Workspace,
- Generowanie kodów QR na obudowy urządzeń,
- Moduł zgłaszania usterek technicznych.

4. Harmonogram i Kamienie Milowe (Tabela)
[Tabela z kolumnami: Faza, Zadanie, Odpowiedzialny, Termin oddania, Status].

5. Budżet i Wymagania Technologiczne
[Tabela kosztów oraz specyfikacja: baza w chmurze, hosting, licencje].

6. Kryteria Sukcesu i Oceny Końcowej
[Mierzalne wskaźniki KPI – np. skrócenie czasu inwentaryzacji z 4 dni do 2 godzin].
```

---

## 7. Przełom AI: Warsztat z Google NotebookLM

### 7.1. Dlaczego NotebookLM a nie ChatGPT?
Standardowy ChatGPT to model ogólny – uczył się na internecie, więc gdy pytasz go o wewnętrzny regulamin Twojej szkoły, zaczyna zmyślać (halucynuje).
**Google NotebookLM** działa na zasadzie **RAG (Retrieval-Augmented Generation)**:
* Nie szuka odpowiedzi w całym internecie, lecz **TYLKO w plikach, które sam do niego wgrałeś**.
* Przy każdej odpowiedzi generuje **odnośniki źródłowe (Cytowania `[1]`, `[2]`)**.
* Po kliknięciu w cytat, po lewej stronie ekranu podświetla się oryginalny dokument i dokładny akapit!

### 7.2. Procedura Krok po Kroku w NotebookLM
1. Wejdź na platformę: `https://notebooklm.google.com/` (zaloguj się kontem Google).
2. Kliknij **Nowy notatnik** (*New Notebook*).
3. **Dodaj źródła (Add sources):**
   * Możesz wgrać pliki PDF, dokumenty Google Docs, pliki tekstowe, linki do stron WWW, a nawet wkleić surowy tekst ze schowka.
4. **Przegląd źródeł:** NotebookLM wygeneruje automatyczne podsumowanie (*Source Guide*) każdego pliku wraz z proponowanymi pytaniami kluczowymi.
5. **Konwersacja z dokumentami:**
   * Wpisz zapytanie: `Wypisz w tabeli wszystkie kary dyscyplinarne przewidziane w statucie szkoły wraz z artykułami`.
   * AI wygeneruje precyzyjną tabelę i wskaże odsyłacze do konkretnych paragrafów.
6. **Przegląd Audio (Audio Overview - opcjonalnie):**
   * NotebookLM potrafi wygenerować 10-minutowy podcast w języku angielskim (Deep Dive), w którym dwóch syntetycznych ekspertów AI dyskutuje o Twoich notatkach!

### 7.3. Etyka i Bezpieczeństwo Danych w AI
* Nigdy nie wgrywaj do publicznych narzędzi AI danych osobowych kolegów (PESEL, adresy zamieszkania, hasła).
* Pamiętaj: Nawet najbardziej zaawansowane AI jest tylko kalkulatorem słów – ostateczna odpowiedzialność prawna i merytoryczna za treść dokumentu spoczywa na autorze podpisanym pod plikiem!
