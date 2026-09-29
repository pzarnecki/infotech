# Koncepcja Dydaktyczna: Informatyka w INFOTECH (Poziom Podstawowy)

Rozkład materiału został zaprojektowany z myślą o uczniach Liceum INFOTECH. Pamiętając o sztywnych ramach **polskiej podstawy programowej**, plan realizuje wszystkie jej punkty (w tym pakiety biurowe, prawo, relacyjne bazy danych i bezpieczeństwo), ale ubiera je w **nowoczesny, rynkowy kontekst IT**.

### Jak realizujemy wymogi podstawy programowej w duchu technologicznym?
1. **Pakiety biurowe i Notatniki AI:** Używamy ich jako narzędzi pracy projektowej. Do specyfikacji używamy m.in. **Google NotebookLM** i Docs, arkusz służy do analizy "brudnych" danych, a program do prezentacji uczy tworzenia "Pitch Decków". 
2. **Relacyjne Bazy Danych:** Zamiast przestarzałego MS Accessa, wprowadzamy relacyjne bazy za pomocą języka SQL (SQLite), co łączy się z tematami backendowymi.
3. **Cyberbezpieczeństwo jako fundament:** Dla ucznia liceum kluczowa jest świadomość zagrożeń. W kl. 1 realizujemy higienę cyfrową i phishing, w kl. 2 rozbudowany moduł o wyciekach danych, hashowaniu oraz bezpieczeństwie webowym (SQL Injection, XSS).
4. **Praktyka i Technologie rynkowe:** Python uruchamiany w **Google Colab** dla klasy 1. W klasie 2 wchodzimy w WebDev (HTML/CSS/JS) wraz z koncepcyjną ciekawostką o bezpieczeństwie języków (Rust).
5. **AI jako Asystent:** Systematyczne używanie LLM jako asystenta programisty.
6. **Twój Autorski Portal jako środowisko nauki:** Twój system pełni rolę repozytorium prac (LMS) w 1 klasie oraz "żywego" backendu (API) w 2 klasie.

---

## KLASA 1: Podstawy IT, Analityka i Programowanie w Pythonie (30 godzin)

**Cel:** Realizacja podstawowych wymogów obsługi komputera w kontekście branży IT oraz nauka algorytmiki i programowania skryptowego.

| Nr | Temat zajęć | Odniesienie do podstawy (LO podst.) | Praktyczne aktywności | Narzędzia |
|:---:|---|---|---|---|
| **1** | Wstęp. Kultura środowiska IT i środowisko pracy (Cloud). | V.2 (Ergonomia pracy) | Wprowadzenie do notatników chmurowych bez lokalnej konfiguracji. | **Google Colab** |
| **2-3** | **Cyberbezpieczeństwo:** Higiena cyfrowa, 2FA, hasła i Social Engineering. | III.3, V.1 (Bezpieczeństwo) | Rozpoznawanie phishingu, weryfikacja incydentów w sieci, menedżery haseł. | Przeglądarka |
| **4-5** | **Prawo w IT:** Licencje Open Source, prawa autorskie i etyka AI. | V.1, V.4 (Prawo autorskie) | Jak legalnie używać kodu z GitHuba? Co oznacza licencja MIT/GPL? | GitHub, AI |
| **6** | **Procesor tekstu i AI w IT:** Dokumentacja projektowa. | III.1 (Procesor tekstu) | Formatowanie specyfikacji i syntetyzowanie obszernych źródeł z AI. | Docs, **NotebookLM** |
| **7-8** | **Arkusz kalkulacyjny:** Narzędzie analityka danych przed napisaniem skryptu. | III.1 (Arkusz kalkulacyjny) | Obróbka "brudnych" danych (np. logów sieciowych): filtrowanie, wykresy. | Excel / Google Sheets |
| **9** | **Prezentacje:** Sztuka tworzenia technologicznego "Pitch Decku". | III.1 (Tworzenie prezentacji) | Reguły prezentacji własnego pomysłu biznesowego przed klientem. | PowerPoint / Slides |
| **10** | Prompt Engineering: LLM jako wirtualny asystent. | V.3 (Wiarygodność) | Budowa system promptów, tłumaczenie pojęć technicznych z AI. | LLM (ChatGPT/Claude) |
| **11** | Reprezentacja informacji: Binarny i HEX. Kody ASCII i Unicode. | I.1 (Reprezentowanie danych) | Jak komputer widzi tekst i liczby? Przeliczanie systemów liczbowych. | Tablica, AI |
| **12** | Algorytmika klasyczna: Wyszukiwanie (binarne) i Sortowanie. | I.2 (Projektowanie algorytmów) | Rozwiązywanie problemów analitycznych krok po kroku (bez kodu). | Tablica |
| **13-14** | Zmienne i operatory w Pythonie ("Hello World"). | II.1 (Implementacja) | Pisanie pierwszych skryptów (kalkulatory, operacje na tekstach). | Python, **Google Colab** |
| **15-16** | Instrukcje warunkowe (if/else) – decyzyjność w kodzie. | II.1 (Podejmowanie decyzji) | Logika biznesowa i sprawdzanie warunków (np. symulator logowania). | Python, Colab |
| **17-18** | Automatyzacja powtarzalnych zadań: Pętle (for, while). | II.1 (Iteracje) | Skrypty przetwarzające pakiety danych. | Python, Colab |
| **19-20** | Złożone struktury danych: Listy w analizie informacji. | II.1 (Tablice/listy) | Agregacja wyników w pamięci programu. | Python, Colab |
| **21-22** | Funkcje i modułowość. Debugowanie z LLM. | II.1, II.2 (Funkcje, Testy) | Szukanie błędów z AI. Wyjaśnianie wyjątków (Error handling). | Python, LLM |
| **23-24** | Współpraca Arkusza z kodem: Odczyt CSV w Pythonie. | II.1 (Operacje na plikach) | Programistyczna obróbka pliku ze starszych zajęć w arkuszu. | Python, Colab |
| **25** | **Wprowadzenie do Twojego Portalu Edukacyjno-Zadaniowego.** | I.1, IV.1 (Praca z aplikacjami) | Logowanie do systemu, pobieranie zadań, system oddawania kodu. | **Twój Portal (LMS)** |
| **26-28** | *Projekt (Gr)*: Rozwiązywanie problemów biznesowych (Python). | II.1, IV.1 (Zarządzanie) | Skrypty rozwiązujące konkretne case'y. Kod oddawany przez Twój portal. | Python, Twój Portal |
| **29-30** | Demo Day & AI Code Review. | IV.3, II.2 (Prezentacja, ocena) | Zespoły prezentują zadania. Przegląd rozwiązań za pośrednictwem platformy. | Twój Portal, Rzutnik |

---

## KLASA 2: Technologie Webowe, Bezpieczeństwo i Architektura (30 godzin)

**Cel:** Zrozumienie weba (front & back), baz danych, świadomość cyber-zagrożeń oraz kontynuacja pracy w Twoim portalu (tym razem jako API/Backend).

| Nr | Temat zajęć | Odniesienie do podstawy (LO podst.) | Praktyczne aktywności | Narzędzia |
|:---:|---|---|---|---|
| **1-2** | Architektura Internetu (HTTP, DNS, Klient-Serwer). | III.2 (Sieci komputerowe) | Analiza ruchu w DevTools, cykl życia zapytania. | DevTools |
| **3-4** | Podstawy HTML5: Budowa semantycznego interfejsu. | II.1, III.1 (Tworzenie witryn) | Znaczniki odpowiedzialne za układ, znaczenie dostępności. | HTML |
| **5-7** | CSS3 (Flexbox/Grid): Estetyka i układ współczesnych aplikacji. | II.1, III.1 (Stylowanie) | Tworzenie responsywnego (RWD) interfejsu. | CSS |
| **8** | AI w pracy Frontendowca. | V.3 (Rozwój przy pomocy AI) | Weryfikacja stylów i debugowanie błędów layoutu z LLM. | HTML/CSS, LLM |
| **9-11** | JavaScript (ES6+): Ożywianie interfejsu przeglądarki (DOM). | II.1 (Skrypty po stronie klienta) | Interaktywność, podpinanie logiki pod akcje użytkownika. | JS |
| **12-13** | JS i komunikacja sieciowa: Fetch API (format JSON). | III.2, II.1 (Usługi sieciowe) | Pobieranie zewnętrznych danych asynchronicznie (bez przeładowania). | JS |
| **14-15** | **Relacyjne Bazy Danych:** Język SQL (SELECT, JOIN). | III.1 (Bazy, relacje) | Projektowanie 2 połączonych tabel i wyciąganie z nich danych. | DB Fiddle / SQLite |
| **16** | **RUST i C/C++:** Dlaczego sprzęt ma "dziury"? | V.1, III.3 (Bezpieczeństwo OS) | Wykład/Ciekawostka: Koncepcje bezpieczeństwa pamięci. Dlaczego powstają nowe języki? | Prezentacja |
| **17** | **Cyberbezpieczeństwo:** Twoje dane. Wycieki i hashowanie. | III.3 (Prywatność, szyfrowanie) | OSINT (HaveIBeenPwned). Dlaczego bazy nie trzymają haseł jawnym tekstem? Metody hashowania (np. bCrypt). | Przeglądarka |
| **18** | **Cyberbezpieczeństwo:** Ataki na bazy danych (SQL Injection). | III.3 (Zagrożenia sieciowe) | Praktyczna próba "włamania" do spreparowanego formularza z użyciem surowego SQL'a. | SQL, LLM |
| **19** | **Cyberbezpieczeństwo:** Ataki na przeglądarkę (XSS). | III.3 (Zagrożenia sieciowe) | Jak haker wstrzykuje obcy kod JS w stronę, żeby ukraść Twoją sesję. | JS, Spreparowana strona |
| **20-21** | **Twój Portal jako Backend (API) dla uczniów.** | I.1, III.2 (Rozumienie systemów) | Nauka komunikacji z Twoim środowiskiem. Wysyłanie i pobieranie danych. | **Twój Portal (API)** |
| **22-23** | *Projekt Web (Gr)*: Architektura i projekt interfejsu klienta. | I.1, IV.1 (Planowanie projektowe) | Szkicowanie aplikacji (Figma), która będzie nakładką wizualną na Twój system. | Figma/NotebookLM |
| **24-27** | *Projekt Web (Gr)*: Realizacja interfejsu w JS podłączonego pod API. | II.1, IV.1 (Systemy webowe) | Kodowanie aplikacji, asynchroniczna wymiana danych z portalem, Pair Programming z AI. | JS, Twój Portal |
| **28** | Weryfikacja jakości (Code Review i audyt bezpieczeństwa). | II.2, III.3 (Ewaluacja) | Testowanie inputów pod kątem poznanych wcześniej ataków (XSS) u kolegów z grupy. | Przeglądarka, Portal |
| **29-30** | Demo Day – Symulacja odbioru projektu przez "klienta". | IV.3 (Prezentacja, media) | Grupy prezentują projekt korzystający z Twojego portalu. | Rzutnik |
