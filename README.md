# 🛡️ CYBER.ACADEMY • Laboratorium Cyberbezpieczeństwa dla Uczniów

Nowoczesny, interaktywny portal edukacyjny z zakresu cyberbezpieczeństwa stworzony specjalnie dla uczniów **Liceum Ogólnokształcącego** oraz **Technikum Informatycznego / Programistycznego**.

Zaprojektowany na bazie autorskich rozkładów materiału i scenariuszy lekcji **Przemysława Żarneckiego (INFOTECH)**, w pełnej zgodności z polską podstawą programową nauczania informatyki w szkole średniej.

---

## 🚀 Jak uruchomić?

Strona została zbudowana jako w 100% samodzielna aplikacja **Single Page Application (SPA)**:
1. **Opcja 1 (Bezpośrednia):** Po prostu kliknij dwukrotnie w plik `index.html` w dowolnej nowoczesnej przeglądarce (Chrome, Firefox, Edge, Safari). Nie wymaga żadnych instalacji ani kompilacji.
2. **Opcja 2 (Lokalny serwer):**
   ```bash
   cd /home/przemek/Dokumenty/Cyber_Uczniowie
   python3 -m http.server 8080
   # Wejdź w przeglądarce na: http://localhost:8080
   ```

---

## 🎯 Dwie Dedykowane Ścieżki Kształcenia

Portal posiada wbudowany **przełącznik profili (Track Switcher)** w górnym menu, który w ułamku sekundy dostosowuje poziom merytoryczny, spis treści, slajdy oraz zadania:

### 📘 1. Ścieżka Liceum Ogólnokształcące (1h / tydz.)
*„Rozpoznanie z lotu ptaka & Higiena Cyfrowa”*
* **Cel:** Natychmiastowa ochrona tożsamości młodego człowieka w sieci, bez konieczności lokalnej instalacji środowisk programistycznych (praca w przeglądarce i Google Colab).
* **Kluczowe moduły:**
  * **Syndrom jednego hasła:** Dlaczego `Piesek123` użyty w 20 serwisach to zaproszenie dla hakera.
  * **Wycieki danych (Data Breaches) & Credential Stuffing:** Jak hakerzy zdobywają bazy i weryfikacja w serwisie `HaveIBeenPwned`.
  * **Trzy Złote Zasady:** Zasada 1:1, Menedżer haseł (Bitwarden) oraz weryfikacja dwuetapowa 2FA/MFA.
  * **Anatomia Phishingu:** Analiza złośliwych wiadomości SMS („na dopłatę do paczki InPost 1,50 PLN”) i 4 czerwone flagi.
  * **Prawo i Etyka:** Licencje Open Source (MIT vs GPL copyleft) oraz odpowiedzialne korzystanie ze sztucznej inteligencji.

### ⚡ 2. Ścieżka Technikum Informatyczne (2h / tydz.)
*„Profil Audytor / Red Team / Pentester / Kod”*
* **Cel:** Praktyczne uzupełnienie przedmiotów zawodowych (INF.03 / INF.04) bez nudnego powtarzania podstawowych pętli.
* **Kluczowe moduły:**
  * **Kryptografia w Pythonie:** Moduł `hashlib`, funkcja skrótu SHA-256 jako jednokierunkowy cyfrowy odcisk palca.
  * **Efekt Lawinowy & Tęczowe Tablice (Rainbow Tables):** Dlaczego dodajemy sól kryptograficzną (`salt`) i jak zapobiegać atakom słownikowym.
  * **Biały Wywiad (OSINT):** Badanie wektorów ataku, profilowanie organizacji, studium głośnych afer wyciekowych (Morele.net, ALAB laboratoria).
  * **Bezpieczeństwo Webowe (OWASP Top 10):** Podatność SQL Injection (`admin' OR '1'='1 --`) oraz ochrona poprzez *Prepared Statements*.
  * **Ataki po stronie przeglądarki:** Cross-Site Scripting (XSS) i kradzież sesji użytkownika.
  * **Memory Safety:** Dlaczego kod C/C++ generuje błędy *Buffer Overflow* i dlaczego nowoczesna branża stawia na język Rust.

---

## 🧪 Interaktywne Laboratorium na Żywo (CTF Lab)

1. **Kalkulator SHA-256 & Efekt Lawinowy:**
   * Dynamiczne hashowanie dowolnego tekstu w czasie rzeczywistym z użyciem `SubtleCrypto`.
   * Przełącznik dołączania soli kryptograficznej.
   * Porównanie hashów przy zmianie tylko 1 znaku (`Piesek123` vs `Piesek124`).
   * Gotowy snippet kodu Python do uruchomienia w Google Colab.
2. **Inspektor SMS Phishing (Makieta Smartfona):**
   * Interaktywny telefon z symulacją fałszywego SMS-a od InPost.
   * Uczeń musi kliknąć i zidentyfikować 4 czerwone flagi (presja czasu, mikrodopłata 1,50 zł, fałszywa domena, brak znaków diakrytycznych).
3. **Symulator SQL Injection:**
   * Formularz logowania ze spreparowanym payloadem `' OR '1'='1 --`.
   * Wizualizacja budowy zapytania SQL w locie i ominięcia logowania.
   * Przełącznik *Prepared Statements* pokazujący poprawne zabezpieczenie aplikacji przez programistę.
4. **Wyzwanie AI Red Teaming (Prompt Injection Guard):**
   * Wirtualny strażnik serwera INFOTECH pilnujący tajnej flagi `FLAG{INFOTECH_CYBER_2026}`.
   * Uczeń testuje techniki jailbreakowania promptu (wcielenie w rolę, tryb debugowania, poetycka ekstrakcja), aby przełamać instrukcje nadrzędne.

---

## 📋 Integracja z Google Classroom

W zakładce **„Zadania Classroom”** umieszczono gotowe treści zadań domowych i projektowych z opcją **kopiowania do schowka jednym kliknięciem**:
* **Zadanie LO (Lekcja 4):** *Zostań Audytorem Bezpieczeństwa* (weryfikacja maila w HaveIBeenPwned + wyjaśnienie fałszywego SMS-a dla babci).
* **Zadanie Tech (Moduł 2-3):** *Biały Wywiad (OSINT) & Skrypt Pętli Hashującej w Google Colab*.
* **Zadanie Web (Klasa 2):** *Audyt podatności SQL Injection i XSS*.

---

## 🚨 Moduł SOS & Zgłaszanie Incydentów

Dedykowany moduł bezpieczeństwa młodzieży w sieci:
* Bezpłatny numer SMS **8080** do natychmiastowego zgłaszania fałszywych SMS-ów do zespołu **CERT Polska**.
* Telefon Zaufania dla Dzieci i Młodzieży **116 111**.
* Procedura ratunkowa krok po kroku: *„Co zrobić, gdy ktoś włamał się na moje konto (Instagram / Discord / Gmail / BLIK)”*.

---

## 🎨 Design i Technologie

* **Stylistyka:** Cyberpunk Hacker Lab / Dark Neon (Glassmorphism, scanlines, glow).
* **Audio:** Wbudowany syntezator dźwięków cybernetycznych bazujący na natywnym **Web Audio API** (z opcją wyciszenia SFX).
* **Tryb Prezentacji:** Pełnoekranowe slajdy z obsługą klawiszy strzałek i notatkami dla nauczyciela.
* **Certyfikat:** Generator personalizowanego Certyfikatu Ukończenia Szkolenia do druku / PDF.
* **Technologie:** Semantyczny HTML5, nowoczesny Tailwind CSS, JavaScript ES6+. Zero zależności Node.js.
