# Lekcja 06: Inżynieria Dokumentacji Technicznej: Docs-as-Code, Markdown, User Stories i NotebookLM
## Ścieżka: Technikum Programistyczne / Informatyczne (Rozszerzenie Zawodowe)
**Autor:** Przemysław Żarnecki • Standard INFOTECH / DevOps & Software Engineering

---

## Slajd 1: Inżynieria Dokumentacji: Paradygmat "Docs-as-Code"
* **Koniec plików `.docx` w repozytoriach programistycznych:**
  * Pliki binarne Worda uniemożliwiają czytelne śledzenie zmian w Git (`git diff` nie działa na plikach docx).
  * Niemożliwe jest automatyczne testowanie dokumentacji w potokach CI/CD.
* **Filozofia Docs-as-Code (Dokumentacja jako Kod):**
  * Dokumentacja jest pisana w czystym tekście (Markdown, AsciiDoc).
  * Jest przechowywana w tym samym repozytorium co kod źródłowy aplikacji.
  * Przechodzi przez ten sam cykl życia: gałęzie Git, Pull Requesty, Code Review i automatyczne wdrażanie.

---

## Slajd 2: Składnia Markdown i GFM (GitHub Flavored Markdown)
* **Czysty tekst o wielkich możliwościach:**
  * Tworzony w dowolnym edytorze kodu (VS Code, Vim, Neovim) bez odrywania rąk od klawiatury.
* **Kluczowe elementy składni deweloperskiej:**
  * **Hierarchia:** `# H1`, `## H2`, `### H3`.
  * **Bloki kodu z syntax highlighting:** Trzy grawisy i nazwa języka:
    ````markdown
    ```bash
    npm install && npm run dev
    ```
    ````
  * **Tabele danych i konfiguracji:**
    `| Zmienna ENV | Typ | Wartość domyślna | Opis |`
  * **Checklisty zadań (Task Lists):** `- [x] Autoryzacja JWT` / `- [ ] Testy jednostkowe`.

---

## Slajd 3: Anatomia Produkcyjnego Pliku README.md
* **README.md to wizytówka i "drzwi wejściowe" do Twojego projektu:**
  * Projekt bez README jest uważany w branży za martwy lub porzucony.
* **Obowiązkowe sekcje profesjonalnego README:**
  1. **Header & Badges:** Nazwa projektu, badges (status builda CI, wersja v1.2, licencja MIT).
  2. **Elevator Pitch:** Jednozdaniowy, bezwzględnie konkretny opis problemu, który rozwiązuje system.
  3. **Wymagania wstępne (Prerequisites):** Wersje środowisk (np. `Node.js >= 20.x`, `PostgreSQL 16`).
  4. **Szybki start (Quickstart):** Krok po kroku: klonowanie, konfiguracja zmiennych `.env`, migracje bazy i uruchomienie.
  5. **Architektura / Endpointy:** Tabela kluczowych tras API lub schemat Mermaid.
  6. **Konfiguracja środowiskowa:** Tabela wszystkich zmiennych z pliku `.env.example`.
  7. **Licencja i Kontrybucja:** Zasady zgłaszania PR i licencja Open Source.

---

## Slajd 4: Inżynieria Wymagań: Zwinne User Stories (Agile / Scrum)
* **Dlaczego chaotyczne maile od klienta niszczą projekty?**
  * *"Chcemy, żeby system był intuicyjny i szybko się logował"* – to nie jest wymóg techniczny.
* **Międzynarodowy standard User Story:**
  > **Jako** [konkretna rola / persona użytkownika],  
  > **Chcę** [wykonać precyzyjną akcję w systemie],  
  > **Aby** [osiągnąć mierzalną wartość biznesową].
* **Kryteria Akceptacji (Acceptance Criteria - BDD / Gherkin):**
  * **Zakładając, że (Given):** Użytkownik znajduje się na ekranie logowania i wprowadził błędne hasło 3 razy.
  * **Kiedy (When):** Klika przycisk "Zaloguj się".
  * **Wtedy (Then):** Konto zostaje tymczasowo zablokowane na 15 minut, a na ekranie pojawia się komunikat o kodzie HTTP 429.

---

## Slajd 5: Praca Zespołowa: Code Review i Audyt Dokumentacji
* **Przegląd dokumentacji (Documentation Review):**
  * Zanim funkcja wejdzie do produkcji, dokumentacja jest sprawdzana przez innych programistów w ramach Pull Requesta na GitHubie.
  * W dyskusjach używa się komentarzy *inline* odwołujących się do konkretnych linijek kodu lub Markdowna.
* **Śledzenie zmian i standaryzacja CHANGELOG.md:**
  * Stosowanie konwencji *Keep a Changelog* oraz *Semantic Versioning (SemVer)*: `MAJOR.MINOR.PATCH` (np. `v2.4.1`).
  * Podział na sekcje: `Added`, `Changed`, `Deprecated`, `Removed`, `Fixed`, `Security`.

---

## Slajd 6: AI dla Inżyniera: Google NotebookLM i Specyfikacje Techniczne
* **Rola Technical Writera w dobie AI:**
  * Dzisiejszy inżynier nie pisze schematów od zera – wykorzystuje asystentów AI do syntezy i weryfikacji.
* **Przewaga Google NotebookLM nad standardowym ChatGPT:**
  * Wgrywasz do NotebookLM: 150-stronicową specyfikację protokołu RFC, schemat bazy SQL oraz wyciąg z logów błędów.
  * NotebookLM buduje bazę wiedzy **uziemioną w Twoich plikach (Grounded RAG)**.
  * Zapewnia **interaktywne odsyłacze źródłowe `[1]`** – programista natychmiast widzi, z którego paragrafu dokumentacji wynika dane ograniczenie pamięciowe czy wymóg szyfrowania TLS.

---

## Slajd 7: Podsumowanie Zasad Inżynierskich
* **Zasada DRY (Don't Repeat Yourself):** Nie twórz trzech różnych opisów tego samego API – generuj dokumentację ze specyfikacji OpenAPI (Swagger) i plików Markdown.
* **Atomic Commits:** Zmiana w kodzie i odpowiadająca jej aktualizacja w `README.md` muszą iść w **tym samym commicie**.
* **Język precyzji:** W dokumentacji technicznej nie ma miejsca na słowa *"prawdopodobnie"*, *"dosyć szybko"*, *"ładny interfejs"*. Liczą się kody błędów, milisekundy, formaty JSON i kryteria akceptacji.
