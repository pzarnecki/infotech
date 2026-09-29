# 🎓 Google Classroom – Zoperacjonalizowany Pakiet Dydaktyczny (Miesiąc 1)
## Kompletne Szablony Wpisów, Materiałów, Zadań i Formularzy dla Uczniów
**Autor:** Przemysław Żarnecki • Program Edukacyjny INFOTECH 2026  
**Struktura:** Liceum Ogólnokształcące oraz Technikum Informatyczne (profil rozszerzony/zawodowy)

---

## 📌 JAK KORZYSTAĆ Z TEGO DOKUMENTU?
Każdy tydzień zawiera dwa gotowe bloki tekstowe:
1. **📝 Treść Posta / Materiału dla Nauczyciela:** Zawiera wprowadzenie, cel operacyjny oraz zarys tablicy/prezentacji.
2. **📋 Zadanie do Google Classroom:** Zawiera twarde instrukcje krok po kroku, kryteria oceniania NaCoBeZu (3-6) oraz **gotowy formularz odpowiedzi**, który uczeń wkleja do pola odpowiedzi w Classroomie.

---

# ==============================================================================
# 📘 ŚCIEŻKA LICEUM OGÓLNOKSZTAŁCĄCE
# ==============================================================================

## 🗓️ TYDZIEŃ 1: Twoje Pierwsze Środowisko IT w Chmurze (Google Colab)
* **Typ wpisu:** Materiał + Zadanie z projektem
* **Cel operacyjny:** Uczeń potrafi uruchomić notatnik w chmurze bez instalacji środowiska lokalnego, rozróżnia komórki tekstowe (Markdown) od komórek z kodem i potrafi udostępnić link z uprawnieniami do odczytu.

### 📝 Treść posta do wklejenia w Classroom:
```markdown
Cześć! Witajcie na pierwszych zajęciach z informatyki w INFOTECH. 🚀
W dzisiejszym świecie IT programiści i analitycy rzadko instalują całe oprogramowanie na własnym laptopie. Gdy pracujesz w zespole, z podróży lub na słabszym sprzęcie – Twoim środowiskiem pracy staje się Chmura Obliczeniowa (Cloud Computing).

Na naszych zajęciach będziemy używać Google Colab – wirtualnego notatnika działającego w przeglądarce, na którym pracuje prawdziwy system Linux i język Python, a za moc obliczeniową odpowiadają potężne centra danych Google.

ZARYS TABLICY / PREZENTACJI:
1. Co to jest Chmura Obliczeniowa? (Dostęp do zasobów obliczeniowych przez Internet).
2. Zalety Chmury: brak instalacji, automatyczny zapis, praca zespołowa w czasie rzeczywistym.
3. Notatnik Jupyter / Colab: komórka tekstowa (notatki, instrukcje w Markdown) + komórka kodu (wykonywalny kod Pythona).
```

### 📋 Zadanie w Classroom (Polecenie + Formularz):
```markdown
# ZADANIE 01: Konfiguracja Notatnika w Google Colab
Termin: Do końca lekcji / najbliższe zajęcia
Forma: Link do notatnika w chmurze

INSTRUKCJA KROK PO KROKU:
1. Wejdź na stronę: https://colab.research.google.com/ (zaloguj się kontem szkolnym Google).
2. Kliknij: Plik -> Nowy notatnik. Zmień nazwę pliku na: `L01_Chmura_[Twoje_Imie_Nazwisko]`.
3. Dodaj komórkę TEKSTOWĄ (+ Tekst) i wpisz:
   # Laboratorium Informatyki INFOTECH
   Uczeń: [Twoje Imię i Nazwisko]
   Status: Środowisko chmurowe skonfigurowane poprawnie!
4. Dodaj komórkę KODU (+ Kod) i wpisz:
   print("Witaj w chmurze Google Colab! Mój system działa.")
   Uruchom komórkę klikając przycisk Play.
5. Kliknij w prawym górnym rogu przycisk "Udostępnij" (Share) -> Zmień dostęp ogólny na: "Każda osoba mająca link" -> Rola: "Przeglądający" -> Skopiuj link.
6. Wklej skopiowany link w formularzu odpowiedzi poniżej.

KRYTERIA OCENY (NaCoBeZu):
- Ocena Dostateczna (3): Utworzenie notatnika z komórką tekstową.
- Ocena Dobra (4): Poprawny notatnik z uruchomionym kodem print() i działającym linkiem.
- Ocena Bardzo Dobra (5): Ocena 4 + sformatowany nagłówek Markdown w komórce tekstowej.
- Ocena Celująca (6): Dodanie drugiej komórki kodu obliczającej proste działanie matematyczne (np. 2026 * 365) z opisem tekstowym.

--- FORMULARZ ODPOWIEDZI UCZNIA ---
Imię i Nazwisko: [WPISZ TUTAJ]
Klasa: [WPISZ KLASĘ]
1. Mój link do notatnika Colab: [WKLEJ LINK TUTAJ]
2. Jakie zalety ma praca w chmurze w porównaniu z instalacją programów na dysku C?:
   [Twoja odpowiedź w 1 zdaniu...]
-----------------------------------
```

---

## 🗓️ TYDZIEŃ 2: Tajemnice Haseł i Wycieki Danych (Data Breach)
* **Typ wpisu:** Materiał + Śledztwo cyfrowe
* **Cel operacyjny:** Uczeń potrafi wyjaśnić mechanizm wycieku bazy danych i ataku Credential Stuffing, weryfikuje status konta w bazie HaveIBeenPwned i zna zasadę działania menedżera haseł.

### 📝 Treść posta do wklejenia w Classroom:
```markdown
Czy wiesz, że ponad 60% włamań na konta społecznościowe nie wynika ze złamania hasła, lecz z kradzieży bazy ze słabo zabezpieczonych sklepów? 🔓
Jeśli używasz hasła "Piesek123" na starym forum o grach, a potem tego samego hasła na Gmailu – przestępcy bez trudu przejmą Twoją skrzynkę pocztową. Nazywamy to Credential Stuffing.

ZARYS TABLICY / PREZENTACJI:
1. Jak bazy danych przechowują hasła? (Jednokierunkowy skrót hash SHA-256).
2. Dlaczego jedno hasło wszędzie to katastrofa? (Zasada uniwersalnego klucza).
3. Menedżer haseł (Bitwarden) – jak działa architektura Zero-Knowledge?
4. Zasada 1:1 – Jedno konto = Jedno unikalne hasło.
```

### 📋 Zadanie w Classroom (Polecenie + Formularz):
```markdown
# ZADANIE 02: Śledztwo Wyciekowe w HaveIBeenPwned
Termin: Najbliższe zajęcia
Forma: Formularz odpowiedzi w Classroomie

INSTRUKCJA KROK PO KROKU:
1. Otwórz zaufany serwis prowadzony przez dyrektora Microsoft ds. bezpieczeństwa: https://haveibeenpwned.com/
2. Wpisz swój adres e-mail (lub adres testowy/kogoś bliskiego za zgodą).
3. Sprawdź, czy adres pojawił się w publicznych wyciekach (Pwned!).
4. Jeśli adres wyciekł: zapisz nazwę serwisu, rok i jakie dane skradziono.
   Jeśli jest czysty: pogratuluj sobie, a w serwisie sprawdź popularny portal, np. Adobe lub Canva.
5. Wypełnij formularz odpowiedzi.

KRYTERIA OCENY (NaCoBeZu):
- Ocena Dostateczna (3): Sprawdzenie 1 adresu i wpisanie statusu.
- Ocena Dobra (4): Podanie nazwy bazy wyciekowej, roku i kategorii wykradzionych danych.
- Ocena Bardzo Dobra (5): Ocena 4 + podanie nazwy darmowego menedżera haseł i wyjaśnienie pojęcia Master Password.
- Ocena Celująca (6): Wyjaśnienie, dlaczego zmiana samego hasła po wycieku PESEL-u (np. w aferze Morele/ALAB) nie rozwiązuje problemu tożsamości.

--- FORMULARZ ODPOWIEDZI UCZNIA ---
Imię i Nazwisko: [WPISZ TUTAJ]
Klasa: [WPISZ KLASĘ]
1. Wynik w HaveIBeenPwned: [CZYSTE / WYCIEKŁO Z ...]
2. Nazwa serwisu i rok wycieku (jeśli dotyczy): [WPISZ TUTAJ]
3. Jakie dane dostały się w ręce hakerów?: [WPISZ TUTAJ]
4. Do czego służy Hasło Główne (Master Password) w menedżerze haseł?:
   [Twoja odpowiedź...]
-----------------------------------
```

---

## 🗓️ TYDZIEŃ 3: Phishing i Ochrona Przed Socjotechniką
* **Typ wpisu:** Materiał + Analiza przypadku
* **Cel operacyjny:** Uczeń potrafi zidentyfikować 4 czerwone flagi w wiadomości phishingowej, poprawnie analizuje strukturę adresu URL i zna numer alarmowy CERT Polska (8080).

### 📝 Treść posta do wklejenia w Classroom:
```markdown
Hakerzy rzadko pokonują zapory sieciowe – znacznie łatwiej jest oszukać człowieka! 🎣
Phishing to manipulacja emocjami: strachem, pośpiechem lub chciwością.

ZARYS TABLICY / PREZENTACJI:
1. Anatomia oszustwa „na dopłatę do paczki InPost 1,50 PLN”.
2. Jak czytać domenę? Zawsze od prawej do lewej strony!
   - inpost.pl -> PRAWDA
   - inpost-paczka-platnosc.xyz -> FAŁSZ (domena to platnosc.xyz!)
3. Gdzie zgłaszać fałszywe SMS-y? Bezpłatny numer CERT Polska: 8080.
```

### 📋 Zadanie w Classroom (Polecenie + Formularz):
```markdown
# ZADANIE 03: Dekonstrukcja Złośliwego SMS-a
Termin: Najbliższe zajęcia

Przeanalizuj treść SMS:
"Twoja paczka InPost zostala wstrzymana z powodu niedoplaty 1,50 PLN. Kliknij w link aby uregulowac: http://inpost-platnosci-paczka.pl/login"

Wypełnij formularz poniżej, wyjaśniając problem tak, jakbyś tłumaczył go swojej babci.

KRYTERIA OCENY (NaCoBeZu):
- Ocena Dostateczna (3): Wskazanie 1 czerwonej flagi.
- Ocena Dobra (4): Wskazanie 2 czerwonych flag z uzasadnieniem dla babci.
- Ocena Bardzo Dobra (5): Ocena 4 + podanie numeru 8080 i wyjaśnienie pojęcia mikro-dopłaty.
- Ocena Celująca (6): Analiza protokołu http:// vs https:// i wyjaśnienie certyfikatów SSL.

--- FORMULARZ ODPOWIEDZI UCZNIA ---
Imię i Nazwisko: [WPISZ TUTAJ]
Klasa: [WPISZ KLASĘ]
1. Czerwona flaga 1 (wyjaśnij babci): [WPISZ TUTAJ]
2. Czerwona flaga 2 (wyjaśnij babci): [WPISZ TUTAJ]
3. Dlaczego przestępcy żądają małej kwoty 1,50 zł, a nie 500 zł?: [WPISZ TUTAJ]
4. Na jaki numer telefonu przekażesz tego SMS-a w Polsce?: [WPISZ NUMER]
-----------------------------------
```

---

## 🗓️ TYDZIEŃ 4: Weryfikacja Dwuetapowa (2FA) & Prawo Open Source
* **Typ wpisu:** Materiał + Projekt Podsumowujący
* **Cel operacyjny:** Uczeń potrafi wyjaśnić różnicę między SMS 2FA a aplikacją TOTP oraz rozróżnia licencje MIT i GNU GPL.

### 📋 Zadanie Podsumowujące Miesiąc 1 (Liceum):
```markdown
# ZADANIE 04: Zostań Architektem Bezpieczeństwa Domowego
Wypełnij formularz końcowy modułu 1:
1. Wyjaśnij, dlaczego kody SMS 2FA są mniej bezpieczne niż aplikacja Google Authenticator (podpowiedź: SIM Swapping).
2. Twój kolega chce sprzedać program, w którym użył biblioteki na licencji GNU GPL v3. Czy może to zrobić bez ujawniania kodu źródłowego? Uzasadnij.
3. Wskaż 3 konkretne zmiany, które wprowadziłeś na swoich prywatnych kontach w tym miesiącu.

--- FORMULARZ ODPOWIEDZI UCZNIA ---
Imię i Nazwisko: [WPISZ TUTAJ]
1. SMS 2FA vs Aplikacja TOTP: [WYJAŚNIENIE...]
2. Licencja GNU GPL v3 w projekcie: [WYJAŚNIENIE ZASADY COPYLEFT...]
3. Moje 3 wdrożone zasady higieny cyfrowej:
   a) ...
   b) ...
   c) ...
-----------------------------------
```

---

# ==============================================================================
# 📙 ŚCIEŻKA TECHNIKUM INFORMATYCZNE
# ==============================================================================

## 🗓️ TYDZIEŃ 1: Architektura Chmurowa & Wprowadzenie do Kryptografii (SHA-256)
* **Typ wpisu:** Projekt Laboratoryjny
* **Cel operacyjny:** Uczeń rozumie różnicę między szyfrowaniem symetrycznym a jednokierunkową funkcją skrótu, potrafi zaimportować moduł `hashlib` i wygenerować skrót SHA-256 w Pythonie.

### 📝 Treść posta do wklejenia w Classroom:
```markdown
Cześć przyszli inżynierowie IT! ⚡
Na informatyce ogólnej nie będziemy dublować podstaw programowania z przedmiotów zawodowych. Skupiamy się na twardej architekturze systemów i bezpieczeństwie backendu.
Dziś badamy matematyczny fundament baz danych: jednokierunkowe funkcje skrótu (Cryptographic Hashing).

ZARYS TABLICY / PREZENTACJI:
1. Szyfr (dwukierunkowy) vs Hash (jednokierunkowy).
2. Algorytm SHA-256: 512-bitowe bloki, 64 rundy bitowych przekształceń logicznych, 256-bitowy wynik w HEX (64 znaki).
3. Efekt Lawinowy (Avalanche Effect): zmiana 1 bitu na wejściu zmienia ~50% bitów wyjściowych.
```

### 📋 Zadanie w Classroom (Polecenie + Formularz):
```markdown
# PROJEKT 01: Pierwszy Silnik Hashujący SHA-256 w Pythonie
Termin: Zakończenie zajęć projektowych
Forma: Link do Google Colab z kodem

INSTRUKCJA KROK PO KROKU:
1. Otwórz Google Colab i utwórz notatnik: `TECH_L01_SHA256_[Nazwisko]`.
2. Zaimplementuj funkcję `oblicz_sha256(tekst)`, która zamienia tekst na bajty (.encode('utf-8')) i zwraca .hexdigest().
3. Przetestuj funkcję dla słowa "haslo123" oraz "haslo124".
4. Oblicz różnicę wizualną w obu hashach i opisz w komórce tekstowej pojęcie efektu lawinowego.
5. Udostępnij notatnik z uprawnieniami do odczytu i wklej link do formularza.

KRYTERIA OCENY (NaCoBeZu):
- Ocena Dostateczna (3): Poprawne wygenerowanie hasha dla 1 słowa.
- Ocena Dobra (4): Poprawna funkcja + test 2 słów różniących się 1 znakiem + publiczny link.
- Ocena Bardzo Dobra (5): Ocena 4 + profesjonalny opis efektu lawinowego w notatniku.
- Ocena Celująca (6): Zaimplementowanie pętli sprawdzającej ile znaków różni oba hashe!

--- FORMULARZ ODPOWIEDZI UCZNIA ---
Imię i Nazwisko: [WPISZ TUTAJ]
Klasa: [NP. 1TI / 2TI]
1. Link do notatnika Google Colab: [WKLEJ LINK]
2. Czym różni się hashowanie SHA-256 od szyfrowania AES-256?: [ODPOWIEDŹ...]
3. Wygenerowany hash dla hasła 'haslo123': [WKLEJ HASH]
-----------------------------------
```

---

## 🗓️ TYDZIEŃ 2: Tęczowe Tablice i Sól Kryptograficzna (Salt)
* **Typ wpisu:** Projekt Laboratoryjny
* **Cel operacyjny:** Uczeń potrafi zaimplementować bezpieczne solenie haseł za pomocą modułu `secrets`, rozumie zasadę działania Rainbow Tables i potrafi wyjaśnić dlaczego SHA-256 wymaga wolnych KDF (bcrypt/Argon2id).

### 📋 Zadanie w Classroom (Polecenie + Formularz):
```markdown
# PROJEKT 02: Implementacja Soli (Salt) i Obrona przed Rainbow Tables
Termin: Zakończenie zajęć projektowych
Forma: Notatnik Colab + formularz

INSTRUKCJA:
1. Wykorzystaj moduł `hashlib` oraz `secrets`.
2. Napisz funkcję `haszuj_z_sola(haslo, sol=None)`, która w przypadku braku soli losuje 16 bajtów (`secrets.token_hex(16)`).
3. Stwórz listę 4 haseł słownikowych: `["admin", "123456", "root", "qwerty"]`.
4. Użyj pętli `for`, generując dla każdego unikalną sól i hash.
5. Wykaż w notatniku, że hashowanie tego samego hasła dwukrotnie z inną solą daje zupełnie inny ciąg w bazie.

KRYTERIA OCENY (NaCoBeZu):
- Ocena Dostateczna (3): Działający kod bez pętli.
- Ocena Dobra (4): Pętla for po liście haseł z losową solą dla każdego z nich.
- Ocena Bardzo Dobra (5): Ocena 4 + wyjaśnienie pojęcia Tęczowych Tablic (Rainbow Tables).
- Ocena Celująca (6): Wyjaśnienie dlaczego karta graficzna RTX 4090 łamie SHA-256 z prędkością 8 mld/s i dlaczego systemy produkcyjne wymagają bcrypt/Argon2id.

--- FORMULARZ ODPOWIEDZI UCZNIA ---
Imię i Nazwisko: [WPISZ TUTAJ]
1. Link do notatnika Colab z soleniem haseł: [WKLEJ LINK]
2. Dlaczego solenie haseł unieszkodliwia ataki tęczowymi tablicami?: [WYJAŚNIENIE...]
3. Co to jest funkcja Argon2id i dlaczego jest memory-hard?: [WYJAŚNIENIE...]
-----------------------------------
```

---

## 🗓️ TYDZIEŃ 3: Biały Wywiad (OSINT) & Raport z Afery Medycznej ALAB
* **Typ wpisu:** Raport Audytorski Red Team
* **Cel operacyjny:** Uczeń stosuje techniki Google Dorking w celach audytowych, bada publiczne bazy wyciekowe i sporządza analizę podatności na bazie incydentu ALAB / Morele.

### 📋 Zadanie w Classroom (Polecenie + Formularz):
```markdown
# PROJEKT 03: Raport Wywiadowczy OSINT (Afera ALAB Laboratoria)
Wcielasz się w rolę Analityka Bezpieczeństwa (Threat Intelligence).
Przeanalizuj atak ransomware grupy RA World na sieć laboratoriów ALAB z listopada 2023 roku.

WYPEŁNIJ FORMULARZ AUDYTORSKI:
- Wektor ataku (jak napastnicy dostali się do infrastruktury).
- Kategorie skradzionych danych pacjentów (PESEL, badania krwi, onkologia).
- Skutki prawne: RODO, postępowanie UODO, konieczność zastrzegania PESEL w mObywatelu.
- Dorking: Wyjaśnij do czego służy kwerenda: `filetype:env DB_PASSWORD`.

--- FORMULARZ ODPOWIEDZI UCZNIA ---
Imię i Nazwisko: [WPISZ TUTAJ]
1. Wektor ataku na sieć ALAB: [OPIS...]
2. Jakie dane pacjentów zostały opublikowane w Darknecie?: [OPIS...]
3. Jakie ryzyko dla obywatela niesie kradzież numeru PESEL w połączeniu z adresem i nazwiskiem?: [OPIS...]
4. Do czego haker użyje zapytania Google Dork: `site:pl filetype:sql "INSERT INTO users"`?: [OPIS...]
-----------------------------------
```

---

## 🗓️ TYDZIEŃ 4: Bezpieczeństwo Webowe (OWASP Top 10: SQL Injection)
* **Typ wpisu:** Audyt Kodu i Refaktoryzacja
* **Cel operacyjny:** Uczeń potrafi rozpoznać podatność SQL Injection w kodzie backendu, wyjaśnia ładunek `admin' OR '1'='1 --` oraz pisze bezpieczne zapytanie z Prepared Statements.

### 📋 Zadanie w Classroom (Polecenie + Formularz):
```markdown
# PROJEKT 04: Neutralizacja Podatności SQL Injection
Przeanalizuj podatne zapytanie backendowe:
`query = "SELECT * FROM users WHERE login = '" + user_input + "' AND pass = '" + pass_input + "'"`

ZADANIA DO WYKONANIA:
1. Wyjaśnij matematyczno-logiczną zasadę, dzięki której wpisanie `admin' OR '1'='1 --` loguje hakera bez hasła.
2. Napisz poprawną wersję zapytania w języku Python (sqlite3) lub PHP (PDO) z użyciem bindowania parametrów (Prepared Statements).
3. Czym różni się atak In-Band SQLi od Blind SQLi (opartego na opóźnieniach czasowych SLEEP)?

--- FORMULARZ ODPOWIEDZI UCZNIA ---
Imię i Nazwisko: [WPISZ TUTAJ]
1. Zasada działania ładunku ' OR '1'='1: [WYJAŚNIENIE...]
2. Bezpieczny kod (Prepared Statements):
```python
# Wklej bezpieczny fragment kodu...
cursor.execute("SELECT * FROM users WHERE login = ? AND pass = ?", (user_input, pass_input))
```
3. Czym jest Blind SQL Injection?: [WYJAŚNIENIE...]
-----------------------------------
```
