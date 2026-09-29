# 🛡️ CYBER.ACADEMY • Laboratorium Cyberbezpieczeństwa dla Uczniów

Nowoczesny, interaktywny portal edukacyjny z zakresu cyberbezpieczeństwa stworzony specjalnie dla uczniów **Liceum Ogólnokształcącego** oraz **Technikum Informatycznego / Programistycznego**.

Zaprojektowany na bazie autorskich rozkładów materiału i scenariuszy lekcji **Przemysława Żarneckiego (INFOTECH)**, w pełnej zgodności z polską podstawą programową nauczania informatyki w szkole średniej.

🌐 **Wersja online (GitHub Pages):** [https://pzarnecki.github.io/infotech/](https://pzarnecki.github.io/infotech/)

---

## 🚀 Jak uruchomić lokalnie?

Strona została zbudowana jako w 100% samodzielna aplikacja **Single Page Application (SPA)**:
1. **Opcja 1 (Bezpośrednia):** Po prostu kliknij dwukrotnie w plik `index.html` w dowolnej przeglądarce (Chrome, Firefox, Edge, Safari). Nie wymaga żadnych instalacji, baz danych ani kompilacji.
2. **Opcja 2 (Lokalny serwer deweloperski):**
   ```bash
   cd /home/przemek/Dokumenty/Cyber_Uczniowie
   python3 -m http.server 8080
   # Otwórz w przeglądarce: http://localhost:8080
   ```

---

## 📋 Zoperacjonalizowany Model Zadań (Google Classroom)

Wszystkie zadania w zakładce **„Zadania Classroom”** zostały zaprojektowane według nowoczesnego modelu operacyjnego **Zrób &rarr; Przetestuj &rarr; Wklej do Classroom**:

### Każda misja zawiera:
1. **Jasny cel operacyjny:** Co uczeń potrafi po wykonaniu zadania.
2. **Instrukcję wykonawczą krok po kroku:** Precyzyjne kroki, adresy zaufanych narzędzi i zadania analityczne.
3. **Kryteria sukcesu NaCoBeZu (od 3 do 6):**
   * *Ocena 3 (Dostateczny):* Poziom podstawowy (minimalny).
   * *Ocena 4 (Dobry):* Poprawne wykonanie z uzasadnieniem.
   * *Ocena 5 (Bardzo Dobry):* Rozszerzona analiza techniczna i wnioski.
   * *Ocena 6 (Celujący):* Wyzwanie z gwiazdką (np. konfiguracja Bitwarden z 2FA, skrypt brute-force w Colabie, analiza Blind SQLi).
4. **Dwa dedykowane przyciski kopiowania jednym kliknięciem:**
   * 📋 **„Treść dla Nauczyciela”** – gotowa treść polecenia do wklejenia w Google Classroom jako nowe zadanie.
   * ✍️ **„Formularz dla Ucznia”** – ustrukturyzowany szablon odpowiedzi z polami `[WPISZ TUTAJ]`, który uczeń wkleja do pola odpowiedzi i wypełnia.

### 4 Pełne Misje Projektowe:
* **Misja LO-01:** *Operacja „Tarcza Osobista” – Audyt Wycieków w HaveIBeenPwned & Dekonstrukcja Phishingu SMS*
* **Misja LO-02:** *Operacja „Licencyjny Detektyw” – Legalność Kodu z GitHuba (MIT vs GPL) & Prawa Autorskie w Erze GenAI*
* **Misja TECH-01:** *Operacja „Hash & Salt” – Implementacja Funkcji SHA-256 w Pythonie (Google Colab) & Analiza Efektu Lawinowego*
* **Misja TECH-02:** *Operacja „Web Auditor” – Audyt Podatności SQL Injection (' OR '1'='1) & Studium Przypadku Wycieku ALAB (OSINT)*

---

## 📝 Interaktywne Karty Samodzielnej Pracy (Self-Study Labs)

Pod zadaniami Classroom znajduje się 8-etapowa interaktywna checklista samodzielnych ćwiczeń uczniowskich (zapisująca stan w pamięci `localStorage` przeglądarki):
* **Karta A (Osobista Cyber-Twierdza):** Sprawdzenie e-maila w HIBP, silne hasło 16+ znaków, konfiguracja 2FA (TOTP) i bezpieczne zapisanie kodów zapasowych offline.
* **Karta B (Laboratorium Audytora & Kod):** Uruchomienie skryptu w Colabie, zrozumienie podatności konkatenacji w SQL, zapisanie w telefonie numeru CERT 8080 oraz zdanie testu na min. 80%.

---

## 🎯 Dwie Ścieżki Kształcenia (Dynamic Track Switcher)

W górnym menu znajduje się natychmiastowy przełącznik dostosowujący treści, spis modułów, slajdy i zadania:

### 📘 1. Ścieżka Liceum Ogólnokształcące
*„Rozpoznanie z lotu ptaka & Higiena Cyfrowa”*
* **Moduł 1:** Anatomia haseł, bazy danych serwera i zjawisko *Credential Stuffing* (studium wycieku Morele.net).
* **Moduł 2:** Trzy złote zasady higieny (zasada 1:1, menedżer Bitwarden, hierarchia 2FA: SMS vs TOTP vs klucze FIDO2 YubiKey).
* **Moduł 3:** Phishing i 4 filary manipulacji socjotechnicznej (pośpiech, autorytet, lęk, chciwość), demaskowanie fałszywych domen i numer 8080.
* **Moduł 4:** Prawo w IT: licencje Open Source (permisywna MIT vs wirusowa GNU GPL copyleft) oraz status prawny kodu wygenerowanego przez AI (art. 1 pr. aut.).

### ⚡ 2. Ścieżka Technikum Informatyczne
*„Profil Audytor / Red Team / Pentester / Kod”*
* **Moduł 1:** Kryptografia w praktyce: architektura SHA-256 (64 rundy bitowe, rejestry, padding), efekt lawinowy i paradoks urodzin.
* **Moduł 2:** Sól kryptograficzna (Salt), unieszkodliwianie Tęczowych Tablic (Rainbow Tables) oraz nowoczesne funkcje KDF (bcrypt, Argon2id, PBKDF2).
* **Moduł 3:** Biały Wywiad (OSINT), zaawansowany Google Dorking oraz studium wycieku medycznego ALAB Laboratoria (ransomware RA World).
* **Moduł 4:** Bezpieczeństwo Webowe OWASP Top 10: SQL Injection (`admin' OR '1'='1 --`), bindowanie parametrów *Prepared Statements* oraz Cross-Site Scripting (XSS).
* **Moduł 5:** Memory Safety: przepełnienie bufora stosu (*Stack Buffer Overflow*) w C/C++ oraz rewolucja Borrow Checkera w języku Rust.

---

## 🧪 Interaktywne Laboratoria na Żywo (CTF)

1. **Kalkulator SHA-256 z Efektem Lawinowym:** hashowanie w locie (`SubtleCrypto`), test zmiany 1 znaku, dodanie kryptograficznej soli i gotowy kod Python.
2. **Inspektor SMS Phishing (Makieta Smartfona):** klikalne „czerwone flagi” (presja czasu, mikrodopłata 1,50 zł, podmieniona domena, brak HTTPS).
3. **Symulator SQL Injection:** formularz logowania z podglądem generowanego zapytania w bazie oraz przełącznikiem na *Prepared Statements*.
4. **Wyzwanie AI Red Teaming:** mini-chatbot strażnik pilnujący flagi `FLAG{INFOTECH_CYBER_2026}` – testowanie socjotechniki na LLM.
5. **Gra Decyzyjna: Atak Ransomware w Szkole:** symulator podejmowania decyzji w pierwszych sekundach po zainfekowaniu komputera pendrivem.
6. **Miernik Siły Hasła RTX 4090 & Generator Passphrase XKCD:** obliczanie czasu łamania hasła oraz losowanie 4-słownych haseł słownikowych.
7. **Egzamin & Quiz Adepta:** dynamiczny test z oceną szkolną (1-6) i natychmiastowym feedbackiem.

---

## 🎨 Oprawa Techniczna

* **Stylistyka:** Dark Cyberpunk / Neon Green & Cyan & Magenta (Glassmorphism, glow, scanlines).
* **Dźwięk:** Wbudowany syntezator dźwięków cybernetycznych bazujący na natywnym **Web Audio API** (laserowy sweep zakładek, dźwięki terminala, fanfary sukcesu).
* **Prezentacja:** Pełnoekranowy tryb slajdów z paskiem miniatur (Thumbnails) i notatkami metodycznymi.
* **Certyfikat:** Generator personalizowanego Certyfikatu Ukończenia z datą i nazwiskiem ucznia.

---

## 📁 Kompletne Repozytorium Materiałów Dydaktycznych (`materialy/`)

Wszystkie pliki źródłowe, rozkłady oraz zoperacjonalizowane karty zadań z konwersacji zostały przeniesione do repozytorium i rozbudowane o pełne opisy merytoryczne, rubryki NaCoBeZu oraz szablony dla uczniów:

### 🎓 1. Rozkłady Materiału & Dokumentacja Szkolna:
* [`rozklad_materialu_infotech.md`](materialy/rozklad_materialu_infotech.md) – Pełny, 30-godzinny autorski rozkład materiału dla klas 1 i 2 (podstawa programowa w nowoczesnym ujęciu rynkowym).
* [`rozklad_dla_dyrekcji.md`](materialy/rozklad_dla_dyrekcji.md) oraz [`rozklad_dla_dyrekcji.pdf`](materialy/rozklad_dla_dyrekcji.pdf) – Wersja oficjalna dla dyrekcji szkoły i kuratorium.
* [`rozklad_dla_nauczyciela.pdf`](materialy/rozklad_dla_nauczyciela.pdf) – Praktyczny przewodnik metodyczny dla nauczyciela prowadzącego.

### 📋 2. Zoperacjonalizowane Pakiety Google Classroom (Miesiąc 1):
* [`materialy_classroom_m1.md`](materialy/materialy_classroom_m1.md) – **Główny Master-Dokument:** Zestawienie 4 tygodni zajęć dla Liceum i Technikum z gotowymi postami nauczyciela, zarysami tablicy, instrukcjami krok po kroku, rubrykami oceniania 3-6 i szablonami odpowiedzi.
* [`LO_Lekcja_2_do_4_Cyber.md`](materialy/LO_Lekcja_2_do_4_Cyber.md) – Pogłębiony pakiet dydaktyczny dla Liceum: hasła, menedżery Zero-Knowledge, wycieki HaveIBeenPwned, socjotechnika SMS InPost, procedura CERT 8080.
* [`Tech_Lekcja_2_3_OSINT.md`](materialy/Tech_Lekcja_2_3_OSINT.md) – Profesjonalny pakiet dla Technikum: skryptowanie SHA-256 w Pythonie z soleniem (`hashlib`, `secrets`), obrona przed Rainbow Tables, analiza wycieku ALAB / Morele (OSINT).

### ⚖️ 3. Prawo w IT, Licencje i Etyka AI:
* [`LO_Lekcja_4_5_Prawo_Teoria.md`](materialy/LO_Lekcja_4_5_Prawo_Teoria.md) & [`LO_Lekcja_4_5_Prawo_Zadania.md`](materialy/LO_Lekcja_4_5_Prawo_Zadania.md) – Analiza licencji MIT vs GPL oraz praw autorskich do wytworów generatywnej sztucznej inteligencji (Liceum).
* [`Tech_Lekcja_4_5_Prawo_Teoria.md`](materialy/Tech_Lekcja_4_5_Prawo_Teoria.md) & [`Tech_Lekcja_4_5_Prawo_Zadania.md`](materialy/Tech_Lekcja_4_5_Prawo_Zadania.md) – Zaawansowany audyt licencyjny, efekt wirusowy Copyleft, License Laundering w modelach LLM oraz specyfikacja SBOM (Technikum).

### 🕵️ 4. Prywatność w Sieci, Sieci Cebulowe i Bezpieczeństwo Systemów:
* [`LO_Prezentacja_Prywatnosc.md`](materialy/LO_Prezentacja_Prywatnosc.md) & [`LO_Zadania_Prywatnosc.md`](materialy/LO_Zadania_Prywatnosc.md) – Przegląd narzędzi: Tryb Incognito vs VPN vs Tor, ochrona przed profilowaniem reklamowym (Liceum).
* [`Tech_Prezentacja_Prywatnosc.md`](materialy/Tech_Prezentacja_Prywatnosc.md) & [`Tech_Zadania_Prywatnosc.md`](materialy/Tech_Zadania_Prywatnosc.md) – Inżynieria prywatności: analiza Exit Node w sieci Tor, DNS Sinkhole (Pi-Hole) oraz izolacja hiperwizora Xen w systemie Qubes OS (Technikum).

### 💻 5. Pierwsze Środowisko i Wprowadzenie do Chmury:
* [`LO_L01_Tutorial.md`](materialy/LO_L01_Tutorial.md) & [`LO_L01_Prezentacja.md`](materialy/LO_L01_Prezentacja.md) – Pierwsze kroki w chmurze Google Colab bez instalacji lokalnej.
* [`LO_L07_Zadanie_Podsumowujace.md`](materialy/LO_L07_Zadanie_Podsumowujace.md) – Projekt integracyjny.

