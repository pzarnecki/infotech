# 🛡️ CYBERBEZPIECZEŃSTWO OD PODSTAW (Liceum Ogólnokształcące)
## Pakiet Dydaktyczny do Google Classroom: Lekcje 2, 3 oraz Wyzwanie Podsumowujące (Lekcja 4)
**Autor:** Przemysław Żarnecki • Program Edukacyjny INFOTECH 2026  
**Poziom:** Podstawowy (1 godzina tygodniowo) • **Środowisko:** Przeglądarka / Google Colab (brak instalacji lokalnej)

---

## 📌 METODYKA PROWADZENIA ZAJĘĆ
Każda lekcja została przygotowana według **modelu zoperacjonalizowanego**:
1. **Wprowadzenie i zarys problemu (5-7 min):** Realny case study z życia nastolatka lub głośny incydent w Polsce.
2. **Kluczowa wiedza merytoryczna:** Zwięzłe wyjaśnienie mechanizmu technicznego bez zbędnego żargonu akademickiego.
3. **Praktyczne laboratorium uczniowskie:** Samodzielna weryfikacja narzędziowa (HaveIBeenPwned, przeglądarka).
4. **Zadanie do oddania w Google Classroom:** Uczeń otrzymuje jasną instrukcję, kryteria oceniania NaCoBeZu (od 3 do 6) oraz gotowy formularz odpowiedzi.

---

# 📘 LEKCJA 2: Tajemnice Haseł, Wycieki Danych i Menedżery

### 🎯 Cele operacyjne (Co uczeń potrafi po lekcji?):
* Rozumie, dlaczego posiadanie jednego hasła na wielu portalach stanowi krytyczne zagrożenie (zjawisko *Credential Stuffing*).
* Potrafi wyjaśnić, czym różni się hasło przechowywane w bazie danych serwera od hasła jawnym tekstem.
* Zna zasady działania menedżerów haseł typu *Zero-Knowledge* (np. Bitwarden).
* Potrafi skonfigurować weryfikację dwuetapową 2FA w oparciu o aplikację TOTP.

---

### 📝 Treść merytoryczna dla Ucznia (Do wklejenia jako Post / Materiał w Classroom)

#### 1. Wstęp: Dlaczego "Piesek123" to najgorszy pomysł na świecie?
Zapewne masz konto w 20-30 serwisach: e-dziennik, Discord, Steam, Instagram, TikTok, sklepy z grami i ubraniami. Większość internautów używa jednego, względnie skomplikowanego hasła do wszystkich tych miejsc. **To kardynalny błąd!**

Hakerzy nie tracą czasu na bezpośrednie włamywanie się na Twoje konto na Instagramie czy do banku – te serwery mają potężne systemy ochronne. Zamiast tego atakują **słabo zabezpieczony mały sklep internetowy lub stare forum o grach**, kradną stamtąd całą bazę użytkowników (miliony adresów e-mail i haseł), a następnie za pomocą botów testują te same dane w innych serwisach. Zjawisko to nazywamy **Credential Stuffing**.

> **Wyobraź sobie, że masz jeden fizyczny klucz, który pasuje do drzwi Twojego domu, do szafki w szkole, do Twojego roweru i do sejfu w banku. Jeśli zgubisz ten klucz na basenie – tracisz kontrolę nad całym swoim życiem.** Dokładnie tym jest jedno hasło w sieci!

#### 2. Jak wygląda baza danych serwera?
W profesjonalnych systemach hasła nie są zapisywane zwykłym tekstem. Zamiast tego stosuje się **funkcje skrótu (hash)**, np. SHA-256 lub bcrypt.
* Tekst hasła: `Piesek123`
* Zabezpieczony hash w bazie: `a1b2c3d4e5f6...` (odcisk palca o stałej długości)
Niestety, jeśli hasło jest słabe i popularne (np. `123456`, `qwerty`, `admin`), przestępcy odgadują je w ułamku sekundy za pomocą gotowych słowników (tzw. Rainbow Tables).

#### 3. Trzy Złote Zasady Cyberhigieny:

* **Zasada 1: Jedno konto = Jedno unikalne hasło**  
  Nigdy nie używaj tego samego hasła w dwóch różnych miejscach. Jeśli wycieknie hasło z forum o grach, Twoja poczta i media społecznościowe pozostają bezpieczne.

* **Zasada 2: Menedżer Haseł (np. Bitwarden, Apple Keychain)**  
  „Jak mam zapamiętać 30 trudnych haseł typu `$k8#mP!92`?” – **nie musisz!** Od tego jest menedżer haseł. To cyfrowy, zaszyfrowany sejf (szyfrowanie AES-256), który sam wymyśla skomplikowane hasła i automatycznie uzupełnia je na stronach. Ty pamiętasz tylko **jedno hasło główne (Master Password)** do sejfu.

* **Zasada 3: Weryfikacja Dwuetapowa 2FA (Two-Factor Authentication)**  
  Włącz 2FA wszędzie, gdzie to możliwe (zwłaszcza na e-mailu!). Logowanie wymaga dwóch elementów:
  1. Coś, co wiesz (Twoje hasło).
  2. Coś, co masz (Twój telefon z aplikacją np. Google Authenticator lub Bitwarden).  
  Nawet jeśli haker pozna Twoje hasło w wyniku wycieku, **nie zaloguje się na konto bez Twojego fizycznego telefonu**.

---

# 🎣 LEKCJA 3: Phishing – Anatomia Oszustwa i Czerwone Flagi

### 🎯 Cele operacyjne (Co uczeń potrafi po lekcji?):
* Zna definicję phishingu i potrafi wskazać 4 psychologiczne mechanizmy manipulacji socjotechnicznej.
* Potrafi zdemaskować fałszywą domenę internetową oraz brak bezpiecznego protokołu HTTPS.
* Zna oficjalną procedurę zgłaszania złośliwych wiadomości SMS na bezpłatny państwowy numer **8080** (CERT Polska).

---

### 📝 Treść merytoryczna dla Ucznia (Do wklejenia jako Post / Materiał w Classroom)

#### 1. Czym jest Phishing?
**Phishing** (od słowa *fishing* – łowienie) to przestępstwo polegające na podszywaniu się pod zaufane firmy lub osoby (InPost, bank, policję, dyrektora szkoły, platformę Steam), aby wyłudzić od ofiary dane logowania, numer PESEL lub dane karty płatniczej.

#### 2. Cztery Czerwone Flagi – Jak rozpoznać oszusta?
1. **Sztuczna Presja Czasu i Panika:**  
   Oszuści zawsze piszą, że musisz kliknąć NATYCHMIAST: *„Paczka zostanie odesłana za 2 godziny!”*, *„Twoje konto bankowe zostanie zablokowane!”*. Pośpiech wyłącza racjonalne myślenie.
2. **Podstęp z Mikro-dopłatą (1,50 PLN):**  
   Dlaczego oszuści proszą o 1,50 zł, a nie o 1000 zł? Ponieważ drobna kwota nie budzi podejrzeń. Jednak fałszywa bramka płatności kradnie Twój login i hasło do banku!
3. **Fałszywa Domena (Adres strony):**  
   Zawsze czytaj adres strony **od prawej strony do lewej**, patrząc na tekst przed pierwszym ukośnikiem `/`:
   * Prawdziwy adres: `https://inpost.pl/sledzenie`
   * Fałszywy adres: `http://inpost-platnosci-paczka.pl/login` (domena to `inpost-platnosci-paczka.pl`, a nie `inpost.pl`!)
4. **Brak polskich znaków i literówki:**  
   Wiadomości tłumaczone automatycznie przez zagraniczne botnety często zawierają błędy gramatyczne i brak polskich liter (np. *„Twoja paczka zostala wstrzymana”*).

---

# 🏆 LEKCJA 4: WYZWANIE PODSUMOWUJĄCE (ZADANIE DO ODDANIA)
**Temat zadania w Google Classroom:** *Operacja „Tarcza Osobista” – Zostań Audytorem Bezpieczeństwa IT*  
**Typ wpisu:** Projekt Indywidualny • **Czas wykonania:** 45 min

---

### 📌 Treść polecenia dla Nauczyciela (Do wklejenia w Google Classroom):
```markdown
# 🛡️ ZADANIE: Operacja „Tarcza Osobista” – Zostań Audytorem Bezpieczeństwa IT
Termin oddania: Najbliższe zajęcia informatyki
Format: Wpisz odpowiedzi bezpośrednio w Classroomie wg poniższego formularza

DROGI UCZNIU!
W ramach podsumowania modułu bezpieczeństwa wcielasz się w rolę Niezależnego Audytora Bezpieczeństwa. Wykonaj dwa poniższe kroki i złóż raport w Classroomie.

---
### 🔍 KROK 1: Śledztwo w sieci (Wycieki tożsamości)
1. Wejdź na zaufaną stronę stworzoną przez ekspertów Microsoft ds. cyberbezpieczeństwa: https://haveibeenpwned.com/
2. Wpisz swój adres e-mail (lub adres testowy/kogoś z rodziny za jego zgodą).
3. Sprawdź, czy Twój e-mail pojawił się w ujawnionych wyciekach danych.
4. Jeśli pojawił się w wyciekach: zanotuj nazwę przynajmniej jednego serwisu, rok wycieku oraz kategorie wykradzionych danych (hasła, PESELe, numery telefonów). Jeśli jest czysty – gratulacje! Wpisz, że jest czysty i sprawdź popularny serwis, np. Adobe lub Canva.

---
### 📱 KROK 2: Analiza kryminalistyczna fałszywego SMS-a
Wyobraź sobie, że otrzymałeś na telefon wiadomość:
"Twoja paczka InPost zostala wstrzymana z powodu niedoplaty 1,50 PLN. Kliknij w link aby uregulowac kwote: http://inpost-platnosci-paczka.pl/login"

Odpowiedz na pytania w formularzu:
1. Wskaż dokładnie 2 czerwone flagi (dowody oszustwa) i wyjaśnij je prostym językiem – tak, jakbyś tłumaczył to swojej babci lub młodszemu rodzeństwu.
2. Dlaczego oszust żądał symbolicznej kwoty 1,50 zł, a nie np. 300 zł?
3. Na jaki bezpłatny numer telefonu w Polsce należy przekazać takiego SMS-a, aby analitycy zablokowali stronę oszusta w całym kraju?

---
### 📊 KRYTERIA OCENY (NaCoBeZu):
- Ocena Dostateczna (3): Sprawdzenie adresu w HIBP oraz wskazanie 1 czerwonej flagi w SMS.
- Ocena Dobra (4): Pełny audyt HIBP z podaniem nazwy serwisu + 2 czerwone flagi wyjaśnione prostym językiem.
- Ocena Bardzo Dobra (5): Ocena 4 + podanie poprawnego numeru CERT (8080) oraz sformułowanie 3 złotych zasad higieny cyfrowej dla domu.
- Ocena Celująca (6) - Wyzwanie Red Team: Dołączenie zrzutu ekranu potwierdzającego wdrożenie menedżera haseł (np. Bitwarden) lub włączenie weryfikacji dwuetapowej (2FA) na wybranym koncie (zrzut z zamazanymi danymi prywatnymi)!
```

---

### ✍️ Formularz Odpowiedzi dla Ucznia (Do skopiowania i uzupełnienia w Classroom):
```text
--- FORMULARZ ODPOWIEDZI UCZNIA (Wklej do Google Classroom) ---
Imię i Nazwisko: [TWOJE IMIĘ I NAZWISKO]
Klasa: [NP. 1A LICEUM]
Data wykonania: [RRRR-MM-DD]

1. WYNIK ŚLEDZTWA HAVEIBEENPWNED:
- Sprawdzony adres e-mail: [WPISZ ADRES LUB INFORMACJĘ: ADRES CZYSTY]
- Czy adres pojawił się w wyciekach?: [TAK / NIE]
- Nazwa serwisu i rok wycieku (jeśli dotyczy): [NP. Morele.net 2018 / Wattpad / Canva]
- Jakie kategorie danych wyciekły?: [NP. hashe haseł, numery telefonów, adresy e-mail]

2. DEKONSTRUKCJA ZŁOŚLIWEGO SMS-A:
- Czerwona flaga nr 1 (wraz z wyjaśnieniem dla babci): 
  [WPISZ TUTAJ: np. Presja czasu i straszenie, że paczka przepadnie...]
- Czerwona flaga nr 2 (wraz z wyjaśnieniem dla babci): 
  [WPISZ TUTAJ: np. Fałszywy adres strony inpost-platnosci-paczka.pl zamiast prawdziwego inpost.pl...]
- Dlaczego oszust zażądał tylko 1,50 zł?: 
  [WPISZ TUTAJ: np. Uśpienie czujności ofiary, żeby bez wahania podała login do banku...]
- Numer do zgłoszenia fałszywego SMS-a w Polsce: 
  [WPISZ NUMER: np. 8080 do zespołu CERT Polska]

3. MOJE REKOMENDACJE BEZPIECZEŃSTWA DLA RODZINY:
- Zasada 1: [Unikalne hasło 1:1...]
- Zasada 2: [Używanie menedżera haseł...]
- Zasada 3: [Weryfikacja dwuetapowa 2FA...]

4. WYZWANIE NA OCENĘ CELUJĄCĄ (6) - OPCJONALNE:
- [Opis wdrożenia Bitwarden / 2FA + dołączony zrzut ekranu jako załącznik w Classroomie]
----------------------------------------------------------------
```
