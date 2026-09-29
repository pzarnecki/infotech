# Lekcja 06: Procesor Tekstu, Chmura i Asystenci AI w Dokumentacji Projektowej
## Ścieżka: Liceum Ogólnokształcące | Przedmiot: Informatyka (TIK)
**Autor:** Przemysław Żarnecki • Standard INFOTECH / ECDL Module B3

---

## Slajd 1: Od Maszynopisu do Dokumentu Chmurowego
* **Koniec ery pliku lokalnego:** Wysyłanie załączników `projekt_v2_ostateczny_FINAL3.docx` to gwarancja chaosu, utraty danych i konfliktów wersji.
* **Nowy paradygmat pracy:** Edytor tekstu (Google Docs, Microsoft 365) stał się środowiskiem współbieżnym, działającym w czasie rzeczywistym.
* **Trzy filary nowoczesnego edytora:**
  1. *Struktura logiczna* (Style, automatyczny spis treści, standaryzacja typograficzna).
  2. *Współpraca synchroniczna* (Komentarze, wzmianki `@`, tryb sugerowania zmian).
  3. *Uziemiona Inteligencja (Grounded AI)* (Google NotebookLM do analizy źródeł bez halucynacji).

---

## Slajd 2: Złote Zasady Typografii i Edytorstwa (Standard ECDL)
* **Zasada 1: Enter to NIE nowa linia!**
  * Klawisz `Enter` służy **wyłącznie** do tworzenia nowego akapitu (nowej myśli logicznej).
  * Do łamania wiersza wewnątrz tego samego akapitu służy miękki podział: `Shift + Enter`.
* **Zasada 2: Zero pustych linijek!**
  * Odstępy między akapitami ustawiamy w menu formatowania akapitu (*Odstęp przed* i *Odstęp po*), a nie wielokrotnym wciskaniem klawisza Enter.
* **Zasada 3: Twarda spacja (Nierozdzielająca):**
  * Spójniki i przyimki jednoliterowe (*w, z, i, o, a, u*) nie mogą wisieć na końcu wiersza (tzw. "sierotki").
  * Stosujemy skrót: `Ctrl + Shift + Spacja`.

---

## Slajd 3: Dlaczego "Pogrubienie i Rozmiar 16" to Błąd?
* **Problem formatowania ręcznego (ad-hoc):**
  * Ręcznie zmieniony font i rozmiar wyglądają jak nagłówek tylko dla ludzkiego oka.
  * Komputer, robot wyszukiwarki i czytnik osób niewidomych (WCAG) widzą to jako zwykły tekst!
* **Potęga Stylów Akapitowych (ECDL B3):**
  * **Tytuł (Title):** Nazwa całego dokumentu.
  * **Nagłówek 1 (Heading 1 / H1):** Główne rozdziały dokumentu.
  * **Nagłówek 2 (Heading 2 / H2):** Podsekcje wewnątrz rozdziałów.
  * **Zwykły tekst (Normal):** Treść merytoryczna akapitów.
* **Magia spójności:** Zmiana definicji stylu *Nagłówek 1* (np. na kolor granatowy) natychmiast aktualizuje cały, nawet 200-stronicowy dokument!

---

## Slajd 4: Automatyzacja: Spis Treści i Konspekt
* **Automatyczny Spis Treści (Table of Contents):**
  * Generowany jednym kliknięciem na podstawie zdefiniowanych stylów H1, H2, H3.
  * Każda pozycja w spisie jest aktywnym hiperłączem do odpowiedniego fragmentu tekstu.
  * Po edycji dokumentu wystarczy kliknąć przycisk **Odśwież spis treści** – numery stron aktualizują się same.
* **Panel nawigacji (Konspekt):**
  * Boczny panel w Google Docs / MS Word pozwala na natychmiastowe przeskakiwanie między sekcjami oraz przeciąganie całych rozdziałów metodą "drag & drop".

---

## Slajd 5: Architektura Strony i Podziały (Sekcje a Strony)
* **Koniec z wciskaniem Entera 30 razy!**
  * Aby rozpocząć nowy rozdział na nowej kartce, wstawiamy **Podział strony** (`Ctrl + Enter`).
* **Podziały sekcji (Sekcja następna / Sekcja ciągła):**
  * Pozwalają na stosowanie różnych układów w jednym dokumencie:
    * Strona 1-2: Pionowa (tekst wstępu).
    * Strona 3: Pozioma (szeroka tabela harmonogramu projektu lub wykres).
    * Strona 4: Znowu pionowa.
  * Pozwalają na brak numeru strony na karcie tytułowej i rozpoczęcie numeracji od strony drugiej.

---

## Slajd 6: Nagłówek, Stopka i Precyzyjne Tabele
* **Nagłówek i Stopka (Header & Footer):**
  * Treści powtarzające się na każdej stronie (tytuł projektu, autor, data).
  * Dynamiczne pole numeracji: `Strona X z Y` (automatycznie przeliczana łączna liczba stron).
* **Profesjonalne Tabele (Zasady czytelności):**
  * Wyraźnie wyróżniony pierwszy wiersz (Nagłówek tabeli – pogrubienie, tło).
  * Opcja "Powtórz wiersz nagłówka na każdej nowej stronie" przy tabelach wielostronicowych.
  * Wyrównanie: Tekst do lewej, liczby i kwoty finansowe do prawej (ułatwia porównywanie rzędów wielkości!).

---

## Slajd 7: Praca Zespołowa w Chmurze (Google Docs / M365)
* **Trzy tryby dostępu:**
  1. *Edycja:* Bezpośrednie wprowadzanie zmian.
  2. *Sugerowanie (Tryb Recenzji / Track Changes):* Każda usunięta lub dopisana litera jest oznaczona kolorem i wymaga akceptacji właściciela dokumentu.
  3. *Przeglądanie:* Bezpieczny podgląd tylko do odczytu.
* **Komentarze i delegowanie zadań:**
  * Zaznacz fragment tekstu -> Dodaj komentarz -> Wpisz `@jan.kowalski Sprawdź te wyliczenia budżetowe`.
  * Google Docs wyśle e-mail z powiadomieniem i przypisze zadanie!

---

## Slajd 8: Bezpieczeństwo i Audyt: Historia Wersji
* **Mit utraconego dokumentu:** W chmurze nie ma przycisku "Zapisz" – zapis następuje po każdym naciśnięciu klawisza.
* **Panel Historii Wersji (`Plik -> Historia wersji`):**
  * Rejestracja kto, kiedy i jakie słowo zmienił (kodowanie kolorami autorów).
  * Możliwość cofnięcia całego dokumentu do stanu sprzed 10 minut, wczoraj lub z zeszłego tygodnia.
* **Nazwane wersje dokumentu:**
  * Zamiast tworzyć kopie plików na dysku, nadajemy etykiety w historii: *"Wersja 1.0 - Złożona do Klienta"*, *"Wersja 1.1 - Po uwagach dyrekcji"*.

---

## Slajd 9: Czym jest Brief Projektowy w Branży IT?
* **Definicja:** Zwięzły dokument strategiczny (1-3 strony), który definiuje cele, ramy i zakres projektu cyfrowego zanim programiści napiszą pierwszą linijkę kodu.
* **Kluczowa struktura Briefu:**
  1. **Executive Summary:** Kim jesteśmy i co chcemy zbudować w jednym akapicie.
  2. **Problem i Grupa Docelowa:** Jaki realny problem użytkowników rozwiązujemy?
  3. **Wymagania Funkcjonalne:** Lista kluczowych funkcji systemu (MVP - Minimum Viable Product).
  4. **Harmonogram i Role:** Kto odpowiada za projekt i jakie są kamienie milowe (Milestones).
  5. **Kryteria Sukcesu:** Skąd będziemy wiedzieć, że projekt się udał? (np. 500 aktywnych uczniów).

---

## Slajd 10: Przełom AI: Google NotebookLM a ChatGPT
* **Dlaczego standardowy ChatGPT zawodzi przy dokumentacji?**
  * Halucynacje: Zmyśla fakty, gdy nie zna odpowiedzi.
  * Brak uziemienia (Grounding): Nie zna specyfiki Twojej szkoły ani wewnętrznych regulaminów.
* **Jak działa Google NotebookLM?**
  * Zasilasz go **Twoimi własnymi źródłami** (PDF, pliki Docs, notatki, linki www).
  * AI odpowiada **wyłącznie na podstawie dostarczonych dokumentów**.
  * **Interaktywne cytowania:** Każde zdanie wygenerowane przez NotebookLM ma przypis w nawiasie `[1]`, który po kliknięciu podświetla dokładny akapit w pliku źródłowym!
* **Zastosowanie:** Błyskawiczna analiza 50-stronicowych specyfikacji, wyciąganie krytycznych wniosków, tworzenie FAQ dla klientów.

---

## Slajd 11: Podsumowanie i Standardy Branżowe
* **Higiena edytorska:**
  * Używaj stylów nagłówków – bez nich dokument jest tylko cyfrowym brudnopisem.
  * Zawsze wstawiaj automatyczny spis treści w dokumentach dłuższych niż 3 strony.
  * Korzystaj z historii wersji i trybu sugerowania zamiast przesyłać załączniki mailowe.
* **Etyka i rzetelność AI:**
  * Sztuczna inteligencja to Twój asystent redakcyjny, nie autor.
  * Weryfikuj źródła – za błędy merytoryczne w dokumentacji zawsze odpowiada człowiek.
