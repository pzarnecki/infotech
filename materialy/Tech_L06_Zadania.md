# 📋 Zoperacjonalizowana Karta Zadań: Inżynieria Dokumentacji Technicznej i Docs-as-Code
## Przedmiot: Informatyka Zawodowa / Programowanie | Klasa: Technikum Informatyczne / Programistyczne
**Autor:** Przemysław Żarnecki • Standard INFOTECH / DevOps & Software Engineering  
**Forma oddania:** Plik `README.md` / Link do repozytorium GitHub + Wypełniony Formularz w Google Classroom

---

## 🎯 Cele Operacyjne (Co będziesz potrafił po tej lekcji?):
1. Przekształcać nieprecyzyjne, biznesowe życzenia klienta w formalne **User Stories** zgodnie ze standardem zwinnego zarządzania projektami (Agile/Scrum).
2. Tworzyć rygorystyczne **Kryteria Akceptacji (Acceptance Criteria)** w konwencji BDD / Gherkin (**Given-When-Then**).
3. Samodzielnie napisać produkcyjny plik **`README.md`** w standardzie GitHub Flavored Markdown (GFM) z tarczami Shields.io, blokami kodu, tabelami i checklistami zadań.
4. Przeprowadzać inżynierski przegląd dokumentacji technicznej (**Code Review**) w poszukiwaniu błędów składniowych i architektonicznych.
5. Zastosować narzędzie **Google NotebookLM** do uziemionej analizy specyfikacji technicznej z weryfikacją cytowań źródłowych `[1]`.

---

## 🛠️ ZADANIE 1 (Inżynieria Wymagań): Refaktoryzacja do User Stories i BDD
Poniżej znajdują się 3 autentyczne, chaotyczne notatki z rozmowy z klientem zamawiającym system informatyczny dla szkoły/uczelni.  
Przekształć każdą z nich w:
1. **Oficjalne User Story:** `Jako [rola], chcę [działanie], aby [wartość biznesowa]`.
2. **Kryteria Akceptacji (Given-When-Then):** Wypisz co najmniej 1 scenariusz pozytywny (Success path) oraz 1 scenariusz błędu / obsługi wyjątku (Failure path).

### Opisy wejściowe klienta:
* **Wymaganie A (Moduł ocen i powiadomień):**  
  *„Rodzice skarżą się, że dowiadują się o jedynkach na koniec semestru. Chcemy, żeby rodzic dostawał natychmiast powiadomienie push na telefon, jak tylko nauczyciel wpisze ocenę niedostateczną do dziennika.”*
* **Wymaganie B (Eksport danych dla dyrekcji):**  
  *„Dyrektor musi co miesiąc składać raport do kuratorium o frekwencji. Teraz sekretarka siedzi nad tym 3 dni. Chcemy przycisk w panelu dyrektora, który wygeneruje plik Excel/CSV ze statystykami obecności dla wszystkich klas za wybrany miesiąc.”*
* **Wymaganie C (Ochrona przed atakami Brute-Force):**  
  *„Ostatnio jacyś dowcipnisie próbowali odgadnąć hasło do konta administratora. Zróbcie tak, żeby po 5 błędnych próbach hasła konto się blokowało na pół godziny i żeby admin dostawał maila z ostrzeżeniem.”*

---

## 🛠️ ZADANIE 2 (Warsztat Docs-as-Code): Produkcyjny Plik README.md
Stwórz plik o nazwie `README.md` w formacie czystego Markdown (GFM) dla projektu programistycznego o nazwie **`NetGuard-CLI`** (narzędzie konsolowe w Pythonie/Node do audytu portów sieciowych i certyfikatów SSL).

### Rygorystyczne wymagania strukturalne Markdown:
1. **Nagłówek i Tarcze:**
   * Tytuł H1 z ikoną.
   * Co najmniej 2 tarcze (badges) z serwisu shields.io (np. wersja, licencja, status testów).
2. **Elevator Pitch:**
   * Precyzyjny opis w 1-2 zdaniach, do czego służy program (bez lania wody!).
3. **Wymagania wstępne (Prerequisites):**
   * Lista punktowana narzędzi (np. `Python >= 3.10`, `Git`, dostęp do uprawnień administratora).
4. **Szybki start (Quickstart / Installation):**
   * Blok kodu `bash` zawierający sekwencję komend: klonowanie repozytorium, instalacja środowiska wirtualnego / modułów oraz pierwsze uruchomienie.
5. **Tabela Konfiguracji Zmiennych Środowiskowych (`.env`):**
   * Tabela GFM z poprawnym wyrównaniem kolumn:
     `| Zmienna | Typ | Domyślna | Wymagana? | Opis |`
   * Musi zawierać przynajmniej 3 zmienne (np. `SCAN_TIMEOUT`, `ALERT_WEBHOOK_URL`, `LOG_LEVEL`).
6. **Przykład Użycia z Wynikiem JSON:**
   * Blok kodu `bash` z komendą skanowania oraz blok kodu `json` pokazujący przykładowy wynik zwrócony przez program.
7. **Checklista Rozwojowa (Roadmap):**
   * Lista zadań z checkboxami: przynajmniej 2 ukończone (`- [x]`) i 2 planowane (`- [ ]`).

---

## 🛠️ ZADANIE 3 (Code Review i Google NotebookLM)

### Część A: Code Review Markdowna
W kodzie Markdown nadesłanym przez młodszego stażystę wkradły się błędy. Wskaż w formularzu odpowiedzi, co jest nie tak i jak powinno wyglądać poprawnie:
```markdown
#2 Specyfikacja Modułu
Link do dokumentacji: (Sprawdź tutaj)[https://docs.infotech.edu.pl]
Oto kod uruchomienia:
'python start.py'
```

### Część B: Uziemiona Analiza w Google NotebookLM
1. Otwórz `https://notebooklm.google.com/`.
2. Utwórz notatnik o nazwie `Inżynieria Wymagań Tech`.
3. Wgraj plik `Tech_L06_Tutorial.md` (lub treść sekcji 4 tego tutoriala o User Stories i BDD).
4. Zadaj w NotebookLM pytanie:  
   *`Jakie elementy składają się na składnię Given-When-Then i dlaczego samo User Story nie wystarcza programistom? Wskaż numery cytowań.`*
5. Skopiuj odpowiedź wraz z numerami odnośników źródłowych `[1]` i wklej do formularza.

---

## 📊 KRYTERIA OCENY (NaCoBeZu):
* **Ocena Dostateczna (3):**
  * Poprawne sformułowanie 3 User Stories w szablonie `Jako... chcę... aby...`.
  * Utworzenie podstawowego pliku `README.md` z nagłówkiem i blokiem kodu.
* **Ocena Dobra (4):**
  * Spełnienie kryteriów na 3.
  * Opracowanie kryteriów akceptacji Given-When-Then dla wszystkich 3 zadań.
  * Kompletny plik `README.md` zawierający tabelę zmiennych `.env` oraz instrukcję instalacji.
  * Bezbłędne wskazanie błędów w zadaniu Code Review Markdowna.
* **Ocena Bardzo Dobra (5):**
  * Spełnienie kryteriów na 4.
  * Profesjonalna jakość `README.md`: tarcze Shields.io, składnia GFM z formatowaniem JSON i bash, checklista zadań `- [x]`.
  * Wzorcowa inżynieria wymagań BDD (uwzględnienie kodów HTTP, limitów czasowych i komunikatów o błędach w Given-When-Then).
  * Przeprowadzenie analizy w Google NotebookLM z odnotowaniem odsyłaczy źródłowych `[1]`.
* **Ocena Celująca (6):**
  * Spełnienie kryteriów na 5.
  * Umieszczenie pliku `README.md` w publicznym repozytorium GitHub z poprawnie wyrenderowanym podglądem i diagramem architektury w składni Mermaid (````mermaid flowchart LR ... ````).
  * Dołączenie analizy porównawczej: dlaczego specyfikacje w BDD zapobiegają błędom regresji w testach automatycznych (pytest / jest).

---

## 📝 FORMULARZ ODPOWIEDZI UCZNIA
*(Skopiuj poniższy blok, wypełnij go i wklej w polu odpowiedzi do zadania w Google Classroom)*

```markdown
==================================================================
📋 FORMULARZ ODPOWIEDZI: LEKCJA 06 (TECH) – DOCS-AS-CODE & BDD
==================================================================
Imię i Nazwisko: [WPISZ TUTAJ]
Klasa: [WPISZ KLASĘ, NP. 1P TECHNIKUM]
Data wykonania: [DATA]

1. REFAKTORYZACJA WYMAGAŃ (USER STORIES & GIVEN-WHEN-THEN):

   a) Wymaganie A (Moduł ocen i powiadomień):
      - User Story: Jako [rola], chcę [działanie], aby [wartość biznesowa].
      - Kryterium Sukcesu (Given-When-Then):
        * Given: ...
        * When: ...
        * Then: ...
      - Kryterium Błędu / Wyjątku (Given-When-Then):
        * Given: ...
        * When: ...
        * Then: ...

   b) Wymaganie B (Eksport danych dla dyrekcji):
      - User Story: Jako [rola], chcę [działanie], aby [wartość biznesowa].
      - Kryteria Akceptacji (Given-When-Then):
        * Given: ...
        * When: ...
        * Then: ...

   c) Wymaganie C (Ochrona przed atakami Brute-Force):
      - User Story: Jako [rola], chcę [działanie], aby [wartość biznesowa].
      - Kryteria Akceptacji (Given-When-Then):
        * Given: ...
        * When: ...
        * Then: ...

2. REPOZYTORIUM / KOD PLIKU README.MD:
   Link do repozytorium GitHub (lub GitHub Gist): [WKLEJ LINK]
   (LUB wklej poniżej pełną zawartość swojego pliku README.md w Markdownie):
   ---------------------------------------------------------------
   [TUTAJ WKLEJ TREŚĆ TWOJEGO README.MD]
   ---------------------------------------------------------------

3. AUDYT CODE REVIEW (POPRAWA BŁĘDÓW W MARKDOWN):
   a) Błąd nagłówka (#2) – jak powinien wyglądać poprawny zapis?:
      Odpowiedź: [WYJAŚNIENIE I POPRAWKA]
   b) Błąd linku ((Sprawdź tutaj)[url]) – jak poprawnie zamknąć nawiasy?:
      Odpowiedź: [WYJAŚNIENIE I POPRAWKA]
   c) Błąd bloku kodu ('python start.py') – jakich znaków należy użyć?:
      Odpowiedź: [WYJAŚNIENIE I POPRAWKA]

4. RAPORT Z GOOGLE NOTEBOOKLM:
   a) Wklej odpowiedź NotebookLM z numerami cytowań źródłowych [1]:
      [WKLEJ ODPOWIEDŹ]
   b) Jakie korzyści daje programiście funkcja uziemionych cytowań (Grounding) przy wdrażaniu nowej specyfikacji?:
      Odpowiedź: [TWÓJ KOMENTARZ INŻYNIERSKI]
==================================================================
```
